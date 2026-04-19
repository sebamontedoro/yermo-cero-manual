# 87

**Juego de mesa de exploración, combate y supervivencia en un futuro distópico post-colapso.**

Un mundo donde las megacorporaciones implosionaron y dejaron atrás seis asentamientos humanos, miles de kilómetros de yermo peligroso y robots antiguos que siguen ejecutando sus últimas directivas en bucle infinito. Los jugadores encarnan a Barredores que exploran ese mundo junto a sus robots compañeros, buscando recursos, sobreviviendo y construyendo algo que importe.

---

## Archivos del proyecto

| Archivo | Descripción |
|---|---|
| `manual_del_jugador.html` | Manual completo del juego — lore, mecánicas, creación de personaje, sistema de dados |
| `aventura_01_senal_muerta.html` | Módulo de aventura 01 — historia, encuentros, jefe final GRÚA-7 |
| `kit_aventura_01.html` | Kit interactivo jugable en el navegador — mapa hexagonal, inventario, combate |
| `fichas.html` | Fichas imprimibles — Barredor y Ensamblado (2 páginas A4) |
| `cartas_enemigos.html` | Cartas de enemigos imprimibles — 9 mobs + 4 Primordiales (2 páginas A4) |

---

## Cómo leer / jugar

1. Abrí `manual_del_jugador.html` para conocer el mundo y las reglas
2. Leé `aventura_01_senal_muerta.html` para la primera aventura
3. Jugá `kit_aventura_01.html` directamente en el navegador — sin instalación ni dependencias

Los tres archivos están interconectados. Podés navegar entre ellos desde el sidebar y el header de cada uno.

---

## Mecánicas principales

- **Sistema de dados D&D** — D4 al D100, cada uno con su rol específico
- **Simbiosis humano-robot** — escala dinámica (0–10) que afecta tiradas, combate y supervivencia
- **Mapa hexagonal** con fog of war y eventos procedurales
- **Robots modulares** — piezas intercambiables de distintos materiales con bonuses únicos
- **4 atributos** — Código, Armazón, Terreno, Contactos
- **Modos** — Solitario, Cooperativo, Competitivo, Campaña

---

## Kit Interactivo — funcionalidades

- Mapa hexagonal procedural 12×9 con fog of war y tokens de posición
- 9 hexes de historia con eventos únicos y tiradas de dado animadas
- Pool de 14 eventos aleatorios con drops de ítems
- **Sistema de inventario** — 7 tipos de ítems (Chatarra, Cables, Paneles, Actuadores, Núcleo de Procesamiento, Batería, Kit de Reparación)
- **Mejoras de MOTE** — 3 slots modulares + upgrade a Nivel 2 con el Núcleo
- **Combate menor** — Guarda Clase I con 3 opciones: atacar, evadir, hackear
- **Combate principal** — GRÚA-7 con 3 fases, acciones del jugador y turno del enemigo
- Guardado / carga en `localStorage` + auto-guardado en cada movimiento

---

## El mundo

El **La Firma** ocurrió hace 87 años. Las cuatro megacorporaciones dominantes firmaron el Acuerdo de Singapur otorgándose soberanía industrial autónoma. En 72 horas, las redes de suministro, los bancos de datos y las fábricas automatizadas dejaron de funcionar. No por destrucción — por ausencia de gobierno.

Hoy existen **seis Nodos** de civilización conectados por caravanas que transportan mercancías sobre Bestias de Carga biomecánicas colosales:

| Nodo | Gobierno | Especialización |
|---|---|---|
| Ferrópolis | Dictadura militar | Metalurgia · Armamento |
| Calima | Mercado libre total | Comercio · Información |
| Vórtex | Tecnocracia | Software · IA |
| Confluencia | Democracia directa | Agricultura · Biomedicina |
| Sanctum Machina | Teocracia mecanicista | Robótica artesanal |
| El Umbral | Anarquía organizada | Reciclaje · Modificaciones |

Entre los Nodos: el **Yermo**. Peligroso, generoso, indiferente.

---

## Aventura 01 — Señal Muerta

**Punto de partida:** El Umbral  
**Jugadores:** 1–3 · **Duración:** 60–90 minutos · **Dificultad:** Iniciación

Tu madre, Sael Renn, desapareció en el Sector Delta-4 hace tres semanas. La señal de su robot de carga sigue activa. Lo que no sabías es que un Primordial Clase II lleva ochenta y siete años ejecutando su última directiva en esa instalación.

**Estructura:** 3 actos · 6 encuentros de historia · 1 jefe final (GRÚA-7)

**Mecánicas introducidas en esta aventura:** D20+Atributo vs CD · Extracción con D100 · Asistencia de robot · Simbiosis dinámica · Combate por fases · Desactivación técnica de Primordial

---

## Estado del proyecto

| | Estado |
|---|---|
| Manual del Jugador | ✓ Borrador v0.1 |
| Aventura 01 — Señal Muerta | ✓ Borrador v0.1 |
| Kit Interactivo Av.01 | ✓ Step 2 — funcional |
| Aventura 02 — Calima | 🔄 En desarrollo |
| Fichas de personaje y robot | 📋 Pendiente |
| Mazo de Eventos (modo solitario) | 📋 Pendiente |
| Tarjetas de módulos | 📋 Pendiente |

---

## Stack técnico

HTML · CSS · JavaScript vanilla — sin frameworks, sin dependencias, sin build step. Cada archivo es autocontenido. El kit interactivo usa `localStorage` para persistencia de partida.

---

> *"El Yermo no es tu enemigo. Es simplemente indiferente. Y entre la indiferencia y la hostilidad activa hay un espacio muy estrecho donde viven los que saben moverse."*
>
> — Mara Solt, Barredora Senior, tres brazos protésicos, ningún arrepentimiento
