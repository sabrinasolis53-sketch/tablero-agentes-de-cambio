# Tablero de Agentes de Cambio · Clusterciar en Acción

El tablero lee los datos de una planilla de Google. Cuando cargás una acción o participantes en la planilla, el tablero se actualiza solo.

## Qué hay en esta carpeta

- `index.html`: el tablero.
- `config.js`: acá va el ID de tu planilla de Google.
- `insignias/`: las imágenes de las insignias (ya está la de la colecta de sangre).
- `manifest.webmanifest`, `icono-192.png`, `icono-512.png`: permiten instalar el tablero en el celular como una app.
- `Planilla_Tablero_Agentes.xlsx`: la planilla modelo, ya cargada con la colecta de sangre y sus 18 participantes. Esta no hace falta subirla a GitHub.

## Paso 1: crear la planilla de Google

1. Subí `Planilla_Tablero_Agentes.xlsx` a tu Google Drive.
2. Abrila y andá a **Archivo › Guardar como Hojas de cálculo de Google**.
3. En la planilla nueva, tocá **Compartir** y en "Acceso general" elegí **Cualquier persona con el enlace**, con rol **Lector**.
4. Copiá el ID de la planilla: es la parte del link entre `/d/` y `/edit`.
5. Abrí `config.js` con el Bloc de notas y pegá el ID entre las comillas de `sheetId: ""`. Guardá.

Importante: cualquiera que tenga el link de la planilla puede ver los nombres cargados. No pongas ahí datos que no se puedan mostrar en el tablero.

## Paso 2: subir el proyecto a GitHub

1. Entrá a github.com (si no tenés cuenta, creala gratis) y tocá **New repository**. Ponele un nombre, por ejemplo `tablero-agentes-de-cambio`, y crealo.
2. En el repositorio, tocá **Add file › Upload files**.
3. Arrastrá todo el contenido de esta carpeta: `index.html`, `config.js`, `manifest.webmanifest`, los dos íconos y la carpeta `insignias`.
4. Tocá **Commit changes**.

## Paso 3: publicarlo en Vercel

1. Entrá a vercel.com e iniciá sesión con tu cuenta de GitHub.
2. Tocá **Add New › Project** y elegí el repositorio `tablero-agentes-de-cambio`.
3. En "Framework Preset" dejá **Other** y tocá **Deploy**.
4. En un minuto tenés el link, del estilo `tablero-agentes-de-cambio.vercel.app`. Ese es el link que compartís en Comunidad.

## Cómo actualizarlo

- **Nueva acción:** agregá una fila en la hoja **Acciones**. Con estado "Programada" aparece como "Próxima acción".
- **Participantes:** en la hoja **Participaciones**, una fila por persona y por acción. Si alguien participa de varias acciones, escribí su nombre igual en cada fila.
- **Insignia nueva:** subí la imagen a la carpeta `insignias` del repositorio en GitHub (Add file › Upload files) y escribí el nombre del archivo en la columna **Insignia**. Vercel vuelve a publicar el sitio solo.
- **Mostrar el ranking:** en la hoja **Config**, poné `mostrar_ranking` en **SI** para que aparezcan el podio y las posiciones.

Los cambios de la planilla pueden tardar unos minutos en verse, porque Google demora en actualizar la versión que lee el tablero.

## Instalarlo en el celular

Abrí el link del tablero en el celular y elegí **Agregar a pantalla de inicio** (en Android, desde el menú de Chrome; en iPhone, desde el botón Compartir de Safari). Queda con su ícono, como una app.
