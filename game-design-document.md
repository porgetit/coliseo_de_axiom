# 🎮 DOCUMENTO DE DISEÑO DEL VIDEOJUEGO
## Coliseo de Axiom

### 🎯 1. TÍTULO DEL JUEGO
**Coliseo de Axiom: Prueba de Supervivencia**

### 📝 2. RESUMEN DEL JUEGO Y OBJETIVOS DEL JUGADOR

#### Sinopsis
*Coliseo de Axiom* es un roguelike de combate cuerpo a cuerpo con vista superior, donde los jugadores controlan a un estudiante universitario que, tras quedarse dormido desarrollando un videojuego para su proyecto final, despierta misteriosamente en un coliseo gótico-futurista. Armado únicamente con una espada básica, deberá enfrentarse a oleadas de enemigos que aumentan progresivamente en dificultad mientras el tiempo transcurre.

#### Tipo de juego
- Roguelike de combate
- Vista superior
- Partidas rápidas (aproximadamente 10-15 minutos)
- Estilo visual: Pixel art con estética gótico-futurista

#### Objetivos del jugador
- Sobrevivir a oleadas crecientes de enemigos
- Derrotar al Custodio, un poderoso enemigo final que aparece después de aproximadamente 10 minutos que además es casi invencible
- Mejorar sus habilidades de combate a medida que transcurre el tiempo

### 🔁 3. ESTRUCTURA DE NAVEGACIÓN DEL JUEGO

#### 3.1 Diagrama de navegación
```
[Intro/Pantalla de Título]
↓
[Menú Principal]
├── [Jugar]
│    └── [Arena de Combate]
│         └── [Fin de Partida/Tiempo]
├── [Mejores Tiempos]
├── [Ayuda/Controles]
├── [Créditos]
└── [Salir]
```

#### 3.2 Descripción de secciones
- **Intro**: Pantalla con el logo del juego y una breve animación que establece el tono gótico-futurista.
- **Menú Principal**: Interfaz minimalista con las opciones principales del juego.
- **Jugar**:
  - **Arena de Combate**: El coliseo donde transcurre la acción
  - **Fin de Partida/Tiempo**: Muestra estadísticas de la partida y permite guardar el tiempo
- **Mejores Puntuaciones**: Tabla con los 10 mejores resultados (Tiempo de supervivencia)
- **Ayuda/Controles**: Instrucciones básicas y mapeo de teclas
- **Créditos**: Detalles de los desarrolladores y recursos utilizados
- **Salir**: Opción para cerrar el juego

### 📖 4. HISTORIA O NARRATIVA

#### Trasfondo
Un estudiante universitario cae rendido de cansancio mientras desarrolla un videojuego para su proyecto final de computación gráfica. Al despertar, se encuentra en un extraño coliseo rodeado de niebla, con una espada en sus manos. Una voz resuena en el lugar:

*"Bienvenido, mortal. Has sido elegido para participar en la Prueba de Axiom. Demuestra tu valía sobreviviendo a las criaturas que invocaré. Si logras derrotar al Custodio, serás liberado. Si fracasas, tu esencia alimentará el Coliseo por toda la eternidad. El tiempo es tu aliado y tu enemigo; mientras más resistas, más fuerte te volverás, pero también enfrentarás desafíos mayores. ¡Que comience la prueba!"*

#### Personajes
- **Protagonista**: Un estudiante universitario normal que debe adaptarse rápidamente a las circunstancias para sobrevivir.
- **La Voz**: Entidad misteriosa que controla el coliseo y establece las reglas.
- **El Custodio**: Guardián final del coliseo, una imponente figura con armadura que mezcla elementos góticos y tecnológicos avanzados.

#### Desenlace
Al derrotar al Custodio, el estudiante es devuelto a su realidad, despertándose frente a su computadora con su proyecto completado misteriosamente.

### ⚙️ 5. MECÁNICAS DEL JUEGO

