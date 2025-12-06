


<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Catálogo de Equipos | AT&T ZAZIL</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&display=swap" rel="stylesheet">

<style>
/* ============================================================
    🎁 GENERAL Y FONDO
    ============================================================ */
:root {
    /* Paleta de colores temáticos */
    --color-primary: #1a1a1a;        /* Fondo oscuro de tarjeta */
    --color-secondary: #00aaff;      /* Azul neón/brillo principal */
    --color-accent: #ff004c;         /* Rojo de acento */
    --color-gold: #ffd700;           /* Dorado para precios/hover */
    --color-text-light: #f0f0f0;     /* Texto claro */
    --color-plan: #ffe14b;           /* Amarillo para plan */
    --color-precio: #00ff72;         /* Verde para precio */
}

body {
    margin: 0;
    font-family: "Poppins", sans-serif;
    color: var(--color-text-light);
    line-height: 1.6;
    min-height: 100vh; /* Asegura que el body cubra toda la altura */
    
    /* Fondo con Opacidad Reducida (más visible) */
    background-image:
        linear-gradient(rgba(0, 0, 0, 0.25), rgba(0, 0, 0, 0.25)), /* Ajustado a 0.25 */
        url("http://w.wallhaven.cc/full/eo/wallhaven-eo6zwo.jpg");

    background-repeat: no-repeat;
    background-position: center center;
    background-attachment: fixed;
    background-size: cover;
}

/* ============================================================
    ❄️ EFECTO DE NIEVE (Optimizado)
    ============================================================ */
.snowflake {
    position: fixed;
    top: -10px;
    color: var(--color-text-light);
    user-select: none;
    opacity: 0.8;
    animation: caer 8s linear infinite;
    z-index: 2000;
}
@keyframes caer {
    0%   { transform: translateY(0) rotate(0); }
    100% { transform: translateY(110vh) rotate(360deg); }
}


/* ============================================================
    🎅 ENCABEZADO
    ============================================================ */
.encabezado {
    text-align: center;
    padding: 30px 20px 0;
}

.encabezado h1 {
    font-family: "Playfair Display", serif; /* Fuente más elegante para el título */
    font-size: clamp(1.8rem, 5vw, 3rem); /* Tamaño responsivo */
    margin: 0;
    color: var(--color-text-light);
    /* Sombra de neón navideña (Rojo y Oro) */
    text-shadow: 0 0 10px var(--color-accent), 0 0 20px var(--color-gold);
}

.encabezado p {
    font-size: 1.2rem;
    font-weight: 300;
    margin-top: 5px;
}

/* ============================================================
    🔎 BUSCADOR (Sticky y Transparente)
    ============================================================ */
.buscador-container {
    position: sticky;
    top: 0;
    padding: 15px 0;
    z-index: 50;
    /* Fondo con transparencia y desenfoque (Efecto "vidrio esmerilado") */
    background: rgba(17, 17, 17, 0.85); /* Opacidad ligeramente reducida */
    border-bottom: 1px solid rgba(255, 255, 255, 0.2); /* Borde más sutil */
    backdrop-filter: blur(8px); /* Blur aumentado */
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.4); /* Sombra para resaltar */
}

#buscador {
    width: clamp(250px, 80%, 600px); /* Ancho más controlado */
    display: block;
    margin: auto;
    padding: 12px 20px;
    font-size: 1.1rem;
    border-radius: 25px; /* Bordes más redondeados */
    background: #333;
    border: 1px solid rgba(255, 255, 255, 0.3); /* Borde más sutil */
    color: var(--color-text-light);
    transition: 0.3s;
}

#buscador::placeholder {
    color: #aaa;
}

#buscador:focus {
    outline: none;
    box-shadow: 0 0 15px var(--color-secondary); /* Brillo azul */
    background: #444;
}

/* ============================================================
    📦 GRID Y CONTENEDOR
    ============================================================ */
.contenedor {
    /* El background y border-radius se mueven a la clase .main-content */
    display: grid;
    padding: 40px 20px;
    gap: 30px;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    max-width: 1400px; /* Ancho máximo para centrar el contenido */
    margin: 0 auto;
}

.main-content {
    /* Nuevo contenedor principal para el fondo oscuro */
    background: rgba(0, 0, 0, 0.65);
    border-radius: 15px;
    margin: 20px auto;
    padding: 10px;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.7);
}

/* ============================================================
    🟥 TARJETAS DE EQUIPOS (Refinadas)
    ============================================================ */
.card {
    background: var(--color-primary);
    border-radius: 16px;
    overflow: hidden;
    /* Borde temático: sutil azul con sombra navideña (Rojo) */
    border: 1px solid rgba(0, 170, 255, 0.2);
    box-shadow: 0 5px 20px rgba(0, 0, 0, 0.6), 0 0 15px rgba(255, 0, 76, 0.3);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.card:hover {
    transform: translateY(-5px); /* Movimiento sutil */
    /* Resplandor dorado elegante al pasar el ratón */
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.8), 0 0 25px var(--color-gold);
}

.card img {
    width: 100%;
    height: 250px; /* Altura ligeramente aumentada */
    object-fit: contain; /* Mejor para imágenes de producto (no se recortan) */
    background: #0d0d0d; /* Fondo muy oscuro para el área de imagen */
    cursor: pointer;
    transition: 0.2s;
}

