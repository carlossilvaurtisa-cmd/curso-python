# 🐍 PyQuest — Curso de Python en 6 meses

Curso interactivo de Python con estética y mecánicas tipo Duolingo. **Un solo archivo
`index.html`** que funciona sin servidor y sin instalar nada.

## Qué contiene

- **6 módulos** (6 meses), **120 lecciones** y **623 ejercicios**
- **Python real en el navegador** con [Pyodide](https://pyodide.org) (WASM)
- **9 tipos de ejercicio**: opción múltiple, opción con código, rellenar huecos, ordenar
  líneas, emparejar, predecir la salida, cazar el bug, escribir código y proyectos
- **Gamificación**: XP, 15 niveles, corazones que se regeneran por tiempo real, racha con
  congeladores, 25 insignias y tienda con 8 artículos
- **6 jefes finales** contrarreloj y **repetición espaciada** (repaso de lo que más fallas)
- **Tutor con IA** opcional (Groq) que sabe qué lección tienes delante, revisa tu código y
  te da pistas graduadas. Sin clave, funciona un buscador local sobre la teoría del curso
- **Cuentas opcionales** con Supabase para sincronizar el progreso entre dispositivos

## Cómo usarlo

Abre `index.html` en el navegador. Listo.

Para que funcione el intérprete de Python necesitas abrirlo desde un servidor local
(Pyodide no carga por CORS con `file://`):

```bash
python -m http.server 8000
# y visita http://localhost:8000
```

El resto del curso (lecciones, teoría, XP, racha) funciona igual abriéndolo con doble clic.

## Configuración opcional

| Función | Qué necesitas |
|---|---|
| Tutor con IA | Una clave gratuita de Groq en `console.groq.com/keys`. Se pega en Ajustes y se guarda **solo en tu navegador** |
| Cuentas y sincronización | Un proyecto gratuito de Supabase. La guía paso a paso y el SQL están dentro de la propia app (Ajustes → Cuenta y sincronización) |

Ninguna de las dos es obligatoria.

## Privacidad

- El progreso se guarda en el `localStorage` del navegador.
- **La clave de Groq nunca se escribe en el archivo**: vive en el navegador de cada alumno.
- Con el tutor activo se envía a Groq solo la lección activa y lo que tú escribes.
- Con las cuentas activas, el progreso viaja cifrado por HTTPS y las reglas RLS de la base
  de datos garantizan que cada alumno solo pueda ver su propia fila.

## Licencia

Contenido didáctico original. La bibliografía citada en cada lección (*Python Crash Course*,
*Automate the Boring Stuff*, *Think Python*) pertenece a sus autores.