#### Sistema de combate
- Combate directo cuerpo a cuerpo con espada
- Ataque básico: golpe rápido de corto alcance
- Ataque cargado: golpe más lento pero potente
- Velocidad base de movimiento: 120% respecto a los enemigos estándar
- Movimiento fluido en 8 direcciones
- Capacidad de retroceder mientras ataca


#### Sistema de oleadas
- Las oleadas duran aproximadamente 2 minutos cada una
- No hay anuncios explícitos de cambio de oleada
- La dificultad aumenta progresivamente con cada oleada
- Tras 10 minutos (5 oleadas), aparece el Custodio
- No se requiere eliminar a todos los enemigos para avanzar a la siguiente oleada

#### Progresión del personaje basada en tiempo
- Regeneración de vida constante: +1% de vida máxima cada 10 segundos
- Daño: +0.005% por segundo transcurrido
- Poder mágico: +0.005% por segundo transcurrido
- La velocidad de movimiento permanece constante durante toda la partida

#### Enemigos (por orden de aparición)
1. **Reclutas**: Enemigos básicos, movimiento y ataques lentos
2. **Soldados**: Más rápidos que los reclutas, ataques más coordinados
3. **Caballeros**: Resistentes, ataques potentes pero predecibles
4. **Campeones**: Rápidos y fuertes, combinan ataques y defensas
5. **Custodio**: Jefe final con patrones de ataque complejos y alta resistencia

#### Condiciones de victoria/derrota
- **Victoria**: Derrotar al Custodio
- **Derrota**: Perder todos los puntos de vida

### 🎮 6. CONTROLES DEL JUEGO

| Tecla | Función |
|-------|---------|
| W/↑ | Movimiento hacia arriba |
| A/← | Movimiento hacia la izquierda |
| S/↓ | Movimiento hacia abajo |
| D/→ | Movimiento hacia la derecha |
| Ci | Ataque básico |
| Cd | Ataque cargado (mantener) |
| ESC | Pausar juego/Menú de opciones |

### 🗺️ 7. DISEÑO DE NIVELES

#### Arena de combate
- Coliseo rectangular con un tamaño de 64 casillas de lado
- Área central despejada para el combate principal
- Elementos decorativos en los bordes (antorchas, estatuas)
- Trampas que aparecen aleatoriamente
- Zonas de sombra que dificultan la visibilidad de los enemigos


#### Progresión de dificultad (Sujeto a cambios)
1. **Minutos 0-2**: 2-3 enemigos básicos simultáneamente
2. **Minutos 2-4**: 3-4 enemigos básicos y soldados
3. **Minutos 4-6**: 4-5 enemigos incluyendo caballeros
4. **Minutos 6-8**: 3-4 enemigos de nivel medio-alto
5. **Minutos 8-10**: 2-3 campeones con habilidades especiales
6. **Pasados 10 minutos**: Aparición del Custodio

### 🎨 8. ELEMENTOS VISUALES

#### Estilo gráfico
- Pixel art de 16x16 o 32x32 píxeles por casilla
- Paleta de colores limitada con tonos oscuros.
- Estética gótico-futurista con elementos steampunk

#### Recursos gráficos
- **Personaje principal**: Estudiante con espada
- **Enemigos**: 
  - Reclutas: Figuras humanas simples con armas básicas
  - Soldados: Armaduras medias con detalles metálicos
  - Caballeros: Armaduras pesadas con símbolos arcanos
  - Campeones: Diseños únicos con elementos tecnológicos
  - Custodio: Figura imponente con armadura tecnológica avanzada
- **Arena**: Suelo de piedra
- **Efectos visuales**: Chispas de metal, destellos de energía, rastros de movimiento

### 🔊 9. SONIDO Y MÚSICA

#### Música de fondo
- **Menú principal**: Melodía ambiental y misteriosa
- **Combate normal**: Ritmo intenso con percusión metálica
- **Combate con Custodio**: Versión épica y más compleja de la música de combate
- **Victoria/Derrota**: Variaciones temáticas según el resultado