/* Información */
.info {
    padding: 20px;
}
.info h2 {
    font-size: 1.5rem;
    margin: 0 0 8px;
    color: var(--color-secondary);
}

/* Precios y planes */
.precio {
    font-size: 1.4rem; /* Un poco más grande */
    font-weight: 700;
    margin: 8px 0;
    color: var(--color-precio); /* Verde brillante */
}
.plan {
    font-size: 1rem;
    margin-bottom: 15px;
    color: var(--color-plan); /* Amarillo sutil */
    font-weight: 600;
}

/* Listas */
ul {
    padding-left: 20px;
    margin-top: 10px;
    line-height: 1.5;
    list-style: none; /* Quitamos el estilo por defecto */
}
ul li::before {
    content: "•"; /* Opcional: un punto personalizado */
    color: var(--color-secondary); /* Color del punto */
    font-weight: bold;
    display: inline-block;
    width: 1em;
    margin-left: -1em;
}
li {
    font-size: 0.95rem;
    margin-bottom: 4px;
}

/* ============================================================
    🔥 MODAL (Capa superior)
    ============================================================ */
.modal {
    display: none;
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,0.9); /* Oscurecido para más foco */
    backdrop-filter: blur(8px);
    justify-content: center;
    align-items: center;
    z-index: 3000;
    padding: 20px; /* Padding para evitar que la imagen toque los bordes */
}

.modal-content {
    max-width: 90%;
    max-height: 90%;
    border-radius: 15px;
    background: #000; /* Fondo negro para la imagen */
    box-shadow: 0 0 30px var(--color-secondary);
    object-fit: contain; /* Asegura que la imagen se vea completa */
}

.close {
    position: absolute;
    top: 15px;
    right: 30px;
    font-size: 50px; /* Un poco más grande */
    cursor: pointer;
    color: var(--color-text-light);
    text-shadow: 0 0 15px var(--color-accent); /* Sombra roja */
    transition: 0.3s;
}
.close:hover {
    color: var(--color-accent);
}

/* ============================================================
    📱 RESPONSIVE (Móviles)
    ============================================================ */
@media (max-width: 600px) {
    .encabezado h1 {
        font-size: 2rem;
    }
    .contenedor {
        grid-template-columns: 1fr; /* Una sola columna en móvil */
        padding: 20px 10px;
    }
    .card img {
        height: 200px;
    }
}
</style>
</head>

<body>

<div id="snow"></div>

<header class="encabezado">
    <h1>CATÁLOGO EXCLUSIVO</h1>
    <p>SOLO EN AT&T ZAZIL PLAYA DEL CARMEN — ¡BUSCA EL QUE MÁS TE GUSTE!</p>
</header>

<div class="buscador-container">
    <input type="text" id="buscador" placeholder="Buscar equipo (ej: iPhone 15, Honor, G05)...">
</div>

<main class="main-content">
    <div class="contenedor" id="contenedor"></div>
</main>


<div id="myModal" class="modal">
    <span class="close">&times;</span>
    <img id="img01" class="modal-content" alt="Imagen ampliada del equipo">
</div>

