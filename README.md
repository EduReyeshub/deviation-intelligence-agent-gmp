# Deviation Intelligence Agent · GMP

Agente conversacional para análisis estructurado de desviaciones en manufactura farmacéutica bajo BPM/GMP.

Construido con context engineering aplicado a procesos industriales regulados.

## El problema que resuelve

El análisis de desviaciones es crítico, repetitivo y dependiente del criterio del experto disponible. La profundidad varía según experiencia, presión operativa y tiempo disponible.

Este agente no reemplaza al especialista en Calidad. Le da estructura para que no se le escape nada.

## Lo que hace

Guía el análisis paso a paso con criterios BPM/GMP reales:

- Clasifica la desviación con justificación explícita (crítica, mayor, menor)
- Conduce el Ishikawa de 6M completo, una categoría a la vez
- Aplica 5 Por qués hasta causa raíz sistémica
- Evalúa impacto a lotes con pausa obligatoria si hay riesgo en mercado
- Genera borrador de CAPA con plazos proporcionales al riesgo (ICH Q9(R1))

En cada decisión crítica indica: "Esta conclusión requiere validación del especialista en Calidad."

## Decisión de diseño clave

Incluye Human-in-the-Loop en cada paso relevante. La sexta M del Ishikawa (Medición) está explícitamente incluida: calibración, validación de métodos y trazabilidad metrológica. La mayoría de agentes genéricos no la consideran.

## Normativa de referencia

NOM-059-SSA1 · FEUM · ICH Q9(R1) · ICH Q10 · 21 CFR Part 211

## Cómo usarlo

1. Abre claude.ai y crea un Project nuevo
2. En "Instrucciones del proyecto" pega el contenido del archivo system-prompt-v5.md
3. Inicia una conversación y escribe tu caso o escribe "caso hipotético" para practicar

Cuenta gratuita funciona para casos cortos. Plan Pro recomendado para el flujo completo.

## KPIs de evaluación

El agente se evalúa con 4 indicadores propios:

TCC · Tasa de Clasificación Correcta — ¿clasificó bien la desviación? Escala: 0% / 50% / 100%

TAR · Tasa de Alucinación Regulatoria — ¿citó normativa inexistente? Escala: 0 es el único resultado aceptable.

UBC · Utilidad del Borrador CAPA — ¿qué tan aprovechable es el CAPA generado? Escala: 1 a 5.

TAC · Tiempo de Análisis Completo — ¿cuántos minutos tomó el flujo? Rango óptimo: 15 a 25 minutos.

## Historial de versiones

v1 · System prompt base · Ishikawa 5M (error técnico)
v2 · 6M corregidas · ICH Q9(R1) · proporcionalidad de riesgo
v3 · Plazos CAPA por criticidad
v4 · Banco de casos hipotéticos · mensaje de bienvenida mejorado
v5 · Instrucción de respuesta flexible · versión publicable

## Casos de prueba

C1 · Desviación de limpieza en línea de llenado aséptico
C2 · Excursión de presión diferencial en área Grado A/B
C3 · Fallo de calibración en termohigrómetro

## Contexto del proyecto

Proyecto 1 del portafolio AI Department Design — sistemas de agentes IA que augmentan departamentos de Calidad, Mejora Continua y Validación en manufactura regulada LATAM.

Desarrollado por Jesús Eduardo Reyes Jacinto · Ingeniero Bioquímico · LSS Black Belt · Doctorando en Ciencias en Innovación · UAGro

## Retroalimentación

Si pruebas el agente y trabajas en calidad farmacéutica o mejora continua, abre un Issue o contáctame por LinkedIn. Toda retroalimentación es bienvenida.

*Este agente genera hipótesis de trabajo, no decisiones regulatorias. Todo output requiere validación del especialista en Calidad responsable.*
