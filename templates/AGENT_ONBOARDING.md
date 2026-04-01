# Agent Onboarding — [ROL DEL AGENTE]

> Completado por el Orquestador antes de instanciar el sub-agente.
> Proyecto: [NOMBRE] | Fecha: [FECHA]

---

## Bloque 1 — Identidad

**01. ¿Cuál es el rol exacto de este agente dentro del proyecto?**

[respuesta]

**02. ¿Cuál es el único objetivo que debe completar?**

[respuesta — un objetivo, un párrafo]

**03. ¿Cuál es el output concreto que debe entregar?**

- Formato: [archivo / análisis / código / decisión]
- Ubicación: `[ruta exacta]`
- Nombre del archivo / entregable: `[nombre]`

---

## Bloque 2 — Contexto del proyecto

**04. ¿Qué ya existe en el proyecto que este agente debe conocer?**

[Extraído de mem_context + PLAN.md. Incluir solo lo relevante para este agente.]

**05. ¿Qué restricciones o decisiones ya están cerradas?**

[Lista. No opiniones, hechos.]

- [restricción 1]
- [restricción 2]

**06. ¿Con qué otros agentes interactúa y cómo?**

| Agente | Tipo | Qué recibe / entrega |
|--------|------|----------------------|
| [nombre] | upstream | [descripción] |
| [nombre] | downstream | [descripción] |

---

## Bloque 3 — Scope y límites

**07. ¿Qué está explícitamente fuera de su scope?**

- [NO hacer 1]
- [NO hacer 2]

**08. ¿Cuándo debe escalar al Orquestador en vez de decidir solo?**

- [condición 1]
- [condición 2]

**09. ¿Cómo sabe que terminó correctamente?**

[Criterio de done verificable. El Orquestador usa esto para validar.]

---

## Checklist del Orquestador

- [ ] Las 9 preguntas respondidas
- [ ] Guardado en `projects/[proyecto]/PLAN.md` sección `## Agentes`
- [ ] `mem_save` ejecutado con `type: "agent-init"`
- [ ] Sub-agente instanciado con este documento como contexto inicial
