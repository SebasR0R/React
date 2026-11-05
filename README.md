# Aplicación de Testimonios (React + Vite)

Práctica inicial de React · Ingeniería de Software · Unidad 3 · TECNM Celaya · AGO–DIC 2026

## Integrantes
- Sebastian (22030253@itcelaya.edu.mx)
- Pamela

## Etapa terminada
Etapa básica (navegación manual). Autoplay: pendiente.

## Instalación y ejecución
~~~bash
npm install
npm run dev        # desarrollo en http://localhost:5173
npm run build      # genera dist
npm run preview    # revisa la compilación localmente
~~~

## Estructura
~~~
src/
  components/
    Testimonial.jsx   # presenta un registro (props: item)
    Controls.jsx      # botones; comunica acciones por callbacks
  App.jsx             # conserva el índice (useState) y la navegación
  main.jsx            # monta App en #root
  data.js             # arreglo de testimonios (datos ficticios)
  styles.css          # estilos
~~~

## Decisiones principales
- App conserva el estado `index`; Testimonial solo presenta; Controls solo avisa.
- Navegación circular con el operador `%`.
- Aleatorio usa un salto entre 1 y total-1 para no repetir el actual.
- Con 0 registros se muestra un mensaje; con 1 la interfaz sigue funcionando.
- Fotos desde URLs remotas ficticias (pravatar); dependen de conexión.

## Trabajo en pareja (Driver / Navigator)
| Misión | Driver | Navigator |
|--------|--------|-----------|
| 1. Proyecto base | Sebastian | Pamela |
| 2. Datos | Pamela | Sebastian |
| 3. Testimonial | Sebastian | Pamela |
| 4. Montaje y estilos | Pamela | Sebastian |
| 5. Controles y navegación | Sebastian | Pamela |
| 6. Registro de pruebas | Pamela | Sebastian |
| 7. Ampliación de datos | Sebastian | Pamela |
| 8. README | Pamela | Sebastian |

Los cambios de rol también quedan en el historial de commits.

## Tablero Scrum
Columnas: Pendiente, En proceso, En revisión, Terminado.
Tareas: entorno, datos, tarjeta, navegación, estilos, verificación.
Enlace o captura del tablero: (pendiente)

## Revisión por otra pareja
Pareja revisora: (pendiente)
Observaciones y correcciones: (pendiente)

## Pruebas
Ver [PRUEBAS.md](PRUEBAS.md).

## Capturas
Anchos de 320, 768 y 1280 px en la carpeta `capturas/`.

## Versiones utilizadas
- Node: v26.9.0
- npm: 12.0.2
