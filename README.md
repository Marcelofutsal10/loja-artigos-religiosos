# loja-artigos-religiosos
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Loja de Artigos Religiosos</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <!-- Cabeçalho -->
    <header>
        <div class="logo">
            <h1>Loja Religiosa</h1>
        </div>
        <nav class="navbar">
            <ul>
                <li><a href="#inicio">Início</a></li>
                <li><a href="#produtos">Produtos</a></li>
                <li><a href="#sobre">Sobre Nós</a></li>
                <li><a href="#contato">Contato</a></li>
                <li><a href="#carrinho" onclick="toggleCart()">🛒 Carrinho (<span id="cartCount">0</span>)</a></li>
            </ul>
        </nav>
    </header>

    <!-- Carrossel de Imagens -->
    <section id="inicio" class="carousel">
        <div class="carousel-images">
            <img src="image1.jpg" alt="Imagem 1">
            <img src="image2.jpg" alt="Imagem 2">
            <img src="image3.jpg" alt="Imagem 3">
        </div>
        <div class="carousel-text">
            <h2>Artigos Religiosos para Sua Fé</h2>
            <p>Encontre os melhores artigos para suas necessidades espirituais.</p>
        </div>
    </section>

    <!-- Produtos -->
    <section id="produtos" class="products">
        <h2>Produtos em Destaque</h2>
        <div class="filters">
            <button onclick="filterProducts('todos')">Todos</button>
            <button onclick="filterProducts('crucifixos')">Crucifixos</button>
            <button onclick="filterProducts('livros')">Livros</button>
            <button onclick="filterProducts('rosarios')">Rosários</button>
        </div>
        <div class="product-grid" id="productGrid">
            <!-- Produtos Dinâmicos -->
        </div>
    </section>

    <!-- Sobre Nós -->
    <section id="sobre" class="about">
        <h2>Sobre Nós</h2>
        <p>Somos uma loja dedicada a oferecer artigos religiosos de qualidade, para apoiar a sua jornada espiritual.</p>
    </section>

    <!-- Contato -->
    <section id="contato" class="contact">
        <h2>Entre em Contato Conosco</h2>
        <form id="contactForm" action="mailto:seu-email@dominio.com" method="post" enctype="text/plain">
            <label for="nome">Nome:</label>
            <input type="text" id="nome" name="nome" required>

            <label for="email">E-mail:</label>
            <input type="email" id="email" name="email" required>
            
            <label for="contato">Contato:</label>
            <input type="contato" id="contato" name="contato" rquired>
            
            <label for="mensagem">Mensagem:</label>
            <textarea id="mensagem" name="mensagem" required></textarea>
            
          <button type="submit">Enviar Mensagem</button>
           </form>
           </section>

    <!-- Carrinho de Compras -->
    <section id="carrinho" class="cart-popup">
        <div class="cart-content">
            <h2>Carrinho</h2>
            <ul id="cartItems"></ul>
            <p>Total: R$ <span id="cartTotal">0,00</span></p>
            <button onclick="checkout()">Finalizar Compra</button>
            <button onclick="toggleCart()">Fechar</button>
        </div>
    </section>

    <script src="script.js"></script>
</body>
</html>
