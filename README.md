<!DOCTYPE html>
<html lang="pt">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Angola Shope | Descobre e Compra</title>

<meta name="description" content="Descobre produtos, ofertas e novidades na Angola Shope. Encontra eletrónicos, moda, casa e muito mais.">

<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

:root {
    --azul: #0756c9;
    --azul-escuro: #063b86;
    --laranja: #ff851b;
    --branco: #ffffff;
    --fundo: #f3f6fb;
    --texto: #202938;
}

body {
    font-family: Arial, sans-serif;
    background: var(--fundo);
    color: var(--texto);
}

header {
    background: var(--azul);
    color: white;
    padding: 18px 5%;
}

.topo {
    max-width: 1200px;
    margin: auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 15px;
    flex-wrap: wrap;
}

.logo {
    font-size: 25px;
    font-weight: bold;
}

.logo span {
    color: #ffb347;
}

.slogan {
    font-size: 12px;
    margin-top: 5px;
}

.pesquisa {
    display: flex;
    width: 100%;
    max-width: 420px;
    background: white;
    border-radius: 8px;
    overflow: hidden;
}

.pesquisa input {
    width: 100%;
    min-width: 0;
    padding: 13px;
    border: none;
    outline: none;
    font-size: 15px;
}

.pesquisa button {
    background: var(--laranja);
    color: white;
    border: none;
    padding: 0 17px;
    font-weight: bold;
    cursor: pointer;
}

nav {
    background: var(--azul-escuro);
    padding: 13px 5%;
    overflow-x: auto;
}

.menu {
    max-width: 1200px;
    margin: auto;
    display: flex;
    gap: 24px;
    white-space: nowrap;
}

nav a {
    color: white;
    text-decoration: none;
    font-size: 14px;
}

nav a:hover {
    color: #ffb347;
}