<script>
// ============================================================
// 📌 LISTA DE EQUIPOS (Se mantiene igual, solo se usa 'const' para mayor seguridad)
// ============================================================
const equipos = [
/* ... TU LISTA DE EQUIPOS ORIGINAL AQUÍ ... */
{
  nombre: 'Apple iPhone 13 128GB Negro   3 PZ',
  imagen: 'https://macstoreonline.com.mx/img/sku/iphone474_FZ.jpg',
  precio: '$1,343 Mensual',
  plan: 'Platino a 30 meses con 35% de enganche.',
  caracteristicas: [
    'Pantalla 6.1" Super Retina XDR',
    'Cámara dual 12 MP (Wide + Ultra Wide)',
    'Procesador Apple A15 Bionic',
    'Batería hasta 19 horas de video',
    'Face ID',
    'iOS 17 / 18 compatible',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Apple iPhone 15 128GB Negro',
  imagen: 'https://store.storeimages.cdn-apple.com/4668/as-images.apple.com/is/iphone-15-black-select-202309?wid=940&hei=1112&fmt=png-alpha&.v=1692925511738',
  precio: '$1,253 Mensual',
  plan: 'Black a 36 meses con 35% de engache.',
  caracteristicas: [
    'Pantalla 6.1" Super Retina XDR',
    'Cámara 48 MP + 12 MP',
    'Procesador Apple A16 Bionic',
    'USB-C',
    'Batería hasta 26 horas de video',
    'Dynamic Island',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Apple iPhone 15 128GB Rosa',
  imagen: 'https://macstoreonline.com.mx/img/sku/iphone634_FZ.jpg',
  precio: '$1,253 Mensual',
  plan: 'Black a 36 meses con 35% de engache.',
  caracteristicas: [
    'Pantalla 6.1" Super Retina XDR',
    'Cámara 48 MP + 12 MP',
    'Procesador Apple A16 Bionic',
    'USB-C',
    'Batería hasta 26 horas de video',
    'Dynamic Island',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Apple iPhone 16E 128GB Negro',
  imagen: 'https://resources.sanborns.com.mx/medios-plazavip/t1/1748021533iphone16eback1png?scale=50&qlty=75',
  precio: '$1,331 Mensual',
  plan: 'Black a 24 meses con 35% de emganche',
  caracteristicas: [
    'Pantalla 6.1" Super Retina XDR',
    'Cámara dual 48 MP + 12 MP',
    'Procesador Apple A17 Fusion',
    'Batería con hasta 20h de video',
    'iOS 18',
    'Face ID mejorado',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Apple iPhone 17 Pro 256GB Azul Profundo',
  imagen: 'https://assets.encargomio.com/img/products/iPhone_17_Pro_256GB_Azul_Profundo/17582265572.png',
  precio: '$1,500 Mensual',
  plan: 'Black a 24 meses con 35% de engache',
  caracteristicas: [
    'Pantalla 6.3" ProMotion 1-120Hz',
    'Cámara triple 48 MP Pro Max',
    'Procesador Apple A19 Pro',
    'Titanium Series 3',
    'iOS 19',
    'USB-C Thunderbolt',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Apple iPhone 17 Pro 512GB Naranja Cósmico',
  imagen: 'https://www.pngall.com/wp-content/uploads/20/iPhone-17-Pro-Max-Concept-Art-PNG.png',
  precio: '$1,573 Mensual',
  plan: 'Black a 36 meses con 35% de engache',
  caracteristicas: [
    'Pantalla 6.3" ProMotion',
    'Cámara 48 MP + 48 MP + 48 MP',
    'Chip A19 Pro',
    'Carga rápida 30W',
    'iOS 19',
    'Resistencia IP68',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS' 
  ]
},

{
  nombre: 'Apple iPhone 17 Pro 512GB Plata',
  imagen: 'https://cdsassets.apple.com/live/7WUAS350/images/tech-specs/iphone-17-pro-17-pro-max-hero.png',
  precio: '$1,573 Mensual',
  plan: 'Black a 36 meses con 35% de engache',
  caracteristicas: [
    'Pantalla OLED ProMotion',
    'Chip A19 Pro',
    'Cámara Pro de 48 MP',
    'Titanio pulido',
    'Batería mejorada',
    'iOS 19',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'iPhone 16 128GB Negro',
  imagen: 'https://clevercel.mx/cdn/shop/files/16BLACK_8e3a1f31-b363-4287-96b8-bc21ce211535.png?v=1762441710&width=1214',
  precio: '$1,215',
  plan: 'BLACK A 24 MESES CON $4,725 DE ENGANCHE*',
  caracteristicas: [
    'Pantalla 6.1" OLED',
    'Cámara 48 MP',
    'Chip A18',
    'Batería de larga duración',
    'USB-C',
    'iOS 18',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'iPhone 16 Pro 128GB Titanio Negro',
  imagen: 'https://macstoreonline.com.mx/img/sku/iphone719_FZ.jpg',
  precio: '$1,310',
  plan: 'ORO A 24 MESES CON $7,251 DE ENGANCHE',
  caracteristicas: [
    'Pantalla 6.3" ProMotion',
    'Titanio Negro',
    'A18 Pro',
    'Cámara 48 MP Pro',
    'USB-C Thunderbolt',
    'iOS 18',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'iPhone 16 Pro Max 256GB Titanio Blanco',
  imagen: 'https://macstoreonline.com.mx/img/sku/iphone732_FZ.jpg',
  precio: '$1,521',
  plan: 'BLACK A 24 MESES CON $8,697 DE ENGACHE',
  caracteristicas: [
    'Pantalla 6.9" ProMotion',
    'Cámara Pro Max 48 MP',
    'Chip A18 Pro Max',
    'Titanio Blanco',
    'Batería grande',
    'iOS 18',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'iPhone 16 Pro Max 256GB Titanio Negro  3pz',
  imagen: 'https://tienda.movistar.com.mx/pub/media/catalog/product/i/p/iphone16promaxnegro.png',
  precio: '$1,521',
  plan: 'BLACK A 24 MESES CON $8,697 DE ENGACHE',
  caracteristicas: [
    'Pantalla 6.9" 120Hz',
    'Cámara triple 48 MP',
    'Titanio Black Edition',
    'A18 Pro Max',
    'USB-C',
    'iOS 18',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Google Pixel 9A 128GB Porcelain 2pz',
  imagen: 'https://revendo.ch/cdn/shop/files/google-pixel-9a-google-tensor-g4-4-nm-9a-porcelain-beige-guenstig-gebraucht-kaufen-00.png?v=1746726576',
  precio: '$1,225 Mensual',
  plan: 'Black a 24 meses con 35% de enganche.',
  caracteristicas: [
    'Pantalla 6.1" OLED',
    'Cámara 12 MP Pixel Camera',
    'Procesador Tensor G4',
    'Batería 4300 mAh',
    'Android 15',
    'IA integrada',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Google Pixel 10 128GB Obsidian 2pz',
  imagen: 'https://d1erhn8sljv386.cloudfront.net/Pf4XhY31nJJRYg6KszdmfEGsYF4=/fit-in/800x0/https://s3.amazonaws.com/lmbucket0/media/product/t-mobile-google-pixel-10-backimage-obsidian.20fc6eaa6f7954fe2990acefc6b4aeda509905e2.png',
  precio: '$1,425 Mensual',
  plan: 'Black a 24 meses con 35% de enganche',
  caracteristicas: [
    'Pantalla 6.4" OLED 120Hz',
    'Procesador Google Tensor G5',
    'Cámara 50 MP con IA avanzada',
    'Batería 5100 mAh',
    'Android 16',
    '7 años de actualizaciones',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Google Pixel 10 Pro 256GB Moonstone 2 pz',
  imagen: 'https://cdn.tmobile.com/content/dam/t-mobile/en-p/cell-phones/Google/Google-Pixel-10-Pro/Moonstone/Google-Pixel-10-Pro-Moonstone-leftimage.png',
  precio: '$1,597 Mensual',
  plan: 'Black a 24 meses con 35% de engache',
  caracteristicas: [
    'Pantalla 6.7" LTPO AMOLED 120Hz',
    'Cámara triple 50 MP Pro',
    'Tensor G5 Pro',
    'Batería 5300 mAh',
    'Carga 45W',
    'Android 16',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Google Pixel 10 Pro XL 256GB Porcelain 2pz',
  imagen: 'https://cdn.shopify.com/s/files/1/0448/8921/1040/files/unnamed_8_2.webp?v=1756067040',
  precio: '$1,649 Mensual',
  plan: 'Black a 24 meses con enganche del 35%',
  caracteristicas: [
    'Pantalla 6.9" LTPO 120Hz',
    'Cámara 50 MP ultra pro',
    'Tensor G5 Extreme',
    'Batería 5500 mAh',
    'Android 16',
    '7 años de parches',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Google Pixel 10 Pro XL 512GB Obsidian',
  imagen: 'https://www.gsmpro.com/cdn/shop/files/unnamed_11_2.webp?v=1756067040&width=1554',
  precio: '$1,740 Mensual',
  plan: 'Black a 24 meses con 35% de enganche.',
  caracteristicas: [
    'Pantalla gigante 6.9" 120Hz',
    'Cámara IA 50 MP avanzada',
    'Tensor G5 Extreme',
    'Batería 5500 mAh',
    'Carga rápida 50W',
    'Android 16',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},
{
  nombre: 'Samsung Galaxy A07 Black',
  imagen: 'https://images.samsung.com/is/image/samsung/p6pim/mx/sm-a075mzkaltm/gallery/mx-galaxy-a07-sm-a075-569913-sm-a075mzkaltm-thumb-549785654',
  precio: '—',
  plan: '—',
  caracteristicas: [
    'Pantalla 6.7" FHD+',
    'Cámara 50 MP',
    'Procesador Exynos',
    'Batería 5000 mAh',
    'Android 14',
    'Diseño elegante',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Samsung Galaxy A16 128GB Black 2pz',
  imagen: 'https://images.samsung.com/is/image/samsung/p6pim/mx/sm-a165mzkaltm/gallery/mx-galaxy-a16-sm-a165-sm-a165mzkaltm-544305569?$Q90_1248_936_F_PNG$',
  precio: '$766 Mensual',
  plan: 'AZUL 3 a 24 meses con 35% de engache.',
  caracteristicas: [
    'Pantalla 6.6" FHD+ LCD 90Hz',
    'Cámara 50 MP + 2 MP + 2 MP',
    'Procesador MediaTek Helio G80',
    'Batería 5000 mAh',
    'Android 14',
    'RAM 4GB Y 128GB',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Samsung Galaxy A17 4G Black',
  imagen: 'https://assets.kmart.com.au/transform/86f0b3ac-987a-4385-a906-577db7be6796/43675838-1?io=transform:extend,width:1100,height:1100&quality=90',
  precio: '—',
  plan: '—',
  caracteristicas: [
    'Pantalla 6.8" 90Hz',
    'Cámara 50 MP',
    'Procesador Helio G99',
    '5000 mAh',
    'OneUI 6',
    'Almacenamiento 128GB',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Samsung Galaxy A26 5G Black',
  imagen: 'https://dcdn-us.mitiendanube.com/stores/006/047/864/products/captura-de-pantalla-2025-05-16-131934-66ed2b45cf2302ec8a17474232550474-1024-1024.png',
  precio: '—',
  plan: '—',
  caracteristicas: [
    'Pantalla 6.6" FHD+ 120Hz',
    'Cámara 50 MP',
    'Procesador Exynos 1280',
    'Batería 5000 mAh',
    '5G',
    'Android 14',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Samsung Galaxy A56 5G Black   3pz',
  imagen: 'https://media.flixcar.com/webp/synd-asset/Samsung-317738145-latin-galaxy-a56-5g-sm-a566-sm-a566ezkdgto-545622606--Download-Source--zoom.png',
  precio: '—',
  plan: '—',
  caracteristicas: [
    'Pantalla AMOLED 120Hz',
    'Cámara 50 MP OIS',
    'Procesador Snapdragon 7 Gen 1',
    'Batería 5000 mAh',
    'Carga 25W',
    'RAM 8GB',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Samsung Galaxy S25 Edge Jetblack',
  imagen: 'https://images.cults3d.com/VNSCl-Ec7yCeL9zkJ3_ogO-tyAM=/516x516/filters:no_upscale()/https://fbi.cults3d.com/uploaders/37553749/illustration-file/07f5c297-0cea-4e64-9034-5d955a645995/Samsung-Galaxy-S25-Edge.jpg',
  precio: '—',
  plan: '—',
  caracteristicas: [
    'Pantalla AMOLED 6.3" 120Hz',
    'Cámara 200 MP',
    'Procesador Snapdragon 8 Gen 4',
    'Batería 4800 mAh',
    'Android 16',
    'Carga 45W',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Samsung Galaxy S25 FE Black   4pz',
  imagen: 'https://images.samsung.com/is/image/samsung/p6pim/mx/sm-s731bzkmltm/gallery/mx-galaxy-s25-fe-sm-s731-sm-s731bzkmltm-thumb-549045817',
  precio: '—',
  plan: '—',
  caracteristicas: [
    'Pantalla AMOLED 120Hz',
    'Cámara 50 MP',
    'Exynos 2500',
    'Batería 4500 mAh',
    'Carga rápida',
    'Diseño premium',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Samsung Galaxy Z Flip6 512GB Light Blue',
  imagen: 'https://images.samsung.com/is/image/samsung/assets/es/2407/mpdp/b6/galaxy-z-flip6-share-image.jpg',
  precio: '—',
  plan: '—',
  caracteristicas: [
    'Pantalla plegable 6.7" AMOLED 120Hz',
    'Pantalla externa 3.4"',
    'Procesador Snapdragon 8 Gen 3',
    'Cámara 50 MP',
    'Batería 4000 mAh',
    'Carga rápida 25W',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Xiaomi 15T BDL Sound Outdoor Black  2pz',
  imagen: 'https://xiaomistore.com.hn/wp-content/uploads/Combo_Nov_HN_Xiaomi_15T_Pro.webp',
  precio: '—',
  plan: '—',
  caracteristicas: [
    'Incluye bocina Outdoor',
    'Pantalla 6.6" AMOLED',
    'Cámara 64 MP',
    'Snapdragon 7s Gen 2',
    'Batería 5000 mAh',
    'Carga 67W',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Xiaomi 15T BDL Sound Outdoor Gold',
  imagen: 'https://cdn5.coppel.com/pm/2083563-2.jpg',
  precio: '—',
  plan: '—',
  caracteristicas: [
    'Edición Gold + Bocina',
    'Pantalla 6.6" 120Hz',
    'Cámara 64 MP',
    'Batería 5000 mAh',
    'Carga 67W',
    'MIUI 15',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Xiaomi 15T Pro BDL Redmi Padse Black',
  imagen: 'https://zom.mx/cdn/shop/files/XIAOMI15TPRO_negro_01.jpg?v=1758843181',
  precio: '—',
  plan: '—',
  caracteristicas: [
    'Incluye Redmi Pad SE',
    'Pantalla 6.7" AMOLED',
    'Cámara 108 MP',
    'Snapdragon 8 Gen 3',
    'Carga 120W',
    'RAM 12GB',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Xiaomi Redmi 14C 128GB Black',
  imagen: 'https://i02.appmifile.com/731_item_mx/16/10/2024/5d584c744ba18c57182e94f2df77704f.png',
  precio: '—',
  plan: '—',
  caracteristicas: [
    'Pantalla 6.71" HD+',
    'Cámara 13 MP',
    'Batería 5000 mAh',
    'Procesador Helio G36',
    'Android 14',
    'Dual SIM',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Xiaomi Redmi 14C 128GB Blue  2pz',
  imagen: 'https://imports77.com/cdn/shop/files/CelularRedmi14C4_128Gb-AzulAstral.png?v=1736449834',
  precio: '—',
  plan: '—',
  caracteristicas: [
    'Pantalla grande 6.7" HD+',
    'Procesador Helio G36',
    '5000 mAh',
    'Cámara 13 MP',
    'MIUI 15',
    'Almacenamiento 128GB',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Xiaomi Redmi 15 Black',
  imagen: 'https://tienda.movistar.com.mx/pub/media/catalog/product/r/e/redmi15_dual.png',
  precio: '—',
  plan: '—',
  caracteristicas: [
    'Pantalla FHD+ 6.7"',
    'Cámara 50 MP',
    'Procesador Helio G99',
    'Batería 5000 mAh',
    'Carga 33W',
    'MIUI 15',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Xiaomi Redmi 15 128GB BLACK  2 pz',
  imagen: 'https://tienda.movistar.com.mx/pub/media/catalog/product/r/e/redmi15_dual.png',
  precio: '—',
  plan: '—',
  caracteristicas: [
    'Pantalla 6.9" FHD+ (144 Hz)',
    'Cámara trasera 50 MP',
    'Cámara frontal 8 MP',
    'Batería 7000 mAh',
    'Procesador Snapdragon 6s Gen 3',
    'Android 15 / HyperOS 2',
    'Dual SIM',
    'Carga rápida 33W (carga inversa 18W)',
    'Resistencia polvo/agua IP64',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Xiaomi Redmi 15C 128GB blue 3 pz',
  imagen: 'https://i02.appmifile.com/755_item_mx/28/08/2025/47aad66ef05f71a0d6db2817eb746bbe.png',
  precio: '—',
  plan: '—',
  caracteristicas: [
    'Pantalla 6.9" HD+ (120 Hz)',
    'Cámara trasera 50 MP',
    'Cámara frontal 8 MP',
    'Batería 6000 mAh',
    'Procesador MediaTek Helio G81-Ultra',
    'Android 15 / HyperOS 2',
    'Dual SIM + microSD',
    'Carga rápida 33W',
    'Resistencia polvo/agua IP64',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Xiaomi Redmi A5 Azul Océano',
  imagen: 'https://www.maxmovil.com/media/catalog/product/cache/2c055c968235f5bf43b443aee4bb62c6/x/i/xiaomi_redmi_a5_azul_5__1.png',
  precio: '—',
  plan: '—',
  caracteristicas: [
    'Pantalla 6.52" HD+',
    'Cámara 13 MP',
    'Batería 5000 mAh',
    'Procesador Helio A22',
    'Android 13 Go',
    'RAM 3GB',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Xiaomi 17 Pro Max 256GB',
  imagen: 'https://macstoreonline.com.mx/img/sku/iphone780_FZ.jpg',
  precio: '—',
  plan: '—',
  caracteristicas: [
    'Pantalla LTPO AMOLED 6.9" (≈ 2K, 2608×1200) con hasta 120 Hz, HDR10+, Dolby Vision, brillo hasta ~3,500 nits',
    'Pantalla trasera secundaria AMOLED 2.9" (resolución ≈ 976×596)',
    'Procesador Qualcomm Snapdragon 8 Elite Gen 5',
    'Memoria RAM 12 GB / 16 GB + almacenamiento 256 GB (UFS 4.1)',
    'Triple cámara trasera 50 MP + 50 MP (ultra gran angular) + 50 MP (telefoto periscópico con zoom óptico 5×, lente Leica, OIS, video hasta 8K HDR / 4K HDR)',
    'Cámara frontal 50 MP para selfies',
    'Batería 7,500 mAh con carga rápida 100 W, carga inalámbrica 50 W y carga inversa',
    'Altavoces estéreo con Dolby Atmos',
    'Certificación IP68 (resistente a agua y polvo)',
    'Conectividad 5G / Wi-Fi / Bluetooth / NFC + UWB',
    'Sistema Android 16 con HyperOS 3',
    'Dual SIM'
  ]
},
{
  nombre: 'Honor 400 BDL Headphone Black  3 pz',
  imagen: 'https://tienda.movistar.com.mx/media/catalog/product/cache/087d8656b93b378449aad7de37c3d04e/b/u/bundle.png',
  precio: '$1,175 Mensual',
  plan: 'Black a 24 meses con 35% de engache.',
  caracteristicas: [
    'Audífonos inalámbricos',
    'Cancelación de ruido',
    'Conectividad Bluetooth 5.3',
    'Autonomía 30 horas',
    'Carga USB-C',
    'Micrófono dual',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Honor 400 BDL Headphone Gold  3pz',
  imagen: 'https://www.dxomark.com/wp-content/uploads/medias/post-184771/Honor-400-Featured-image.png',
  precio: '$1,175 Mensual',
  plan: 'Black a 24 meses con 35% de engache.',
  caracteristicas: [
    'Edición dorada premium',
    'Cancelación activa',
    'Bluetooth 5.3',
    'Autonomía 30h',
    'Diseño cómodo',
    'Carga rápida',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Honor Magic6 Lite Orange',
  imagen: 'https://www.honor.com/content/dam/honor/es/shop/1560-1170/m6l-1212.png',
  precio: '$720 Mensual',
  plan: 'Azul 2 a 36 meses con 35% de engache.',
  caracteristicas: [
    'Pantalla curva 6.78" AMOLED',
    'Cámara 108 MP',
    'Procesador Snapdragon 6 Gen 1',
    'Batería 5300 mAh',
    'Carga 35W',
    'RAM 8GB',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Honor Magic6 Lite Silver',
  imagen: 'https://www.honor.com/content/dam/honor/mx/products/smartphone/honor-magic6-lite/imgs/sec4-new/sec4-phone-bg-mb.png',
  precio: '$720 Mensual',
  plan: 'Azul 2 a 36 meses con 35% de engache.',
  caracteristicas: [
    'Pantalla AMOLED 120Hz',
    'Cámara 108 MP',
    'Batería 5300 mAh',
    'Snapdragon 6 Gen 1',
    'MagicOS 8',
    'RAM 8GB',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Honor Magic7 Lite BDL Headphones 5G Jcyan  2pz',
  imagen: 'https://tiendahonor.cr/wp-content/uploads/2025/01/MKT_Bruce_Identity-Pictures_%E9%9D%92%E8%89%B2Cyan_%E7%BA%AF%E8%83%8CBack_RGB_PNG_20240814-2.png',
  precio: '$970 Mensual',
  plan: 'Plata a 30 meses con 35% de engache.',
  caracteristicas: [
    'Pantalla AMOLED 120Hz',
    'Cámara 108 MP',
    'Snapdragon 7s Gen 2',
    'Batería 5100 mAh',
    '5G',
    'Incluye audífonos',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Honor X5C Plus Meteor Silver',
  imagen: 'https://texnohome.az/image/cache/catalog/21.10.2025/cdn-cgi-39-1200x630.png',
  precio: '$495 Mensual',
  plan: 'Azul 1 a 24 meses SIN ENGANCHE.',
  caracteristicas: [
    'Pantalla 6.56" HD+',
    'Cámara 50 MP',
    'Procesador Octa-Core',
    'Batería 5000 mAh',
    'Android 14',
    'Almacenamiento 128GB',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Honor X5C Plus Ocean Cyan',
  imagen: 'https://catalog.sixty60.co.za/v2/files/68e90439ed336b2f66207bbe?width=1440&height=1440',
  precio: '$495 Mensual',
  plan: 'Azul 1 a 24 meses SIN ENGANCHE.',
  caracteristicas: [
    'Pantalla 6.56" HD+',
    'Cámara 50 MP',
    'Batería 5000 mAh',
    'Android 14',
    'Procesador Octa-Core',
    'Diseño resistente',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Honor X6C Cyan  4pz',
  imagen: 'https://www.honor.com/content/dam/honor/common/product-list/product-series/honor-x6c/honor-x6c-g-list.png',
  precio: '$601 Mensual',
  plan: 'Azul 2 con 35% de engache.',
  caracteristicas: [
    'Pantalla 6.56" IPS',
    'Cámara 50 MP',
    'Procesador MediaTek G36',
    'Batería 5200 mAh',
    'RAM 4GB',
    'Android 14',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Honor X7D Desert Gold',
  imagen: 'https://www.honor.com/content/dam/honor/common/product-list/product-series/honor-x7d/honor-x7d-gold-list.png',
  precio: '$770 Mensual',
  plan: 'Azul 3 a 24 meses con 35% de engache.',
  caracteristicas: [
    'Pantalla 6.74" 90Hz',
    'Cámara 50 MP',
    'Procesador Snapdragon 480+',
    'Batería 5000 mAh',
    'Android 14',
    'Carga rápida 22W',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Honor X7D Velvet Black  2pz',
  imagen: 'https://miamicenters.com/wp-content/uploads/2025/09/x7dd-blackk.png',
  precio: '$770 Mensual',
  plan: 'Azul 3 a 24 meses con 35% de engache.',
  caracteristicas: [
    'Pantalla 6.74" HD+',
    'Cámara 50 MP',
    '5G',
    'Batería 5000 mAh',
    'Android 14',
    'Diseño elegante',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Honor X8C BDL Earbuds X7i Morado Nube',
  imagen: 'https://www.honor.com/content/dam/honor/cl/product-list/smartphone/honor-x8c/honor-x8c-p.png',
  precio: '$948 Mensual',
  plan: 'Plata a 24 meses con 35% de engache.',
  caracteristicas: [
    'Incluye audífonos X7i',
    'Pantalla 6.8" FHD+',
    'Cámara 108 MP',
    'Batería 5000 mAh',
    'Carga 30W',
    'RAM 8GB',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},
{
  nombre: 'Oppo A40 4G Lila  2pz',
  imagen: 'https://tienda.movistar.com.mx/media/catalog/product/cache/dfb1fdb7a1cc7d82dc65a70ab5260406/t/m/tmlmxopopa40li00.png',
  precio: '$500 Mensual',
  plan: 'Azul 1 a 24 meses con 35% de engache.',
  caracteristicas: [
    'Pantalla 6.56" LCD',
    'Cámara 50 MP',
    'Procesador Helio G35',
    'Batería 5000 mAh',
    'ColorOS 14',
    'RAM 4GB',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Oppo Find X8 Pro 5G Negro Grafito',
  imagen: 'https://miphone.com.mx/wp-content/uploads/2024/10/Captura-de-pantalla-2024-10-28-a-las-9.50.54.png',
  precio: '$1,545 Mensual',
  plan: 'Platino a 30 meses con el 35% de enganche.',
  caracteristicas: [
    'Pantalla 6.82" AMOLED 120Hz',
    'Cámara 50 MP Hasselblad',
    'Snapdragon 8 Gen 4',
    'Batería 5400 mAh',
    'Carga 100W',
    'RAM 12GB',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Oppo Reno14 BDL Headphones Verde',
  imagen: 'https://resources.sanborns.com.mx/imagenes-sanborns-ii/1200/2005611050633.jpg?scale=500&qlty=75',
  precio: '$1,255 Mensual',
  plan: 'Black a 24 meses con el 35% de engache.',
  caracteristicas: [
    'Pantalla AMOLED 120Hz',
    'Cámara 64 MP',
    '5G',
    'Snapdragon 7 Gen 2',
    '5000 mAh',
    'Audífonos incluidos',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},
{
  nombre: 'Motorola Moto G05 Verde  2pz',
  imagen: 'https://mxmoto.vtexassets.com/arquivos/ids/170403/MotoG05-VerdeProfundo-Hero.png?v=638681517847370000',
  precio: '$497 Mensual',
  plan: 'Azul 1 a 24 Meses SIN ENGACHE',
  caracteristicas: [
    'Pantalla 6.5" HD+',
    'Cámara 16 MP',
    'Procesador Unisoc T606',
    'Batería 5000 mAh',
    'RAM 4GB',
    'Android 14',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Motorola Moto G15 Gris',
  imagen: 'https://cdn5.coppel.com/mkp/74625726-1.jpg',
  precio: '$515 Mensual',
  plan: 'Azul 1 a 24 meses con 35% de enganche',
  caracteristicas: [
    'Pantalla 6.7" 120Hz',
    'Cámara 50 MP OIS',
    'Snapdragon 6 Gen 1',
    'Batería 5000 mAh',
    'Carga 30W',
    'Android 15',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Motorola Moto G15 Verde',
  imagen: 'https://mxmoto.vtexassets.com/arquivos/ids/170371/MotoG15-Verde-Hero.png?v=638680034078200000',
  precio: '$515 Mensual',
  plan: 'Azul 1 a 24 meses con 35% de enganche',
  caracteristicas: [
    'Pantalla 6.7" FHD+',
    'Cámara 50 MP',
    '5G',
    'Snapdragon 6 Gen 1',
    '5000 mAh',
    'Android 15',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Motorola Moto G24 Lavanda',
  imagen: 'https://tienda.movistar.com.mx/media/catalog/product/cache/087d8656b93b378449aad7de37c3d04e/m/o/moto_g24_lavanda_both.png',
  precio: '$500 Mensual',
  plan: 'Azul 1 a 24 meses SIN ENGACHE',
  caracteristicas: [
    'Pantalla 6.6" HD+ 90Hz',
    'Procesador Helio G85',
    'Cámara 50 MP',
    'Batería 5000 mAh',
    'Android 14',
    'RAM 4GB',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Motorola Moto G56 5G Azul  2pz',
  imagen: 'https://mxmoto.vtexassets.com/arquivos/ids/171753-800-auto?v=638832717390770000&width=800&height=auto&aspect=true',
  precio: '$769 Mensual',
  plan: 'AZUL 3 a 24 meses con 35% de engache',
  caracteristicas: [
    'Pantalla 6.7" 120Hz',
    'Cámara 50 MP',
    'Procesador Snapdragon 4 Gen 2',
    'Batería 5000 mAh',
    '5G',
    'Android 14',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

{
  nombre: 'Motorola Moto G56 5G Gris  2pz',
  imagen: 'https://tienda.movistar.com.mx/media/catalog/product/cache/087d8656b93b378449aad7de37c3d04e/m/o/motog56_gris_dual.png',
  precio: '$769 Mensual',
  plan: 'AZUL 3 a 24 meses con 35% de engache',
  caracteristicas: [
    'Pantalla FHD+ 120Hz',
    'Procesador Snapdragon 4 Gen 2',
    'Cámara 50 MP',
    '5000 mAh',
    'USB-C',
    'Android 14',
    'SEGURO DE PROTECCIÓN',
    'CONTROL DE DATOS'
  ]
},

];



// ============================================================
// 📌 FUNCIÓN PARA MOSTRAR EQUIPOS (USANDO CLONACIÓN DE PLANTILLA - Más eficiente)
// ============================================================
const contenedor = document.getElementById("contenedor");
const placeholderImg = 'https://via.placeholder.com/400x250?text=Sin+Imagen';

function crearCardHTML(equipo) {
    const imagenSrc = equipo.imagen || placeholderImg;
    const listaHTML = equipo.caracteristicas.map(c => `<li>${c}</li>`).join("");

    return `
        <div class="card">
            <img src="${imagenSrc}" alt="${equipo.nombre}" class="imagen-equipo" loading="lazy">
            <div class="info">
                <h2>${equipo.nombre}</h2>
                <div class="precio">${equipo.precio}</div>
                <div class="plan">${equipo.plan}</div>
                <ul>${listaHTML}</ul>
            </div>
        </div>
    `;
}

function mostrarEquipos(lista) {
    // Usamos map y join para construir el HTML de una vez (más rápido que appendChild en un bucle)
    contenedor.innerHTML = lista.map(crearCardHTML).join("");
}

// ============================================================
// 🔍 BUSCADOR (Usa desestructuración moderna)
// ============================================================
document.getElementById("buscador").addEventListener("input", function (e) {
    // Usamos e.target.value en lugar de this.value
    const texto = e.target.value.toLowerCase();
    
    // Filtramos por nombre o características para una búsqueda más robusta
    const filtrados = equipos.filter(e => {
        const nombreYMarca = e.nombre.toLowerCase();
        const caracteristicas = e.caracteristicas.join(" ").toLowerCase();
        
        return nombreYMarca.includes(texto) || caracteristicas.includes(texto);
    });
    mostrarEquipos(filtrados);
});

// Mostrar todos al inicio
mostrarEquipos(equipos);


// ============================================================
// 🖼️ MODAL DE IMÁGENES (Delegación de eventos centralizada)
// ============================================================
const modal = document.getElementById("myModal");
const modalImg = document.getElementById("img01");
const closeModal = document.querySelector(".close");

// Abrir Modal (Delegación en el contenedor principal)
contenedor.addEventListener("click", e => {
    // Usamos el método .closest() para manejar mejor los clicks
    const img = e.target.closest(".imagen-equipo");
    if (img) {
        modal.style.display = "flex";
        modalImg.src = img.src;
        modalImg.alt = img.alt;
    }
});

// Cerrar Modal
closeModal.addEventListener("click", () => modal.style.display = "none");

// Cerrar al hacer click fuera de la imagen
modal.addEventListener("click", e => { 
    if (e.target === modal) {
        modal.style.display = "none";
    }
});


// ============================================================
// ❄️ GENERADOR DE NIEVE (Ligeramente optimizado)
// ============================================================
function crearNieve() {
    const snowContainer = document.getElementById("snow");
    const numCopos = 30; // Aumentado a 30 para más efecto
    
    for (let i = 0; i < numCopos; i++) {
        const copo = document.createElement("div");
        copo.className = "snowflake";
        copo.textContent = "•"; // Símbolo más sutil que ❄ (para elegancia)
        copo.style.left = Math.random() * 100 + "vw";
        copo.style.animationDelay = Math.random() * 10 + "s"; // Delay más largo para distribución
        copo.style.animationDuration = (8 + Math.random() * 7) + "s"; // Duración variable
        copo.style.fontSize = (12 + Math.random() * 16) + "px"; // Tamaño sutil
        snowContainer.appendChild(copo);
    }
}
crearNieve();
</script>

</body>
</html>
