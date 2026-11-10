# Registro de pruebas

Ejecutadas por: Sebastian y Pamela · Fecha: __/11/2026 · Navegador: ______ · Node: v26.9.0

## Etapa básica (P01–P10)

| Prueba | Acción realizada | Resultado obtenido | Estado | Corrección realizada |
|--------|------------------|--------------------|--------|----------------------|
| P01 Inicio | Abrir la app con 3 registros | Se muestra Ana Pérez y el contador dice "Testimonio 1 de 3" | Aprobado | Ninguna |
| P02 Siguiente | Clic en Siguiente desde Ana | Se muestra Luis García, "2 de 3" | Aprobado | Ninguna |
| P03 Límite superior | Llegar a María López y pulsar Siguiente | Vuelve a Ana Pérez, "1 de 3" | Aprobado | Ninguna |
| P04 Límite inferior | Desde Ana pulsar Anterior | Muestra María López, "3 de 3" | Aprobado | Ninguna |
| P05 Aleatorio | Pulsar Aleatorio 10 veces | En las 10 ocasiones cambió a un testimonio distinto del actual. Además se revisó la lógica: el salto va de 1 a total−1, por lo que `(actual + salto) % total` nunca da el mismo índice | Aprobado | Ninguna |
| P06 Un registro | Dejar un solo objeto en data.js | La tarjeta se muestra, "1 de 1"; Anterior, Siguiente y Aleatorio no cambian nada y no hay errores en consola. El botón Pausar/Reanudar no aparece (total > 1) | Aprobado | Ninguna. Se restauró data.js |
| P07 Sin registros | Usar `[]` en data.js | Aparece "No hay testimonios disponibles." sin tarjeta ni controles y sin errores | Aprobado | Ninguna. Se restauró data.js |
| P08 Ampliación de datos | Agregar 5 registros (ids 4 a 8) | Navegación completa por los 8 y contador "de 8"; las 8 fotos cargan | Aprobado | Ninguna |
| P09 Presentación | Probar 320, 768 y 1280 px; textos largos; Tab, Enter y Espacio | Sin scroll horizontal, foco visible en todos los botones, texto largo se ajusta. Capturas en `capturas/` | Aprobado | El botón Pausar/Reanudar quedaba pegado a los controles: se agregó `.controls + button { margin-top: 10px; }` |
| P10 Compilación | `npm run build` y `npm run lint` | Compila sin errores; lint con 0 warnings y 0 errores; consola del navegador sin errores de la aplicación | Aprobado | Ninguna |

### Revisión y correcciones registradas

| Origen | Hallazgo | Corrección |
|--------|----------|------------|
| Revisión del equipo | `index.html` tenía `lang="en"` y título "testimonios" aunque la interfaz está en español | Se cambió a `lang="es"` y título "Experiencias de nuestros usuarios" |
| Revisión por otra pareja | (escribir lo que digan) | (escribir lo que corrigieron) |

## Ampliación: reproducción automática (A01–A07)

| Prueba | Acción realizada | Resultado obtenido | Estado | Corrección realizada |
|--------|------------------|--------------------|--------|----------------------|
| A01 Activación | Pulsar Reanudar y esperar | El testimonio cambia aproximadamente cada 5 segundos | Aprobado | Ninguna |
| A02 Pausa | Pulsar Pausar y esperar más de 5 s | El testimonio se mantiene; el botón vuelve a decir Reanudar | Aprobado | Ninguna |
| A03 Acción manual | Con autoplay activo pulsar Anterior, Siguiente y Aleatorio | La tarjeta cambia y el autoplay queda pausado (botón dice Reanudar) | Aprobado | Ninguna |
| A04 Reanudación | Pausar y Reanudar varias veces | Los avances siguen cada 5 s, sin acelerarse | Aprobado | Ninguna |
| A05 Límites | Dejar correr el autoplay hasta el último | Tras el testimonio 8 vuelve al 1 | Aprobado | Ninguna |
| A06 Pocos datos | Con `[]` y con un solo objeto | No hay botón Pausar/Reanudar y no se crea intervalo | Aprobado | Ninguna |
| A07 Limpieza | Revisar el `return` del efecto y alternar pausa/reproducción | El efecto devuelve `() => clearInterval(intervalo)`; al alternar no se acumulan intervalos | Aprobado | Ninguna |s