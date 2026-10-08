# METODOLOGÍA HÍBRIDA (CASCADA + SCRUM) EN LA ERA DE LA IA

**Objetivo:** Redefinir la gestión de proyectos de software. Cuando la IA escribe código a la velocidad de la luz, estimar tareas por "tiempo" es absurdo. La nueva métrica de dificultad es el **Nivel de Definición (Cero Ambigüedad)** y el orden de **Dependencias Lógicas**.

---

## 1. La Muerte del Tiempo y el Nacimiento de la Precisión
En Scrum tradicional, se estimaba que una tarea tomaría "3 días de código". Hoy, la IA genera esa tarea en 3 minutos. El "cuello de botella" ya no es la mecanografía humana, sino **la calidad del contexto entregado**. 

Si le das a la IA una instrucción vaga (*"Haz un login"*), la IA alucinará y perderás horas debugeando código inútil. Por ende, fusionaremos la planificación exhaustiva (Cascada) con la iteración rápida (Scrum).

---

## 2. FASE 1: CASCADA (Ingeniería de Contexto y Arquitectura)
*El diseño se hace a la antigua. La ejecución se hace con IA.*

Para que la IA funcione, necesita restricciones absolutas. En esta fase no se escribe código, se define el **Contrato Arquitectónico**. Aquí aplicamos Cascada porque **nada puede quedar vago**:

- **Definición Estricta (No más "User Stories" vagas):** Un requerimiento no es *"Como usuario quiero ver mi perfil"*. Ahora debe ser: *"Endpoint GET /perfil. Autenticación vía JWT. Debe consultar a la base de datos Supabase, tabla 'usuarios', retornando UUID y Email. Manejo estricto de error 404 y 401"*.
- **Diccionarios de Datos y Mermaid:** Antes de programar, debes generar la estructura de la Base de Datos y los diagramas de flujo. Este es el "mapa" que guiará a la IA. Si la arquitectura base cambia a la mitad, el contexto de la IA se rompe.
- **Acuerdo de Tecnologías (Stack Lock):** Se define todo el stack tecnológico y reglas de *Clean Code* desde el Día 1.

---

## 3. FASE 2: SCRUM ADAPTADO (Sprints de Dependencias, no de Tiempo)
*Adiós a los Sprints de 2 semanas. Hola a los Micro-Sprints Lógicos.*

Dado que la IA codifica rápido, la forma de priorizar el Backlog ya no es "qué podemos hacer en 15 días", sino **"qué pieza debe existir lógicamente antes que la otra"**.

### La Nueva Métrica: Grafo de Dependencias
1. **Priorización Estricta:** No puedes pedirle a la IA que programe el Frontend del carrito de compras si no has definido y bloqueado el Backend del carrito. 
2. **Jerarquía Lógica (El Orden de Requisitos Previos):**
   - Nivel 1: Configuración Base y Base de Datos (Tablas y Scripts DDL).
   - Nivel 2: Servicios Base / API / Endpoints (Sin UI).
   - Nivel 3: Interfaz de Usuario (UI) conectada a los Endpoints.
3. **El Sprint Híbrido:** Un "Sprint" ahora dura lo que tardes en definir la tarea y validar que la IA la generó correctamente. Mueves un ticket a *Done* cuando la IA devuelve el componente y las pruebas lógicas pasan.

---

## 4. El Rol del "Micro-Orquestador" (Human-in-the-Loop)
Bajo esta metodología híbrida, el desarrollador se convierte en un **Arquitecto Orquestador**:

1. Analizas el proyecto usando **Cascada** para obtener la visión global y diseñar el sistema con extremo detalle (Top-Down).
2. Divides ese gran sistema en tareas microscópicas y atómicas (Aislamiento de contexto).
3. Usas **Scrum Adaptado** para despachar estas micro-tareas una por una a la IA, validando la salida y ensamblando las piezas (Bottom-Up).

> **Ley de Oro de la Metodología Híbrida IA:**
> *"Diseña lento, documenta con precisión de francotirador, y deja que la IA construya a la velocidad de la luz. La ambigüedad es el mayor enemigo de la inteligencia artificial."*
