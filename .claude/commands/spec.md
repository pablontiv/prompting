---
description: Especificación formal de features con template estructurado
argument-hint: "feature-description"
allowed-tools: ["Write", "Read", "Grep"]
agents: ["architect", "product-owner"]
primary-agent: architect
communication-mode: conversation
---

# Comando /spec - Especificación Formal

Crea especificación formal para "$ARGUMENTS" aplicando protocolo CLAUDE.md conversation mode.

## 🎯 Filosofía

- **Documentar ANTES de implementar**
- **Template estructurado** garantiza completitud
- **Single Responsibility**: Una especificación = Un componente
- **Validación de assumptions**: Cuestionar, no asumir

## 📋 Template YAML Obligatorio

```yaml
metadata:
  id: SPEC-XXX
  title: "Título descriptivo"
  created_date: "YYYY-MM-DD"
  author: "Tu nombre"
  category: "feature|bugfix|refactor|docs"

spec:
  requirements:
    functional:
      - "Requisito funcional 1"
      - "Requisito funcional 2"
    non_functional:
      - "Requisito no funcional 1"
      - "Requisito no funcional 2"
    constraints:
      - "Restricción técnica 1"
      - "Restricción técnica 2"

  implementation_plan:
    approach: "Descripción del enfoque técnico"
    components:
      - "Componente 1"
      - "Componente 2"
    dependencies:
      - "Dependencia técnica 1"
      - "Dependencia técnica 2"
    risks:
      - "Riesgo identificado 1"
      - "Riesgo identificado 2"

  testing_strategy:
    validation_criteria:
      - "Criterio de validación 1"
      - "Criterio de validación 2"
    test_scenarios:
      - "Escenario de prueba 1"
      - "Escenario de prueba 2"
    acceptance_criteria:
      - "Criterio de aceptación 1"
      - "Criterio de aceptación 2"
```

## 🔍 Proceso de Especificación

1. **Cuestionar assumptions** del usuario
   - ¿Es realmente un solo componente o múltiples?
   - ¿Están claros todos los requirements?
   - ¿Hay dependencias ocultas?

2. **Validar requirements** bien definidos
   - Funcionales: QUÉ debe hacer
   - No funcionales: CÓMO debe comportarse
   - Constraints: Limitaciones técnicas

3. **Evaluar alternativas**
   - Diferentes enfoques técnicos
   - Trade-offs de cada opción
   - Recomendación con rationale

4. **Crear especificación completa**
   - Directorio `docs/specs/SPEC-XXX-nombre/`
   - Archivo `spec.yml` con template completo
   - Documentar decisiones y trade-offs

## 🤖 Coordinación de Agentes

- **Primario**: architect (diseño y validación arquitectural)
- **Soporte**: product-owner (requirements y estrategia)
- **Modo**: conversation según protocolo CLAUDE.md

## ⚖️ Principio de Single Responsibility

**CRÍTICO**: Una especificación = Un componente

✅ **Correcto**:
- SPEC-001-authentication-service
- SPEC-002-user-database
- SPEC-003-api-gateway

❌ **Incorrecto**:
- SPEC-001-backend-stack (múltiples componentes)
- SPEC-002-complete-application (demasiado amplio)

Si detectas múltiples componentes en "$ARGUMENTS", dividir automáticamente en especificaciones separadas.

## 📁 Estructura de Archivos

```
docs/specs/
├── SPEC-001-authentication/
│   ├── spec.yml
│   └── README.md (opcional)
├── SPEC-002-database/
│   ├── spec.yml
│   └── README.md (opcional)
└── spec-template/
    ├── spec.yml
    └── README.md
```

## 🎯 Output Esperado

Especificación completa que incluya:
- Metadata con ID único
- Requirements completos (functional, non_functional, constraints)
- Implementation plan detallado
- Testing strategy definida
- Decisiones arquitecturales documentadas
- Trade-offs considerados y explicados
