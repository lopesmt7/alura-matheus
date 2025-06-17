<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Minha Aventura</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="tela-inicial">
        <h1>Bem-vindo à Aventura!</h1>
        <p>Prepare-se para uma jornada épica. O que você encontrará no seu caminho?</p>
        <button id="iniciarBtn">Iniciar Aventura</button>
    </div>

    <script src="script.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Site Interativo</title>
    <link rel="stylesheet" href="estilos.css">
</head>
<body>

    <header>
        <h1>Bem-vindo ao Meu Site</h1>
        <nav>
            <ul>
                <li><a href="index.html" class="nav-link">Home</a></li>
                <li><a href="sobre.html" class="nav-link">Sobre</a></li>
            </ul>
        </nav>
    </header>

    <section class="conteudo" id="conteudo">
        <h2>Conteúdo Principal</h2>
        <p>Este é o conteúdo inicial da página. Explore as seções para aprender mais!</p>
    </section>

    <footer>
        <p>&copy; 2025 Meu Site</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sobre - Meu Site</title>
    <link rel="stylesheet" href="estilos.css">
</head>
<body>

    <header>
        <h1>Sobre Este Site</h1>
        <nav>
            <ul>
                <li><a href="index.html" class="nav-link">Home</a></li>
                <li><a href="sobre.html" class="nav-link">Sobre</a></li>
            </ul>
        </nav>
    </header>

    <section class="conteudo" id="conteudo-sobre">
        <h2>Quem Somos</h2>
        <p>Este site foi criado para demonstrar navegação interativa e animações!</p>
    </section>

    <footer>
        <p>&copy; 2025 Meu Site</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
/* Resetando margens e paddings */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Corpo do site */
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    color: #333;
}

/* Cabeçalho */
header {
    background-color: #3498db;
    padding: 20px;
    text-align: center;
    color: white;
}

header h1 {
    margin-bottom: 10px;
}

nav ul {
    list-style: none;
}

nav ul li {
    display: inline;
    margin: 0 15px;
}

nav ul li a {
    color: white;
    text-decoration: none;
    font-weight: bold;
}

/* Seção de conteúdo */
.conteudo {
    text-align: center;
    padding: 50px;
    background-color: #fff;
    margin-top: 30px;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    opacity: 0;
    transform: translateY(20px);
    animation: fadeInUp 1s forwards;
}

/* Animação de fade-in e slide-up */
@keyframes fadeInUp {
    0% {
        opacity: 0;
        transform: translateY(20px);
    }
    100% {
        opacity: 1;
        transform: translateY(0);
    }
}

/* Rodapé */
footer {
    text-align: center;
    padding: 10px;
    background-color: #3498db;
    color: white;
    position: fixed;
    width: 100%;
    bottom: 0;
}
document.addEventListener('DOMContentLoaded', () => {
    // Ao carregar a página, adicione a animação ao conteúdo
    const conteudo = document.querySelector('.conteudo');
    if (conteudo) {
        conteudo.classList.add('fade-in');
    }

    // Script para navegação simples (ajustar a URL)
    const linksNav = document.querySelectorAll('.nav-link');
    linksNav.forEach(link => {
        link.addEventListener('click', function(event) {
            event.preventDefault();
            const destino = this.getAttribute('href');
            window.location.href = destino;
        });
    });
});
