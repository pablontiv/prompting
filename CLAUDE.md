# CLAUDE.md

Guía técnica específica del repositorio para Claude Code.

**Para principios de comunicación y filosofía operativa, ver SYSTEM_PROMPT.md.**

## 📚 Comandos Disponibles

- `/explore [query]` - Análisis efímero sin efectos secundarios
- `/spec [feature]` - Especificación formal de features

Ver `.claude/commands/` para detalles de cada comando.

## 🤖 Sistema de Agentes

Agentes especializados disponibles:
- **general-purpose**: Análisis de código, documentación, tareas mixtas
- **troubleshooter**: Diagnóstico sistemático, análisis de causa raíz
- **architect**: Diseño de sistemas, validación arquitectural
- **product-owner**: Requisitos, estrategia de producto
- **shell-dev**: Scripts de automatización, integración sistema

## 🔖 Sistema de Identificadores

### Especificaciones Formales (`/spec`)
- **SPEC-XXX**: Especificaciones de features/componentes

Ver `.claude/commands/spec.md` para detalles de uso.

## 💬 Protocolo de Comunicación

### Claude Code debe:
- Cuestionar suposiciones ambiguas que impacten resultados
- Ofrecer alternativas cuando hay trade-offs significativos
- Resistir solo cuando hay mejora genuina posible
- Ser directo pero respetuoso
- Reconocer limitaciones transparentemente

### Prioridad de Información:
1. CLAUDE.md y repositorio local
2. Clarificación ante ambigüedad
3. Exploración externa solo con "explore"/"investigate"
4. Comandos y rutas exactamente como están escritos
5. Reportar discrepancias sin asumir resolución

### Modos de Operación:
- **🔍 EXPLORATION MODE**: Análisis, cuestionamiento, investigación (aplicar todos los principios)
- **⚡ EXECUTION MODE**: Ejecución con autonomía (solo cuestionamiento crítico)
- **🔧 TROUBLESHOOTING MODE**: Diagnóstico sistemático de problemas

### Modificadores:
- **"directo"**: Ejecutar sin cuestionar ni explicar extensivamente
- **"explora"**: Forzar EXPLORATION MODE completo

### Restricciones de Git:
- **NUNCA hacer commits**: Claude Code nunca debe ofrecer ni ejecutar `git add`, `git commit`, o `git push`
- **Solo modificar archivos**: El trabajo termina al completar cambios en archivos
- **Mostrar estado**: Usar `git status` para mostrar cambios pendientes
- **Commits son responsabilidad exclusiva del usuario**

## 📖 Estándares de Idioma y Código

- **Documentación**: Español - Documentación técnica, especificaciones
- **Código**: Inglés - Todo código, configuración, scripts
- **Comentarios de Código**: NUNCA - No agregar comentarios en código
- **Emojis**: NUNCA en código - Permitido en output-styles para claridad visual

## 📐 Estándares Técnicos

### Versionado:
- Git como única fuente de verdad
- Commits atómicos por acción
- Branches por feature
- Tags para releases

### Testing:
- Validación obligatoria pre-deploy
- Tests idempotentes
- Coverage mínimo 80%
- Tests unitarios y de integración

## 🗂️ Estructura del Proyecto

[Completar según tu proyecto específico]

## ⚙️ Configuración del Entorno

[Completar con comandos específicos de tu stack tecnológico]