.hero {
    background: linear-gradient(120deg, #0756c9, #0c8de5);
    color: white;
    padding: 45px 7%;
    text-align: center;
}

.hero h1 {
    font-size: 32px;
    margin-bottom: 13px;
}

.hero p {
    line-height: 1.6;
    max-width: 600px;
    margin: auto;
}

.hero .destaque {
    color: #ffbf73;
}

.hero button {
    margin-top: 20px;
    background: var(--laranja);
    color: white;
    border: none;
    padding: 14px 24px;
    border-radius: 7px;
    font-weight: bold;
    font-size: 15px;
    cursor: pointer;
}

.container {
    max-width: 1200px;
    margin: auto;
    padding: 30px 5%;
}

.titulo {
    font-size: 23px;
    margin-bottom: 18px;
}

.categorias {
    display: flex;
    gap: 10px;
    overflow-x: auto;
    padding-bottom: 12px;
    margin-bottom: 30px;
}

.categoria {
    background: white;
    border: 1px solid #dfe6f0;
    border-radius: 20px;
    padding: 11px 17px;
    white-space: nowrap;
    cursor: pointer;
    font-size: 14px;
}

.categoria:hover,
.categoria.ativa {
    background: var(--azul);
    color: white;
}

.produtos {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: 17px;
}

.produto {
    background: white;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 3px 12px #0000000b;
    display: flex;
    flex-direction: column;
}

.produto img {
    width: 100%;
    height: 165px;
    object-fit: contain;
    background: white;
    padding: 10px;
}

.info {
    padding: 13px;
    display: flex;
    flex-direction: column;
    flex: 1;
}

.etiqueta {
    color: #087443;
    font-size: 11px;
    font-weight: bold;
    margin-bottom: 8px;
}

.produto h3 {
    font-size: 14px;
    line-height: 1.4;
    margin-bottom: 10px;
}

.preco {
    font-size: 19px;
    color: var(--azul);
    font-weight: bold;
    margin-top: auto;
    margin-bottom: 12px;
}

.comprar {
    display: block;
    width: 100%;
    background: var(--laranja);
    color: white;
    text-align: center;
    text-decoration: none;
    padding: 12px 5px;
    border-radius: 6px;
    font-size: 13px;
    font-weight: bold;
}

.comprar:hover {
    background: #e76e00;
}

.vazio {
    display: none;
    padding: 30px;
    text-align: center;
    grid-column: 1 / -1;
}

.aviso {
    background: #fff6e8;
    border-left: 4px solid var(--laranja);
    padding: 15px;
    border-radius: 5px;
    margin-top: 25px;
    font-size: 13px;
    line-height: 1.6;
}

footer {
    background: #09254a;
    color: white;
    text-align: center;
    padding: 28px 15px;
    margin-top: 20px;
    font-size: 13px;
    line-height: 1.8;
}

footer a {
    color: #ffbf73;
}

@media (max-width: 800px) {
    .produtos {
        grid-template-columns: repeat(2, minmax(0, 1fr));
        gap: 12px;
    }

    .produto img {
        height: 140px;
    }

    .hero h1 {
        font-size: 27px;
    }

    .titulo {
        font-size: 21px;
    }
}

@media (min-width: 801px) {
    .pesquisa {
        width: 45%;
    }
}
</style>
</head>

<body>

<header>
    <div class="topo">
        <div>
            <div class="logo">Angola <span>Shope</span> 🛍️</div>
            <div class="slogan">Descobre produtos. Encontra oportunidades.</div>
        </div>

        <form class="pesquisa" id="formPesquisa">
            <input id="pesquisar" type="search"
                placeholder="O que procuras hoje?"
                aria-label="Pesquisar produtos">
            <button type="submit">Pesquisar</button>
        </form>
    </div>
</header>

<nav>
    <div class="menu">
        <a href="#inicio">Início</a>
        <a href="#categorias">Categorias</a>
        <a href="#produtos">Produtos</a>
        <a href="#promocoes">Promoções</a>
        <a href="#sobre">Sobre nós</a>
    </div>
</nav>

<section class="hero" id="inicio">
    <h1>Bem-vindo à <span class="destaque">Angola Shope!</span></h1>
    <p>
        Descobre produtos de várias categorias num só lugar.
        Explora as nossas sugestões e encontra o que procuras.
    </p>
    <button onclick="document.getElementById('produtos').scrollIntoView({behavior:'smooth'})">
        Explorar produtos
    </button>
</section>

<main class="container">

    <h2 class="titulo" id="categorias">Explora as categorias</h2>

    <div class="categorias">
        <button class="categoria ativa" data-categoria="Todos">Todos</button>
        <button class="categoria" data-categoria="Eletrónicos">📱 Eletrónicos</button>
        <button class="categoria" data-categoria="Moda">👕 Moda</button>
        <button class="categoria" data-categoria="Casa">🏠 Casa</button>
        <button class="categoria" data-categoria="Beleza">✨ Beleza</button>
        <button class="categoria" data-categoria="Acessórios">⌚ Acessórios</button>
    </div>

    <h2 class="titulo" id="produtos">Produtos em destaque</h2>

    <div class="produtos" id="listaProdutos">

        <!-- PRODUTO 1 -->
        <article class="produto" data-categoria="Eletrónicos">
            <img src="https://placehold.co/400x300/f0f5ff/0756c9?text=Auscultadores"
                 alt="Imagem ilustrativa de auscultadores">
            <div class="info">
                <span class="etiqueta">PRODUTO DE EXEMPLO</span>
                <h3>Auscultadores sem fios</h3>
                <p class="preco">Consultar preço</p>
                <a class="comprar" href="#"
                   onclick="alert('Adiciona o teu link de afiliado para este produto.'); return false;">
                   Comprar agora
                </a>
            </div>
        </article>

        <!-- PRODUTO 2 -->
        <article class="produto" data-categoria="Eletrónicos">
            <img src="https://placehold.co/400x300/f0f5ff/0756c9?text=Carregador"
                 alt="Imagem ilustrativa de carregador">
            <div class="info">
                <span class="etiqueta">PRODUTO DE EXEMPLO</span>
                <h3>Carregador USB</h3>
                <p class="preco">Consultar preço</p>
                <a class="comprar" href="#"
                   onclick="alert('Adiciona o teu link de afiliado para este produto.'); return false;">
                   Comprar agora
                </a>
            </div>
        </article>

        <!-- PRODUTO 3 -->
        <article class="produto" data-categoria="Moda">
            <img src="https://placehold.co/400x300/fff3e8/ff851b?text=Moda"
                 alt="Imagem ilustrativa de roupa">
            <div class="info">
                <span class="etiqueta">PRODUTO DE EXEMPLO</span>
                <h3>Roupa casual</h3>
                <p class="preco">Consultar preço</p>
                <a class="comprar" href="#"
                   onclick="alert('Adiciona o teu link de afiliado para este produto.'); return false;">
                   Comprar agora
                </a>
            </div>
        </article>

        <!-- PRODUTO 4 -->
        <article class="produto" data-categoria="Acessórios">
            <img src="https://placehold.co/400x300/f0f5ff/0756c9?text=Relogio"
                 alt="Imagem ilustrativa de relógio">
            <div class="info">
                <span class="etiqueta">PRODUTO DE EXEMPLO</span>
                <h3>Relógio moderno</h3>
                <p class="preco">Consultar preço</p>
                <a class="comprar" href="#"
                   onclick="alert('Adiciona o teu link de afiliado para este produto.'); return false;">
                   Comprar agora
                </a>
            </div>
        </article>

        <!-- PRODUTO 5 -->
        <article class="produto" data-categoria="Casa">
            <img src="https://placehold.co/400x300/f0f5ff/0756c9?text=Casa"
                 alt="Imagem ilustrativa de produto para casa">
            <div class="info">
                <span class="etiqueta">PRODUTO DE EXEMPLO</span>
                <h3>Acessórios para casa</h3>
                <p class="preco">Consultar preço</p>
                <a class="comprar" href="#"
                   onclick="alert('Adiciona o teu link de afiliado para este produto.'); return false;">
                   Comprar agora
                </a>
            </div>
        </article>

        <!-- PRODUTO 6 -->
        <article class="produto" data-categoria="Beleza">
            <img src="https://placehold.co/400x300/fff3e8/ff851b?text=Beleza"
                 alt="Imagem ilustrativa de produto de beleza">
            <div class="info">
                <span class="etiqueta">PRODUTO DE EXEMPLO</span>
                <h3>Acessórios de beleza</h3>
                <p class="preco">Consultar preço</p>
                <a class="comprar" href="#"
                   onclick="alert('Adiciona o teu link de afiliado para este produto.'); return false;">
                   Comprar agora
                </a>
            </div>
        </article>

        <p class="vazio" id="semResultados">
            Não encontrámos produtos para essa pesquisa.
        </p>

    </div>

    <div class="aviso">
        <strong>Informação:</strong> a Angola Shope divulga produtos de outras
        plataformas. Alguns links poderão ser links de afiliado, pelos quais
        podemos receber uma comissão quando uma compra elegível é realizada,
        sem custo adicional para o comprador.
        Os produtos e preços apresentados deverão ser confirmados na plataforma
        de origem.
    </div>

    <section id="promocoes" style="margin-top:35px">
        <h2 class="titulo">🔥 Encontra as tuas próximas ofertas</h2>
        <p>
            Estamos a preparar mais sugestões de produtos para ti.
            Volta para descobrir novidades!
        </p>
    </section>

    <section id="sobre" style="margin-top:30px">
        <h2 class="titulo">Sobre a Angola Shope</h2>
        <p style="line-height:1.7">
            A Angola Shope é um catálogo digital criado para ajudar os visitantes
            a descobrir produtos de diferentes categorias e plataformas.
            As compras são concluídas nos sites dos respetivos vendedores.
        </p>
    </section>

</main>

<footer>
    <strong>Angola Shope</strong><br>
    Descobre produtos e oportunidades online.<br>
    © <span id="ano"></span> Angola Shope. Todos os direitos reservados.
</footer>

<script>
const pesquisa = document.getElementById("pesquisar");
const produtos = [...document.querySelectorAll(".produto")];
const botoes = [...document.querySelectorAll(".categoria")];
const semResultados = document.getElementById("semResultados");

let categoriaAtual = "Todos";

function filtrarProdutos() {
    const termo = pesquisa.value.toLowerCase().trim();
    let encontrados = 0;

    produtos.forEach(produto => {
        const texto = produto.innerText.toLowerCase();
        const categoria = produto.dataset.categoria;

        const correspondeTexto = texto.includes(termo);
        const correspondeCategoria =
            categoriaAtual === "Todos" || categoria === categoriaAtual;

        const mostrar = correspondeTexto && correspondeCategoria;

        produto.style.display = mostrar ? "flex" : "none";

        if (mostrar) encontrados++;
    });

    semResultados.style.display = encontrados ? "none" : "block";
}

document.getElementById("formPesquisa").addEventListener("submit", event => {
    event.preventDefault();
    filtrarProdutos();
    document.getElementById("produtos").scrollIntoView({behavior:"smooth"});
});

pesquisa.addEventListener("input", filtrarProdutos);

botoes.forEach(botao => {
    botao.addEventListener("click", () => {
        categoriaAtual = botao.dataset.categoria;

        botoes.forEach(b => b.classList.remove("ativa"));
        botao.classList.add("ativa");

        filtrarProdutos();
    });
});

document.getElementById("ano").textContent = new Date().getFullYear();
</script>

</body>
</html>
