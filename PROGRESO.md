# Rumbo a La Estrella — Videojuego de Mesa
## Progreso de Desarrollo

**Proyecto:** Videojuego educativo para la campaña "La Estrella, un municipio para jugar"
**Estrategia:** Brújula 2026 — Infancia, Gobernación de Antioquia
**Municipio:** La Estrella, Antioquia, Colombia
**Tecnología:** HTML + CSS + JavaScript puro (sin frameworks)
**Fecha inicio:** 2026-04-08

---

## Estructura del Proyecto

```
/juego/
├── index.html          — Pantalla principal del juego
├── css/style.css       — Estilos globales con paleta La Estrella
├── js/
│   ├── data.js         — Contenido: quizes, datos, casillas
│   ├── minigames.js    — Los 5 minijuegos
│   └── game.js         — Lógica principal del juego
├── assets/
│   ├── fonts/          — Menco Black/Medium/Bold + LumiosBrush
│   └── img/
│       ├── mapa.png    — Mapa limpio de La Estrella (de MAPA ESTRELLA.pdf p.1)
│       └── mascota.png — Ardilla "Sideral" (de Mascota Niños (FINAL).pdf)
└── PROGRESO.md         — Este archivo
```

---

## Assets Disponibles

| Asset | Archivo original | Estado |
|-------|-----------------|--------|
| Mapa limpio | MAPA ESTRELLA.pdf (pág 1) | ✅ Exportado como mapa.png |
| Mascota ardilla "Sideral" | Mascota Niños (FINAL).pdf | ✅ Exportado como mascota.png |
| Ilustración 340 años | Ilustración 340 años.pdf | ⬜ Referencia visual (paleta/estilo) |
| Fuente Menco Black | materialgraficobrjula2026/ | ✅ Copiada |
| Fuente Menco Medium | materialgraficobrjula2026/ | ✅ Copiada |
| Fuente Menco Bold | materialgraficobrjula2026/ | ✅ Copiada |
| Fuente LumiosBrush | materialgraficobrjula2026/ | ✅ Copiada |
| Personajes adicionales | Pendiente del cliente | ⏳ Pendiente |
| Logo La Estrella | Pendiente del cliente | ⏳ Pendiente |
| Logo Brújula 2026 | Pendiente del cliente | ⏳ Pendiente |

---

## Paleta de Colores (de Ilustración 340 años)

| Nombre | Hex | Uso |
|--------|-----|-----|
| Verde oscuro | `#2D5016` | Fondo principal, bordes |
| Verde medio | `#4A7C23` | Botones, paneles |
| Verde claro | `#8DB540` | Acentos, hover |
| Amarillo/Oro | `#F5C518` | Estrella, títulos destacados |
| Naranja | `#E87B3F` | Alertas, eventos especiales |
| Azul marino | `#1B2A4A` | Texto, bordes de personajes |
| Arena/Crema | `#F5E8C0` | Fondos de tarjetas |
| Marrón tierra | `#8B5E3C` | Detalles naturales |

---

## Mecánica del Juego

- **Jugadores:** 1 a 4 simultáneos
- **Turnos:** Lanzar dado (1–6), mover ficha, activar evento de casilla
- **Fin del juego:** Cuando el primer jugador llega a la META
- **Ganador:** Jugador con mayor puntaje total

### Tipos de Casilla (18 total)

| Tipo | Cantidad | Puntos | Descripción |
|------|----------|--------|-------------|
| Inicio | 1 | — | Punto de partida (La Raya) |
| Quiz | 4 | +100 si correcto | Pregunta de 3 opciones |
| Minijuego | 5 | 0–150 | Juego interactivo breve |
| Dato Curioso | 5 | +30 siempre | Ficha informativa del municipio |
| Estrella de Suerte | 1 | +50 automático | Bonus sin acción requerida |
| Desvío | 1 | — | Retrocede 2 casillas |
| Colaboración | 1 | +25 a todos | Momento de equipo |
| Meta | 1 | +200 bonus | Casilla final |

### Los 5 Minijuegos

1. **Atrapa la Estrella** — Haz clic en estrellas que caen (15 seg)
2. **Memoria Siderense** — Encuentra los 6 pares de íconos locales
3. **Ahorcado Siderense** — Adivina la palabra de La Estrella
4. **Simón Siderense** — Repite la secuencia de colores
5. **Palabras Revueltas** — Descifra el nombre revuelto del municipio

