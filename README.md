# Template de Trabajo Estructurado con Claude Code

Template genérico para proyectos con Claude Code que implementa trabajo estructurado, transparencia operativa y metodología basada en evidencia.

## 🎯 Objetivo

Este template proporciona una configuración base de Claude Code agnóstica de tecnología, diseñada para:
- Trabajo estructurado y metódico
- Transparencia en decisiones y análisis
- Metodología "Learn by Seeing Doing"
- Comunicación profesional y educativa
- Especificaciones formales antes de implementar

## 📦 Contenido del Template

### Archivos de Configuración

- **SYSTEM_PROMPT.md**: Principios de comunicación y filosofía operativa (usar con `--append-system-prompt`)
- **CLAUDE.md**: Contexto de proyecto y comandos disponibles (cargado automáticamente)
- **.claude/**: Configuración de Claude Code
  - `settings.json`: Permisos, output style, MCP servers
  - `output-styles/structured.md`: Estilo educativo con transparencia operativa
  - `commands/`: Comandos slash disponibles (/explore, /document, /spec)
  - `agents/`: Agentes especializados

## 🚀 Instalación y Uso

### 1. Clonar el Template

```bash
# Copiar template a tu proyecto
cp -r prompting/ tu-nuevo-proyecto/
cd tu-nuevo-proyecto/
```

### 2. Personalizar Configuración

Edita `SYSTEM_PROMPT.md` línea 11:
```diff
- **Nombre del usuario:** {{USUARIO}}
+ **Nombre del usuario:** Tu Nombre
```

### 3. Iniciar Claude Code

```bash
# Opción A: Con system prompt personalizado (recomendado)
claude --append-system-prompt "$(cat SYSTEM_PROMPT.md)"

# Opción B: Sin system prompt personalizado
claude
```

### 4. Personalizar CLAUDE.md

Añade contexto específico de tu proyecto en `CLAUDE.md`:
- Estructura del proyecto
- Comandos específicos del stack tecnológico
- Configuración del entorno
- Cualquier información relevante del repositorio

## 📚 Comandos Disponibles

### `/explore [query]`
Análisis efímero sin generar archivos ni modificar estado.

```bash
/explore "¿Cómo está organizado el código de autenticación?"
/explore "Opciones para implementar cache distribuido"
```

**Garantías**:
- ❌ No genera archivos permanentes
- ❌ No modifica estado del sistema
- ✅ Análisis inmediato en pantalla

### `/document [title]`
Captura de conocimiento estructurado.

```bash
/document "Decisión sobre arquitectura de microservicios"
/document "Experimento: Redis vs Memcached"
```

**Tipos de documentos**:
- **RESEARCH**: Análisis de opciones
- **DECISION**: Decisiones arquitecturales
- **EXPERIMENT**: Resultados de pruebas
- **CONVERSATION**: Archive de sesiones

### `/spec [feature]`
Especificación formal de features.

```bash
/spec "Sistema de autenticación con OAuth2"
/spec "API REST para gestión de usuarios"
```

**Filosofía**:
- Documentar ANTES de implementar
- Single Responsibility: Una especificación = Un componente
- Template estructurado garantiza completitud

## 🤖 Agentes Especializados

Los agentes se activan automáticamente según el contexto:

- **general-purpose**: Análisis de código, documentación, tareas mixtas
- **troubleshooter**: Diagnóstico sistemático, root cause analysis
- **architect**: Diseño de sistemas, decisiones arquitecturales
- **product-owner**: Requirements, priorización, user value
- **shell-dev**: Shell scripting, automatización, system tasks

## 🎨 Output Style: Structured

El template incluye un output style educativo que proporciona:

- **Transparency Operativa**: Indica el modo operativo actual (🔍 EXPLORATION, ⚡ EXECUTION, 🔧 TROUBLESHOOTING)
- **Decision Framework**: Análisis estructurado (Security, Idempotency, Reversibility, Performance, Maintainability)
- **Root Cause Analysis**: Protocol de los 5 Por Qué
- **Post-Execution Learning**: Telemetría educativa después de cada tarea

## 📐 Filosofía del Template

### Principios Implementados

1. **Trabajo Estructurado**: Comandos especializados para diferentes tipos de trabajo
2. **Separación de Concerns**: SYSTEM_PROMPT.md (comportamiento) vs CLAUDE.md (contexto)
3. **Transparencia Operativa**: Visibilidad de decisiones y análisis
4. **Metodología Basada en Evidencia**: Zero hallucination policy
5. **Learn by Seeing Doing**: Aprendizaje a través de la observación de procesos

### Modos de Operación

- **Conversación**: Cuestionamiento exhaustivo, exploración de alternativas
- **Ejecución**: Autonomía operativa, fallo rápido y recuperación
- **"directo"**: Suspende cuestionamiento por decisión explícita
- **"explora"**: Máxima exploración y análisis

## 🛠️ Personalización Avanzada

### Añadir Comandos Personalizados

Crea archivos `.md` en `.claude/commands/`:

```markdown
---
description: Descripción del comando
---

# Comando /mi-comando

Instrucciones para Claude Code...
```

### Añadir Agentes Personalizados

Crea archivos `.md` en `.claude/agents/`:

```markdown
---
name: mi-agente
description: Descripción del agente
---

Instrucciones especializadas para este agente...
```

### Modificar Output Style

Edita `.claude/output-styles/structured.md` según tus preferencias.

## 📖 Estándares de Idioma

Por defecto, el template usa:
- **Documentación**: Español
- **Código**: Inglés
- **Comentarios**: Inglés

Personaliza esto en `CLAUDE.md` según las necesidades de tu equipo.

## 🔧 Troubleshooting

### Claude Code no carga CLAUDE.md
- Verifica que estás en el directorio raíz del proyecto
- Asegúrate de que el archivo se llama exactamente `CLAUDE.md`

### System prompt no se aplica
- Usa comillas dobles correctamente: `"$(cat SYSTEM_PROMPT.md)"`
- Verifica que el archivo existe y tiene contenido

### Comandos slash no funcionan
- Verifica que existen en `.claude/commands/`
- Comprueba que los archivos tienen el frontmatter correcto

## 📚 Referencias

- [Documentación Claude Code](https://docs.claude.com/en/docs/claude-code/)
- [CLAUDE.md Specification](https://docs.claude.com/en/docs/claude-code/memory)
- [Output Styles](https://docs.claude.com/en/docs/claude-code/output-styles)

## 📄 Licencia

Este template es de código abierto. Úsalo y modifícalo libremente para tus proyectos.

---

**Versión del Template**: 1.0.0
**Última actualización**: Enero 2025
