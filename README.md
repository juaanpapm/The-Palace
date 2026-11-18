# The Palace

Sitio web informativo de **The Palace Nightclub**, un proyecto de rol ambientado en Vinewood, Los Santos. La aplicación presenta la historia del negocio, su ubicación, equipo fundacional, objetivos, servicios, carta gastronómica, indumentaria y operaciones públicas.

El proyecto está construido como una aplicación web pequeña con **Node.js**, **Express** y **EJS**. Express sirve las vistas y los archivos estáticos, mientras que EJS compone una página principal a partir de varias vistas parciales.

## Características

- Historia y origen de The Palace.
- Objetivos operativos y propuesta de rol.
- Ubicación en Vinewood con mapa e imágenes del establecimiento.
- Galería interactiva con vista ampliada.
- Presentación del equipo y de los fundadores.
- Indumentaria de staff y seguridad, con filtros por categoría y género.
- Operaciones legales y acuerdos especiales.
- Carta de comidas, bebidas y alcohol con vistas emergentes.
- Servicios exclusivos, eventos privados y reuniones VIP.
- Fondo animado con dos vídeos alternados.
- Diseño adaptable para escritorio y dispositivos móviles.
- Navegación suave y efectos visuales controlados desde JavaScript.

## Tecnologías

- **Node.js**
- **Express 4**
- **EJS 3**
- **HTML5 y CSS3**
- **JavaScript** del navegador
- **Nodemon** para desarrollo
- **Google Fonts**: Rajdhani
- **Font Awesome 6** para iconos

## Requisitos

- Node.js
- npm

No es necesario configurar una base de datos ni variables obligatorias.

## Instalación

Desde la raíz del repositorio:

```bash
npm install
```

También puede utilizarse la instalación reproducible basada en el archivo de bloqueo:

```bash
npm ci
```

## Ejecución

Iniciar el servidor:

```bash
npm start
```

La aplicación estará disponible en:

```text
http://localhost:3000
```

### Desarrollo con recarga automática

```bash
npm run dev
```

El comando alternativo `npm run serve` ejecuta el servidor con Node.js.

### Puerto personalizado

El servidor usa el puerto `3000` de forma predeterminada. Puede cambiarse mediante la variable de entorno `PORT`.

En Windows PowerShell:

```powershell
$env:PORT=8080
npm start
```

En Linux/macOS:

```bash
PORT=8080 npm start
```

## Estructura del proyecto

```text
.
├── app.js                 # Configuración de Express y ruta principal
├── package.json           # Dependencias y scripts npm
├── public/
│   ├── css/
│   │   └── styles.css     # Estilos globales
│   ├── images/            # Imágenes del local, equipo y uniformes
│   ├── js/
│   │   └── main.js        # Interacciones del navegador
│   └── videos/            # Vídeos del fondo animado
└── views/
    ├── index.ejs          # Composición de la página principal
    └── partials/          # Secciones independientes de la página
```

## Funcionamiento

`app.js` crea el servidor Express, configura EJS como motor de vistas y expone `public/` como directorio de archivos estáticos. La única ruta HTTP definida es `/`, que renderiza `views/index.ejs`.

Las secciones de la página se incluyen desde `views/partials/` y se compilan por EJS al procesar la vista principal. El JavaScript de `public/js/main.js` añade comportamiento a los componentes existentes, incluidos:

- alternancia de vídeos de fondo;
- pestañas de staff y seguridad;
- filtros de género para los uniformes;
- desplazamiento suave;
- animaciones de historia y métricas;
- galería con lightbox;
- menú responsive;
- efectos del mapa;
- pestañas de operaciones.

## Pruebas

El repositorio no incluye actualmente pruebas automatizadas ni un script `test`. Las rutas y funcionalidades pueden comprobarse iniciando la aplicación y abriendo `/` en el navegador.

## Recursos externos

Además de los archivos locales del directorio `public/`, la plantilla HTML carga:

- Rajdhani desde Google Fonts;
- Font Awesome desde CDNJS;
- un icono de corona usado como favicon.

Una conexión a Internet puede ser necesaria para cargar esos recursos externos.
