# MANUAL DE LEVANTAMIENTO DE REQUISITOS (ERA IA)

**Objetivo:** Modernizar la Ingeniería de Requisitos. Dejar atrás los documentos de 100 páginas que nadie lee y usar la IA para descubrir rápidamente el **problema raíz**, definir un alcance estricto (MVP) y aniquilar la "parálisis por perfeccionismo".

---

## 1. El Cambio de Paradigma (Tu rol ya no es escribir)
En la era tradicional, perdías semanas dibujando Diagramas de Entidad-Relación (ER) a mano para descubrir luego que el cliente quería otra cosa.
**En la Era IA:** 
Tu labor es ser el **Filósofo del Problema**. Tu trabajo es hacer las preguntas correctas, establecer las restricciones y decirle al cliente *"No"*. La IA se encargará de redactar los Casos de Uso y dibujar los diagramas ER (Mermaid) en 10 segundos para que tú solo valides la lógica (Top-Down).

---

## 2. El Prompt Maestro: "El Descubridor de Problemas"
*Usa este prompt con tu IA para prepararte antes de hablar con tu cliente (o contigo mismo si el proyecto es tuyo).*

> **Copia y pega esto en tu IA:**
> "Actúa como un Product Manager Senior. Voy a tener una reunión con un cliente (o conmigo mismo) para un nuevo proyecto de software. El contexto inicial que me dieron es: *[INSERTA AQUÍ LA IDEA BÁSICA, Ej: 'Quiero una app para pasear perros']*. 
> 
> Tu misión es no aceptar esa premisa inicial. Haz lo siguiente:
> 1. Dame **5 preguntas contraintuitivas** que debo hacer para descubrir el *verdadero* problema de negocio (El síntoma vs. La enfermedad).
> 2. Sugiéreme **3 métricas de éxito medibles** (KPIs) para saber si la app funcionó.
> 3. Define un límite estricto de **'MVP' (Producto Mínimo Viable)**: Dime qué 3 funcionalidades son absolutamente obligatorias y cuáles 5 debemos prohibir en la primera versión para evitar la parálisis por perfeccionismo."

---

## 3. ¿Cómo saber cuál es el "Verdadero Problema"?
El cliente siempre te pide la solución que él se imaginó (Ej: *"Necesito que me hagas un chatbot con IA para mi web"*). Tu trabajo es usar los **5 Porqués** para llegar al fondo.
- *Cliente:* Quiero un chatbot.
- *Tú:* ¿Por qué?
- *Cliente:* Porque la gente se va de mi web sin comprar.
- *Tú:* ¿Por qué se van?
- *Cliente:* Porque no encuentran los precios.
- **El Verdadero Problema:** La interfaz de usuario oculta los precios. **Solución:** Cambiar el diseño visual. *No necesitabas programar un chatbot.*

---

## 4. El Escudo Anti-Perfeccionismo (Cuándo detener el desarrollo)
El perfeccionismo es el asesino número uno de los programadores. Te mantiene mejorando código en tu computadora sin que nadie lo use. Para evitar esto, debes definir la **Línea de la Muerte (Done Criteria)**:

1. **Anclaje Dinámico:** Acepta que tu visión inicial será borrosa. No intentes diseñar la base de datos perfecta para 5 años en el futuro. Diseña la base de datos para los próximos 3 meses.
2. **Si no duele, lo lanzaste muy tarde:** El producto debe lanzarse apenas resuelva el "Verdadero Problema" (Punto 3). Si la UI es un poco fea, pero el usuario puede registrarse y hacer la tarea principal, **SE LANZA**.
3. **El alcance es sagrado (Scope Creep):** Si en medio del desarrollo a ti o al cliente se les ocurre una "idea genial", no se programa. Se anota en una lista llamada `v2.0` y se ignora hasta que el MVP esté en producción.

---

## 5. Aceleración con IA (Generación Rápida de ERs)
Una vez que el alcance está cerrado y bloqueado, no pierdas tiempo dibujando.

*Usa este prompt:*
> "El alcance del MVP está cerrado y es el siguiente: *[Pega las funcionalidades clave]*. 
> Actúa como Arquitecto de Bases de Datos. Générame el esquema inicial de tablas en formato **Mermaid (Entity-Relationship Diagram)** que cubra solo este MVP, asegurándote de estar en Tercera Forma Normal (3FN). No agregues tablas 'por si acaso en el futuro las usamos'."

*La IA generará el código. Tú (el Arquitecto) solo lo lees, lo debates, corriges la lógica si es necesario, y pasas directamente a programar.*
