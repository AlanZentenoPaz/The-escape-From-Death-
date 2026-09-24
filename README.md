# The Escape From Death

Videojuego 3D de supervivencia y escape desarrollado como parte del **Proyecto 0: Equipo y diseño preliminar del juego**.

## Descripción del proyecto

**The Escape From Death** es un videojuego 3D de supervivencia y escape para un jugador. El jugador controla a un sobreviviente que debe explorar un bosque industrial abandonado, reparar **tres generadores** y escapar por una puerta de salida mientras evita a un enemigo controlado por inteligencia artificial.

El objetivo principal es completar los tres generadores, utilizar estratégicamente los recursos disponibles, evitar al enemigo y llegar a la salida antes de quedarse sin vida.

---

## Equipo

| Integrante                           | Responsabilidad principal          |
| ------------------------------------ | ---------------------------------- |
| **Alan Zenteno Paz**                 | Inteligencia artificial y sistemas |
| **Karen Valencia Rodriguez**         | Diseño y arte del juego            |
| **Jhonatan Martín Gozález Martínez** | Pruebas, rendimiento y calidad     |
| **Gustavo Angel Aragon Aragon**      | Programación e integración         |

Cada integrante cuenta con una responsabilidad principal, pero el desarrollo se realizará de manera colaborativa, apoyando otras áreas cuando sea necesario. El proyecto se gestionará mediante un repositorio compartido utilizando commits para registrar los cambios.

---

## Bucle central

El bucle principal del juego es:

**Explorar → localizar generadores y cofres → reparar generadores → evitar al enemigo → utilizar recursos y trampas → completar los 3 generadores → desbloquear la puerta → escapar.**

### Generadores

El escenario contiene **3 generadores**. Cada uno debe alcanzar el **100 % de reparación**.

Cuando los tres generadores están completos, la puerta de salida se desbloquea.

### Cofres

Existen **3 cofres**, cada uno con un recurso diferente:

* ** Granada de luz:** aturde temporalmente al enemigo.
* ** Pieza de generador:** añade **50 % de progreso** a un generador.
* ** Jeringa:** recupera toda la vida perdida.

Cada recurso tiene un único uso.

### Trampas

El jugador puede activar estructuras defensivas.

Cuando el enemigo pasa por una trampa activada, queda **inmovilizado durante 20 segundos**.

### Enemigo

El enemigo está controlado mediante inteligencia artificial y cuenta con diferentes comportamientos:

* Patrullaje
* Detección
* Persecución
* Ataque
* Aturdimiento
* Inmovilización

---

## Condiciones de victoria y derrota

### Victoria

El jugador gana cuando:

1. Repara los tres generadores.
2. Desbloquea la puerta de salida.
3. Llega a la salida y escapa.

### Derrota

El jugador pierde cuando la vida del sobreviviente llega a **cero**.

---

## Controles

| Tecla             | Acción          |
| ----------------- | --------------- |
| **W / A / S / D** | Movimiento      |
| **Shift**         | Correr          |
| **E**             | Interactuar     |
| **F**             | Utilizar objeto |
| **Esc**           | Pausa           |

El jugador podrá seleccionar entre un personaje masculino y uno femenino. Ambos personajes tendrán las mismas mecánicas.

---

## Nivel

El prototipo contará con **un único escenario de tamaño reducido**, inspirado visualmente en un bosque industrial abandonado, pero con diseño propio.

El escenario incluirá:

* Bosque
* Estructuras
* 3 generadores
* 3 cofres
* Trampas
* Zona inicial
* Zona de patrulla del enemigo
* Puerta de salida

---

## Agentes autónomos

El prototipo incorporará al menos **15 agentes autónomos**:

* **1 enemigo principal** controlado mediante IA.
* **14 agentes ambientales** con comportamientos sencillos.

El enemigo utilizará estados de patrulla, detección, persecución y ataque, además de estados temporales de aturdimiento e inmovilización.

Para evaluar el rendimiento se medirán:

* FPS promedio.
* FPS mínimo.
* Uso aproximado de CPU/GPU.
* Cantidad de agentes activos.

El objetivo inicial será mantener **30 FPS estables** y posteriormente optimizar el proyecto para **60 FPS**, especialmente en equipos con gráficos integrados.

---

## Tecnologías

* **Motor:** Godot Engine 4.7.2
* **Lenguaje:** GDScript
* **Sistema operativo:** Windows 11

Godot será utilizado por su soporte para desarrollo 3D, navegación de agentes, interfaces, animaciones y lógica de juego.

---

## Hardware de desarrollo

