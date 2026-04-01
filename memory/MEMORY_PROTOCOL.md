# Memory Protocol — Engram

Protocolo de uso de Engram para todos los agentes del sistema.

---

## Instalación

```bash
brew install gentleman-programming/tap/engram
```

Configurar en `~/.claude/settings.json`:
```json
{
  "mcpServers": {
    "engram": {
      "command": "engram",
      "args": ["mcp"]
    }
  }
}
```

---

## Las 4 herramientas principales

| Herramienta | Cuándo usarla |
|-------------|---------------|
| `mem_context` | Al iniciar sesión, después de compactación |
| `mem_search` | Antes de empezar cualquier tarea nueva |
| `mem_save` | Después de decisiones, descubrimientos, hitos |
| `mem_session_summary` | Al finalizar la sesión o un sub-agente |

---

## Tipos de memoria (`type` en mem_save)

| Tipo | Uso |
|------|-----|
| `decision` | Decisión de arquitectura o diseño |
| `bugfix` | Problema resuelto y cómo se resolvió |
| `architecture` | Estructura del sistema o componente |
| `agent-init` | Onboarding completado de un sub-agente |
| `discovery` | Hallazgo importante durante investigación |
| `constraint` | Restricción nueva identificada |

---

## Formato obligatorio para mem_save

```
title: [verbo + objeto corto]
type: [uno de los tipos de arriba]
content:
  What: qué pasó o qué se decidió
  Why: por qué se tomó esta decisión
  Where: en qué parte del proyecto aplica
  Learned: qué aprendimos que sirve para el futuro
```

---

## Formato para mem_session_summary

```
Goal: qué se intentaba lograr en esta sesión
Discoveries: qué se aprendió que no se sabía antes
Accomplished: lista de lo que se completó
Files: archivos creados o modificados con su ruta
```

---

## Git Sync

Sincronizar memoria con el repositorio:

```bash
# Exportar memorias nuevas al repo
engram sync

# Commit
git add .engram/ && git commit -m "chore: sync engram memories"

# En otra máquina o sesión nueva
engram sync --import
```

El directorio `.engram/` se incluye en el repo. El archivo `engram.db` está en `.gitignore`.

---

## Reglas para todos los agentes

1. **Nunca inventes contexto.** Si no sabes, llama `mem_search` primero.
2. **mem_context es lo primero** en cada sesión, sin excepciones.
3. **mem_session_summary es lo último** antes de cerrar, sin excepciones.
4. Si Engram no tiene la información, pregunta al usuario. No asumas.