#### Efectos de sonido
- **Interfaz**: Clicks, selecciones, confirmaciones
- **Movimiento**: Pasos sobre piedra (sujeto a disponibilidad)
- **Combate**:
  - Balanceo de espada
  - Impacto en enemigo
- **Enemigos**:
  - Ataque
  - Daño recibido
  - Muerte
- **Ambiente**:
  - Viento

#### Fuentes de audio
- Se utilizarán recursos de dominio público y librerías libres como:
  - Freesound.org
  - OpenGameArt.org
  - Sonidos originales creados por el equipo

### 🧭 10. INTERFAZ DE USUARIO (UI)

#### Pantallas principales
- **Pantalla de título**: Logo, "Presiona cualquier tecla"
- **Menú principal**: Opciones de navegación, fondo del coliseo
- **Arena de combate**: Interfaz minimalista durante la acción
- **Pausa**: Opciones para continuar, reiniciar o salir
- **Fin de partida**: Resumen de estadísticas y tiempo
- **Tabla de puntuaciones**: Lista de mejores resultados
- **Ayuda/Controles**: Controles
- **Créditos**: Lista de desarrolladores y recursos

#### HUD durante el juego (Ubicaciones sujetas a cambio)
- **Barra de salud**: Esquina superior izquierda
- **Barra de magia**: Esquina superior izquierda
- **Temporizador**: Esquina superior izquierda

### 🧩 11. ARQUITECTURA DEL CÓDIGO (Sujeto a cambios)

#### Estructura de archivos
```
/ColiseoDeAxiom
  /src
    /core
      game.py        # Clase principal del juego
      entity.py      # Clase base para entidades
      player.py      # Clase del jugador
      enemy.py       # Clase base de enemigos
      collision.py   # Sistema de colisiones
      timer.py       # Control de tiempo y eventos
    /ui
      menu.py        # Sistemas de menús
      hud.py         # Interfaz durante el juego
      scores.py      # Manejo de puntuaciones
    /screens
      title.py       # Pantalla de título
      game.py        # Pantalla principal de juego
      pause.py       # Pantalla de pausa
      end.py         # Pantalla de fin de juego
    /enemies
      recruit.py     # Enemigo nivel 1
      soldier.py     # Enemigo nivel 2
      knight.py      # Enemigo nivel 3
      champion.py    # Enemigo nivel 4
      custodian.py   # Jefe final
    /utils
      spritesheet.py # Manejo de sprites
      sound.py       # Sistema de audio
      particles.py   # Sistema de partículas
    main.py          # Punto de entrada
  /assets
    /graphics
      /player
      /enemies
      /environment
      /ui
    /sounds
      /music
      /sfx
    /fonts
  /data
    scores.json      # Almacenamiento de puntuaciones
    settings.json    # Configuraciones de usuario
  README.md
  requirements.txt
```

### 👥 13. CRÉDITOS Y REFERENCIAS

#### Equipo de desarrollo
- [Kevin Esguerra Cardona] - Programación principal
- [Kevin Esguerra Cardona] - Diseño de juego
- [Juan Pablo Sánchez Zapata] - Arte y animaciones
- [Juan Pablo Sánchez Zapata] - Sonido y música

#### Recursos externos
- **Bibliotecas**:
  - Pygame (v2.1.2) - https://www.pygame.org
  - NumPy (v1.22.0) - https://numpy.org
  
- **Gráficos**:
  - Sprites base de OpenGameArt.org (con modificaciones)
  - Texturas adicionales creadas por [Nombre del Artista]
  
- **Audio**:
  - Efectos de sonido de Freesound.org
  - Música por [Compositor] bajo licencia CC-BY
  
- **Documentación consultada**:
  - "Python Game Programming By Example" - Alejandro Rodas
  - Tutoriales de Pygame de Clear Code
  - Documentación oficial de Pygame

### ✈️ 14. INSPIRACIÓN

  - https://store.steampowered.com/app/1966900/20_Minutes_Till_Dawn/
  - https://store.steampowered.com/app/1581950/Buriedbornes2__Dungeon_RPG/