| Equipo   | Hardware                                         |
| -------- | ------------------------------------------------ |
| Equipo 1 | RTX 5070 · Ryzen 7 5800XT · 32 GB RAM            |
| Equipo 2 | RTX 5060 · Ryzen 7 5700G · 32 GB RAM             |
| Equipo 3 | Ryzen 7 7840HS · Gráficos integrados · 48 GB RAM |
| Equipo 4 | Hardware por especificar                         |
| Equipo 5 | AMD E1-1200 · Gráficos integrados · 6 GB RAM     |
| Equipo 6 | Hardware por especificar                         |

El proyecto será probado en los diferentes equipos disponibles para comprobar su funcionamiento y rendimiento.

---

## Alcance mínimo

El prototipo debe incluir:

* [ ] Movimiento y selección de personaje.
* [ ] Un escenario jugable.
* [ ] 3 generadores y sistema de reparación.
* [ ] 3 cofres y sus recursos.
* [ ] Trampas.
* [ ] Enemigo con IA.
* [ ] Sistema de vida.
* [ ] Puerta y condiciones de victoria/derrota.
* [ ] 15 agentes autónomos.
* [ ] Pruebas de rendimiento a 30 y 60 FPS.

---

## Posibles ampliaciones

Las siguientes características quedan fuera del alcance mínimo y podrán desarrollarse posteriormente:

* Más enemigos.
* Más escenarios.
* Nuevos objetos.
* Diferentes niveles de dificultad.
* Sistema de puntuación.
* Más tipos de trampas.
* Animaciones adicionales.
* Efectos visuales y sonoros avanzados.

---

## Riesgos y reducción de alcance

| Riesgo                                         | Reducción de alcance                                                                                 |
| ---------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| La IA del enemigo requiere demasiado tiempo    | Utilizar una máquina de estados sencilla con patrulla, detección, persecución y ataque.              |
| Los 15 agentes afectan el rendimiento          | Mantener 14 agentes ambientales con comportamientos simples y reducir actualizaciones no esenciales. |
| El escenario 3D consume demasiado tiempo       | Utilizar un único mapa pequeño con elementos reutilizables.                                          |
| Los modelos y animaciones retrasan el proyecto | Utilizar recursos provisionales o con licencia compatible y priorizar las mecánicas.                 |

---

## Uso de inteligencia artificial

El proyecto contempla tres formas de utilización de IA:

### Generación de recursos

Se podrá utilizar IA generativa para crear conceptos visuales y referencias para el escenario y los objetos.

### Programación asistida

Se podrá utilizar un LLM para apoyar en:

* Generación de código GDScript.
* Explicación de código.
* Depuración.
* Revisión del código.

Todo código generado con asistencia será probado y validado por el equipo.

### IA durante la partida

La IA del enemigo será implementada directamente en Godot mediante:

* Navegación.
* Detección.
* Máquina de estados.

El enemigo **no dependerá de un LLM durante la ejecución del juego**.

---

## Criterios de aceptación

El prototipo deberá cumplir con los siguientes criterios:

1. El jugador puede iniciar y controlar al sobreviviente.
2. Se puede seleccionar personaje masculino o femenino.
3. Los tres generadores pueden repararse.
4. La pieza aumenta 50 % el progreso de un generador.
5. Los tres cofres entregan sus recursos.
6. La granada aturde al enemigo.
7. La jeringa recupera la vida perdida.
8. Las trampas inmovilizan al enemigo durante 20 segundos.
9. El enemigo puede patrullar, detectar y perseguir.
10. Hay 15 agentes autónomos activos durante la prueba.
11. Los tres generadores desbloquean la puerta.
12. El jugador puede escapar y activar la victoria.
13. El jugador puede perder al llegar a cero de vida.
14. El prototipo puede probarse en los equipos disponibles.
15. Se registran pruebas de rendimiento a 30 y 60 FPS.

---

## Organización del repositorio

Se propone mantener una estructura organizada para facilitar el desarrollo:

```text
The-escape-From-Death/
│
├── README.md
├── project.godot
│
├── scenes/
│   ├── player/
│   ├── enemy/
│   ├── generators/
│   ├── chests/
│   ├── traps/
│   └── level/
│
├── scripts/
│   ├── player/
│   ├── enemy/
│   ├── generators/
│   ├── items/
│   └── agents/
│
├── assets/
│   ├── models/
│   ├── textures/
│   ├── audio/
│   └── animations/
│
└── docs/
    └── Proyecto_0/
```

---

## Estado del proyecto

**Fase actual:** Diseño preliminar.

El desarrollo del prototipo comenzará después de establecer la estructura del repositorio y validar el diseño inicial.

---
