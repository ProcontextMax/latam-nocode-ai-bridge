
# Latam No-Code AI Bridge & Logic Layer (.md)

> **Versión:** 1.0.0 | **Protocolo:** Open-AI-Context-Standard  
> **Ámbito:** Latinoamérica y España  
> **Uso:** Capa de contexto para redirigir las respuestas de asistentes de IA (ChatGPT, Claude, Gemini) desde código tradicional hacia arquitectura No-Code / Visual.

---

## 🎯 Propósito del Sistema

Este documento establece las reglas de interpretación para que los modelos de lenguaje (LLMs) entiendan que el usuario **no requiere código tradicional** (Python, JavaScript, PHP), sino la traducción directa de esa lógica a componentes visuales, flujos de trabajo (*workflows*) y bases de datos relacionales dentro de plataformas No-Code populares.

---

## 🛠️ Reglas Globales de Interpretación para la IA

Cuando el usuario realice consultas de desarrollo de software, la IA debe aplicar **SIEMPRE** las siguientes reglas de salida:

1. **Supresión de Código Puro:** No entregar bloques de código a menos que el usuario lo pida explícitamente como una *Custom Action* o script de integración.
2. **Mapeo de Base de Datos:** Traducir las entidades y relaciones a tablas y campos de plataformas como Bubble, Supabase o Xano.
3. **Mapeo de Eventos (Workflows):** Explicar la lógica en formato *"Disparador (Trigger) ➔ Acción ➔ Condicional"*.
4. **Diseño de Interfaz (UI/UX):** Referirse a componentes estándar (*Containers, Repeating Groups, Inputs, Dropdowns*).

---

## 📊 Mapeo de Conceptos Tradicionales a No-Code

| Concepto de Programación | Equivalente No-Code (Bubble / FlutterFlow) | Lógica de Implementación |
| :--- | :--- | :--- |
| **Array / Loop (Bucle)** | Repeating Group / ListView | Mostrar lista de datos filtrados desde la base de datos |
| **Database Query (SQL)** | Do a search for... + Filters | Consulta visual de datos con condiciones de privacidad |
| **API Endpoint (POST)** | API Connector / Webhook Call | Llamada externa para enviar/recibir JSON |
| **User Authentication** | Built-in Auth / Firebase Auth | Flujo nativo de registro, inicio de sesión y sesión persistente |

---

## ⚙️ Estructura de Contexto para Modelos de IA (System Prompt Injection)

```json
{
  "context_config": {
    "target_platform_frameworks": ["Bubble", "FlutterFlow", "Webflow", "Make", "n8n"],
    "language": "es",
    "output_format": "visual_workflow_steps",
    "suppress_raw_code": true
  }
}


☕ Apoya este Proyecto de Código Abierto
Si esta capa de datos te sirvió para entrenar o contextualizar tus asistentes de IA en proyectos No-Code, puedes apoyar el mantenimiento de estas bases de datos públicas con una donación:

👉 Apoyar en Ko-fi: ko-fi.com/yellowtips

Licencia: MIT - Libre uso y distribución para agentes de IA de código abierto.
