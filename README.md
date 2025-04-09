![inicio](https://github.com/user-attachments/assets/92195777-28dc-403d-bd12-a6435261ed77)

# Pasteleria-Saron
# Imagen 
![Uploading image.png…]()

#Inicio "Menu"
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pastelería Rosa de Saron</title>
    <link rel="stylesheet" href="styles.css"> <!-- Conexión con el archivo CSS -->
</head>
<body>
    <!-- Header -->
    <header class="header">
        <nav class="navbar">
            <a href="#" class="logo">Pastelería Rosa de Saron</a>
            <ul class="nav-links">
                <li><a href="#">Inicio</a></li>
                <li><a href="#">Menú</a></li>
                <li><a href="#">Contactos</a></li>
            </ul>
        </nav>
    </header>

    <!-- Sección de Media-Text -->
    <section class="media-text">
        <div class="media-text-content">
            <h3 class="headline">Prueba, disfruta y saborea, los mejores pasteles de México.</h3>
            <p class="link-text"><a href="https://vibrant-itzelmarina2.wordpress.com/?page_id=31" target="_blank" rel="noreferrer noopener">Ver Catalogo ↗</a></p>
        </div>
        <figure class="media-image">
            <img src="https://vibrant-itzelmarina2.wordpress.com/wp-content/uploads/2023/11/91578766_2555969054615007_451018883734700032_n.jpg?w=1000" alt="Pastel de México" />
        </figure>
    </section>

    <!-- Sección de Información -->
    <section class="info-section">
        <h2>Descubre un mundo de sabores únicos</h2>
        <p>Sumérgete en una experiencia que nos distingue de muchas más, somos tradición, somos México.</p>
        <div class="buttons">
            <a href="https://vibrant-itzelmarina2.wordpress.com/?page_id=86" target="_blank" class="button">Más información</a>
        </div>
        <p class="footer-links">
            Condiciones de Uso / Políticas de Privacidad / Políticas de Reembolso
        </p>
        <div class="buttons">
            <a href="https://vibrant-itzelmarina2.wordpress.com/?page_id=127" target="_blank" class="button">Condiciones de Privacidad</a>
        </div>
        <p>&copy; 2023 Pastelería Rosa de Saron Derechos Reservados</p>
    </section>

    <footer>
        <p class="footer-text">Gracias por visitarnos. ¡Nos vemos pronto!</p>
    </footer>
</body>
</html>

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Arial', sans-serif;
    background-color: #f4f4f4;
    color: #333;
    line-height: 1.6;
}

.header {
    background-color: #333;
    padding: 15px 0;
}

.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

.navbar .logo {
    color: #fff;
    font-size: 1.8em;
    font-weight: bold;
    text-decoration: none;
}

.nav-links {
    list-style: none;
    display: flex;
}

.nav-links li {
    margin-left: 20px;
}

.nav-links a {
    color: #fff;
    text-decoration: none;
    font-size: 1.1em;
    padding: 10px;
}

.nav-links a:hover {
    background-color: #ffcc00;
    border-radius: 5px;
}

.media-text {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 60px 20px;
    background-color: #ffffff;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.media-text .media-image {
    flex-basis: 50%;
}

.media-text img {
    width: 100%;
    height: auto;
    border-radius: 10px;
    object-fit: cover;
}

.media-text-content {
    flex-basis: 45%;
    text-align: left;
}

.headline {
    font-size: 2.2em;
    color: #333;
    margin-bottom: 20px;
    font-weight: bold;
}

.link-text a {
    color: #007bff;
    text-decoration: none;
    font-size: 1.2em;
}

.link-text a:hover {
    text-decoration: underline;
}

.info-section {
    background-color: #ffcc00;
    color: #fff;
    padding: 60px 20px;
    text-align: center;
}

.info-section h2 {
    font-size: 2.5em;
    font-weight: bold;
    margin-bottom: 20px;
}

.info-section p {
    font-size: 1.2em;
    margin-bottom: 30px;
}

.buttons {
    margin-bottom: 30px;
}

.button {
    background-color: #007bff;
    color: #fff;
    padding: 15px 30px;
    text-decoration: none;
    font-size: 1.2em;
    border-radius: 50px;
    transition: background-color 0.3s ease, transform 0.3s ease;
}

.button:hover {
    background-color: #0056b3;
    transform: translateY(-5px);
}

.footer-links {
    font-size: 1em;
    margin-bottom: 20px;
}

.footer-links a {
    color: #fff;
    text-decoration: none;
}

.footer-links a:hover {
    text-decoration: underline;
}

footer {
    background-color: #333;
    color: #fff;
    padding: 30px;
    text-align: center;
}

.footer-text {
    font-size: 1.1em;
}
@media screen and (max-width: 768px) {
    .media-text {
        flex-direction: column;
        align-items: center;
    }

    .media-text-content {
        text-align: center;
        margin-top: 20px;
    }

    .media-text img {
        max-width: 80%;
    }

    .buttons .button {
        font-size: 1em;
        padding: 12px 20px;
    }
}
