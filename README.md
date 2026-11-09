# ALMA · Propuesta «Lazo Digital» — Grupo Caliche

Demo interactiva de venta para la solicitud de Ángel González (Navidad 2026):
el lazo de la sede **proyectado por dos proyectores** en lugar del montaje físico,
con simulador 3D del entorno real y análisis honesto de visibilidad de día.

## Cómo abrirla
- **Doble clic a `index.html`** (Chrome/Edge). Funciona sin servidor.
- La primera vez necesita internet solo para las tipografías (Google Fonts);
  el motor 3D va local (`lib/three.min.js`) y las fotos en `assets/`.
- Para enseñarla en pantalla grande: botón de navegador a pantalla completa.

## El guion de la presentación (5 minutos)
1. **Hero** — foto nocturna real de su lazo: «eso mismo, sin grúa ni andamios».
2. **Simulador (sección 01)** — mover el **slider de la hora**:
   - 13:00 → el lazo *no se ve* (el HUD lo dice: «No apreciable · 1 %»). Enseñarlo
     con orgullo: ninguna empresa de proyección vende lo contrario.
   - 18:10 → crepúsculo: «ya es legible». 21:00 → «pleno ×227».
   - Botones **Rotonda / Calzada / Este / Dron / Ortofoto** = sus 5 fotos de referencia.
   - Probar «2×30k láser» y «Lazo físico (comparar)» para el diálogo físico vs digital.
3. **¿De día? (02)** — curva de contraste + comparador de fotos arrastrable.
4. **Comparativa (03)** — montaje, coste recurrente, seguridad, flexibilidad.
5. **Planteamiento (04)** — tiros de 26–38 m desde calzada y glorieta, sin obstrucciones;
   opción A (permiso municipal) y B (jardín propio con mástil).
6. **Cierre** — fases y la única pega: **visita técnica** para cotas y presupuesto.

## Datos que hay que validar en la visita técnica (rellenar y ajustar en el HTML)
- [ ] Medidas del paño real del lazo (alto x ancho de cada cara de la torre).
- [ ] Reflectancia del vidrio (¿con capa selectiva? cambia el modelo de luminancias).
- [ ] Distancias fachada–eje de calzada y a la glorieta (nuestro tiro asumido: 26–38 m).
- [ ] Punto de luz más cercano (porche / planta sótano), sección y protección.
- [ ] Palmera del jardín: ¿fuera del tiro de la cara noroeste? (en el modelo, sí).
- [ ] Permiso de ocupación de vía pública si el pie va en calzada/glorieta (Ayuntamiento).
- [ ] Precios reales de alquiler/compra → sustituir el bloque «Presupuesto» (nota dorada).

## Qué es fácil cambiar
- Colores y tipografía: variables CSS al inicio de `index.html`.
- Geometría: todo el mundo 3D está en la función de construcción del script final
  (comentario `/* ---------- edificio ---------- */`), 1 unidad = 1 m.
- Luminancia del modelo: constantes `LUX`, `RHO=.12`, paño `A=60` m² en `calc()`.
- Textos de propuesta: secciones 02–06, en HTML plano.

## Carpeta
- `index.html` — la propuesta completa (autocontenida)
- `lib/three.min.js` — motor 3D (r159, local)
- `assets/` — fotos del cliente (fachada día, lazo noche, ortos 00–04)

*ALMA PROJECTS · borrador de trabajo · datos lumínicos orientativos hasta visita técnica.*
