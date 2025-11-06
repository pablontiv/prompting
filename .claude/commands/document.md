---
description: Captura de conocimiento estructurado sin estados de implementación
argument-hint: "title"
allowed-tools: ["Write", "Read", "Grep", "Glob"]
agents: ["general-purpose"]
primary-agent: general-purpose
communication-mode: conversation
---

# Comando /document - Gestión de Conocimiento

Captura knowledge conversacional en "$ARGUMENTS" como documento estructurado sin compromisos de implementación.

## 🎯 Filosofía

Knowledge capture conversacional que preserva decisiones, análisis y experimentos SIN entrar en flujo de implementación formal. Memoria organizacional acumulativa del proyecto.

## 📋 Tipos de Documentos

### RESEARCH (RES-XXX)
Análisis de opciones, evaluaciones técnicas, comparativas

**Cuándo usar:**
- Evaluación de tecnologías o librerías
- Análisis comparativo de soluciones
- Investigación de best practices

**Estructura:**
- Contexto y motivación
- Opciones evaluadas
- Criterios de evaluación
- Findings y recomendaciones

### DECISION (DEC-XXX)
Registros de decisiones arquitecturales (ADRs)

**Cuándo usar:**
- Decisiones arquitecturales significativas
- Trade-offs conscientes
- Cambios de dirección técnica

**Estructura:**
- Contexto de la decisión
- Alternativas consideradas
- Decisión tomada y rationale
- Consecuencias esperadas

### EXPERIMENT (EXP-XXX)
Resultados de pruebas y configuraciones

**Cuándo usar:**
- Pruebas de concepto
- Experimentos técnicos
- Validación de hipótesis

**Estructura:**
- Hipótesis a validar
- Setup del experimento
- Procedimiento ejecutado
- Resultados y conclusiones

### CONVERSATION (CONV-XXX)
Archive completo de sesiones importantes

**Cuándo usar:**
- Sesiones de troubleshooting complejas
- Discusiones arquitecturales extensas
- Análisis profundos de problemas

**Estructura:**
- Contexto de la conversación
- Puntos clave discutidos
- Decisiones tomadas
- Follow-ups necesarios

## 🛡️ Garantías del Sistema

- 📋 Captura knowledge conversacional
- ✅ Documentos estructurados por tipo
- ✅ Referencias bidireccionales con especificaciones futuras
- ❌ Sin estados de implementación (no entra en flujo deploy)
- ❌ Sin compromisos de ejecución automática

## 🤖 Coordinación de Agentes

- **Primario**: general-purpose (knowledge management)
- **Modo**: conversation según protocolo CLAUDE.md

## 📁 Estructura de Archivos

Documentos se crean en `docs/` con subdirectorios por tipo:

```
docs/
├── research/
│   └── RES-001-evaluation-caching-solutions.md
├── decisions/
│   └── DEC-001-database-selection.md
├── experiments/
│   └── EXP-001-load-testing-api.md
└── conversations/
    └── CONV-001-architecture-review-session.md
```

## 📋 Instrucción Principal

Crea documento de knowledge capture para "$ARGUMENTS":

1. **Identificar tipo** automáticamente basado en contexto
2. **Asignar ID** secuencial (consultar docs/ para último número)
3. **Crear documento** con estructura según tipo
4. **Capturar conversación** actual si es relevante
5. **Agregar metadata** (fecha, autor, tipo, tags)
6. **Referencias cruzadas** a especificaciones si existen

## 🔗 Referencias Bidireccionales

Cuando documentes algo relacionado con especificaciones futuras:
- Crear link forward: "Ver SPEC-XXX cuando se implemente"
- Especificación futura debe referenciar este documento
- Mantener trazabilidad completa

## ⚠️ No Confundir Con

**`/document` NO es:**
- Especificación formal (eso es `/spec`)
- Compromiso de implementación
- Parte del flujo de deployment
- Reemplazo de documentación técnica estándar

**`/document` SÍ es:**
- Memoria organizacional
- Knowledge conversacional preservado
- Contexto para decisiones futuras
- Archive de análisis y exploración

## 🎯 Output Esperado

Documento markdown estructurado según el tipo, guardado en `docs/{tipo}/`, con:
- ID único y título descriptivo
- Metadata completa
- Contenido estructurado según plantilla del tipo
- Referencias cruzadas donde aplique