### Los 4 Quiz

1. ¿En qué año fue fundado La Estrella? → **1686**
2. ¿Cómo se llaman sus habitantes? → **Siderenses**
3. ¿En qué área metropolitana está? → **Valle de Aburrá**
4. ¿Cuántas puntas tiene la estrella del municipio? → **8 puntas**

### Los 5 Datos Curiosos

1. Peñas Blancas — formaciones rocosas históricas
2. El Pedrero — zona natural biodiversa
3. San Agustín - Suramérica — barrio de integración cultural
4. La Ferrería — primer centro de producción de hierro en Colombia
5. Parque Principal — corazón cívico del municipio

---

## Puntos de Interés del Mapa (Mapa pág. 2)

Identificados en el mapa con puntos de referencia:
- Ferreria (norte)
- San Jose (noroeste)
- San Agustin - Suramerica (noreste)
- Parque Principal (centro)
- El Pedrero (oeste)
- Zona Industrial (este)
- Pueblo Viejo (centro-oeste)
- Ancon (centro-este)
- Sierra Morena (sureste)
- Tablacita (este-bajo)
- Bermejela (suroeste)
- San Isidro2 (sur-este)
- Penas Blancas (sur)
- La Raya (sur-centro) ← INICIO

---

## Sistema de Personajes

- **Personaje base:** Ardilla "Sideral" (disponible, exportada)
- **Jugador 1:** Token Rojo `#E53E3E`
- **Jugador 2:** Token Azul `#3182CE`
- **Jugador 3:** Token Verde `#38A169`
- **Jugador 4:** Token Morado `#805AD5`
- **Futuros personajes:** Se integrarán como PNG transparente 400×400px mínimo

---

## Estado de Desarrollo

| Fase | Estado | Descripción |
|------|--------|-------------|
| ✅ Estructura de carpetas | Completado | /juego/ con css/, js/, assets/ |
| ✅ Assets base | Completado | mapa.png, mascota.png, fuentes |
| ✅ data.js | Completado | Todo el contenido del juego |
| ✅ index.html | Completado | Estructura completa |
| ✅ style.css | Completado | Diseño con paleta La Estrella |
| ✅ game.js | Completado | Lógica principal |
| ✅ minigames.js | Completado | 5 minijuegos funcionales |
| ✅ Primera versión jugable | Completado 2026-04-08 | |
| ✅ Dado SVG blanco con puntos negros | Completado 2026-04-08 | Animación shake + land |
| ✅ Tokens con imagen de La Ardilla | Completado 2026-04-08 | Ring de color por jugador |
| ✅ Camino con mayor contraste | Completado 2026-04-08 | Sombra oscura + línea dorada |
| ✅ 14 etiquetas POI en el mapa | Completado 2026-04-08 | Siempre visibles en el tablero |
| ✅ Escudo de La Estrella | Completado 2026-04-08 | Descargado de Wikimedia Commons |
| ✅ Renombrado: "Sideral" → "La Ardilla" | Completado 2026-04-08 | En todos los archivos |
| ✅ Responsive mejorado | Completado 2026-04-08 | Mobile, tablet portrait/landscape |
| ✅ PNG optimizado (mapa) | Completado 2026-04-08 | Reducido de 6.4MB a 2.5MB (1200px) |
| ⬜ Integración personajes adicionales | Pendiente | PNG transparente 400×400px mínimo |
| ⬜ Logo Brújula 2026 | Pendiente | No encontrado online — pedir al cliente |
| ⬜ Revisión de contenido | Pendiente | Validar quizes y datos con el cliente |
| ⬜ Ajuste fino posiciones de casillas | Pendiente | Revisar visualmente, editar CASILLAS en data.js |

---

## Notas para Continuar en Otro Chat

- El juego es 100% local, sin backend, sin recolección de datos
- Abrir `juego/index.html` directamente en el navegador para probar
- Personajes adicionales: PNG transparente, 400×400px, estilo compatible con la ardilla
- Los textos de quiz y datos curiosos están en `js/data.js` — editar ahí
- Las posiciones de las casillas están en `js/data.js` como array `CASILLAS` con coordenadas x/y en porcentaje del mapa
- Si se necesita cambiar el nombre del juego: buscar "Rumbo a La Estrella" en index.html y data.js
- Si se necesita cambiar el nombre de la ardilla: buscar "Sideral" en los archivos
