---
description: Análisis efímero para diagnóstico y exploración sin efectos secundarios
argument-hint: "query"
allowed-tools: ["Bash", "Read", "Grep", "Glob", "WebSearch", "WebFetch", "Task"]
agents: ["troubleshooter", "architect", "general-purpose", "shell-dev"]
primary-agent: troubleshooter
communication-mode: conversation
---

# Comando /explore - Análisis Efímero

Analiza "$ARGUMENTS" con análisis efímero que proporciona diagnóstico completo, exploración proactiva y análisis del repositorio con cero efectos secundarios.

## 🛡️ Garantías del Sistema

- ❌ No genera archivos permanentes
- ❌ No modifica estado del sistema
- ✅ Análisis inmediato en pantalla
- ✅ Detección automática de tipo

## 📊 Tipos de Análisis

### Diagnóstico Reactivo
Problemas activos, servicios fallando, errores observables

**Indicadores de disparo:**
- Palabras clave: "error", "failing", "down", "problema", "no funciona"
- Síntomas específicos descritos por usuario
- Referencias a logs, stacktraces, mensajes de error

**Enfoque:**
- Análisis sistemático de causa raíz
- Recolección de evidencia
- Hipótesis verificables
- Propuesta de soluciones ordenadas por probabilidad

### Exploración Proactiva
Opciones de implementación, evaluación de alternativas, análisis comparativo

**Indicadores de disparo:**
- Palabras clave: "opciones", "alternativas", "cómo", "mejor manera"
- Preguntas sobre posibilidades
- Evaluación de tecnologías

**Enfoque:**
- Análisis comparativo de opciones
- Evaluación de trade-offs
- Recomendaciones contextualizadas
- Consideraciones de implementación

### Análisis de Repositorio
Arquitectura, patrones, organización del código

**Indicadores de disparo:**
- Palabras clave: "cómo está organizado", "estructura", "arquitectura"
- Preguntas sobre el código existente
- Búsqueda de patrones

**Enfoque:**
- Análisis de estructura
- Identificación de patrones
- Evaluación de arquitectura
- Sugerencias de mejora

## 🤖 Coordinación de Agentes

- **Primario**: troubleshooter (diagnóstico y análisis sistemático)
- **Soporte**: architect (diseño), general-purpose (análisis general), shell-dev (exploración proactiva)
- **Modo**: conversation según protocolo CLAUDE.md

## 📋 Instrucción Principal

Ejecuta análisis efímero completo sin side effects para "$ARGUMENTS":

1. **Detectar tipo automáticamente** (diagnóstico vs exploración vs repositorio)
2. **Recolectar información** relevante del sistema
3. **Analizar y evaluar** según el tipo detectado
4. **Presentar findings** de forma estructurada
5. **Proponer next steps** cuando sea apropiado

## ⚠️ Restricciones Críticas

- **Sin modificaciones**: Nunca cambiar archivos o estado del sistema
- **Sin persistencia**: No generar documentos permanentes
- **Solo lectura**: Usar únicamente herramientas de lectura
- **Análisis inmediato**: Presentar resultados en la conversación actual

## 🎯 Output Esperado

Análisis estructurado que incluya:
- Tipo de análisis realizado
- Findings principales
- Evaluación según criterios relevantes
- Recomendaciones o next steps
- Referencias a documentación cuando aplique
