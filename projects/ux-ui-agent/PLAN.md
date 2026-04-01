# PLAN — Agente UX/UI Landing

> Generado por el Agente Mano Derecha.
> Versión: 1.0 | Fecha: 2026-04-01 | Estado: `borrador`

---

## 1. Problema

El equipo necesita un agente especializado en diseño UX/UI que genere componentes y código listos para usar, con una estética minimalista y moderna, sin intervenir en el código existente.

## 2. Usuarios / audiencia

Uso interno — equipo de desarrollo que necesita componentes UI bajo demanda para una landing page.

## 3. Resultado mínimo aceptable (MVP)

- [ ] El agente responde solicitudes de diseño generando componentes React 19 + Tailwind
- [ ] El agente aplica un estilo minimalista/moderno de forma consistente
- [ ] El agente entrega solo lo que se le pide, sin modificar archivos existentes
- [ ] El agente puede generar secciones de landing (hero, features, CTA, footer, etc.)

## 4. Lo que NO incluye

- No sobreescribe ni modifica archivos existentes
- No toma decisiones de arquitectura del proyecto
- No define rutas, lógica de negocio ni integraciones
- No genera backend ni APIs

## 5. Decisiones cerradas

| Decisión | Valor | Razón |
|----------|-------|-------|
| Framework | React 19 | Definido por el equipo |
| Estilos | Tailwind CSS | Definido por el equipo |
| Estética | Minimalista moderna | Preferencia explícita del usuario |
| Plataforma | Web (landing page) | Scope definido |

## 6. Criterio de éxito

El agente entrega componentes React + Tailwind funcionales, con estética consistente, en respuesta a cualquier solicitud de UI — sin necesidad de correcciones de estilo y sin tocar archivos que no le fueron pedidos.

---

## 7. Agentes

### Agente Mano Derecha
- **Rol**: Planificación y contexto
- **Estado**: Plan entregado

### Agente UX/UI
- **Rol**: Diseño y generación de componentes
- **Objetivo**: Generar componentes React 19 + Tailwind con estética minimalista moderna bajo demanda
- **Output**: Código de componentes listos para copiar/usar
- **Estado**: `pendiente`

---

## 8. Historial de cambios

| Fecha | Cambio | Agente |
|-------|--------|--------|
| 2026-04-01 | Plan inicial creado | Mano Derecha |
