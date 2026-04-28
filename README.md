<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>DUNA Café</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    body {
      margin: 0;
      font-family: 'Arial', sans-serif;
      background: #f8f6f3;
      color: #333;
    }

    header {
      background: url('https://images.unsplash.com/photo-1509042239860-f550ce710b93');
      background-size: cover;
      background-position: center;
      color: white;
      text-align: center;
      padding: 100px 20px;
    }

    header h1 {
      font-size: 42px;
      margin: 0;
    }

    header p {
      font-size: 18px;
      margin-top: 10px;
    }

    .btn {
      background: #6d4c41;
      color: white;
      padding: 12px 20px;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      margin-top: 20px;
    }

    .container {
      max-width: 1000px;
      margin: auto;
      padding: 30px 20px;
    }

    .produto {
      background: white;
      padding: 20px;
      margin: 20px 0;
      border-radius: 10px;
      box-shadow: 0 3px 8px rgba(0,0,0,0.08);
    }

    h2 {
      margin-top: 0;
    }

    .sobre {
      background: #fff;
      padding: 30px;
      border-radius: 10px;
      margin-top: 40px;
    }

    footer {
      background: #2e1b16;
      color: white;
      text-align: center;
      padding: 20px;
      margin-top: 40px;
    }
  </style>
</head>

<body>

<header>
  <h1>DUNA Café</h1>
  <p>Café 100% Arábico • Qualidade Profissional</p>
  <button class="btn" onclick="scrollToProdutos()">Ver Produtos</button>
</header>

<div class="container" id="produtos">

  <div class="produto">
    <h2>☕ Café Expresso em Grãos</h2>
    <p>1kg: R$ 90,00 | 500g: R$ 45,00</p>
    <button class="btn" onclick="comprar('Café Expresso em Grãos')">Comprar</button>
  </div>

  <div class="produto">
    <h2>☕ Café Gourmet em Pó</h2>
    <p>1kg: R$ 70,00 | 500g: R$ 35,00</p>
    <button class="btn" onclick="comprar('Café Gourmet em Pó')">Comprar</button>
  </div>

  <div class="produto">
    <h2>☕ Café Tradicional em Pó</h2>
    <p>1kg: R$ 58,00 | 500g: R$ 29,00</p>
    <button class="btn" onclick="comprar('Café Tradicional em Pó')">Comprar</button>
  </div>

  <div class="produto">
    <h2>☕ Café Extra Forte em Pó</h2>
    <p>1kg: R$ 58,00 | 500g: R$ 29,00</p>
    <button class="btn" onclick="comprar('Café Extra Forte em Pó')">Comprar</button>
  </div>

  <div class="sobre">
    <h2>Sobre o DUNA Café</h2>
    <p>
      Nosso café é 100% arábico, selecionado com padrão profissional e pensado para quem valoriza sabor de verdade.
      Trabalhamos com grãos de qualidade, garantindo um café fresco, aromático e marcante em cada xícara.
    </p>
    <p>
      Ideal para quem quer sair do café comum e experimentar um nível superior de qualidade.
    </p>
  </div>

</div>

<footer>
  <p>Distribuído por RZ Distribuição</p>
  <p>Pedidos pelo WhatsApp</p>
</footer>

<script>
  function comprar(produto) {
    const numero = "5513997710831";
    const mensagem = `Olá! Quero comprar: ${produto}`;
    const url = `https://wa.me/${numero}?text=${encodeURIComponent(mensagem)}`;
    window.open(url, '_blank');
  }

  function scrollToProdutos() {
    document.getElementById("produtos").scrollIntoView({ behavior: "smooth" });
  }
</script>

</body>
</html>