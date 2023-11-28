# assistentecedi
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Assistente de Atendimento - CEDI M</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      margin: 20px;
      background-color: #f4f4f4;
    }

    h1 {
      text-align: center;
      color: #2c3e50;
    }

    .categorias-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-around;
      background-color: #00284c;
      padding: 20px;
      border-radius: 10px;
      margin-bottom: 20px;
    }

    .exame-section {
      text-align: center;
      flex: 1;
      margin: 10px; /* Espaçamento entre as categorias */
    }

    label {
      display: block;
      margin-bottom: 8px;
      color: #fff;
      font-weight: bold;
      font-size: 14px; /* Tamanho da fonte reduzido para evitar quebra de linha */
      background-color: #00284c;
      padding: 10px;
      border-radius: 5px;
    }

    button {
      padding: 10px 20px;
      font-size: 16px;
      border: none;
      border-radius: 20px;
      background-color: #348c98;
      color: #fff;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    button:hover {
      background-color: #1e6379;
    }

    .tabela-setores {
      border: 1px solid #ddd;
      border-collapse: collapse;
      margin-top: 20px;
      width: 100%;
    }

    .tabela-setores th, .tabela-setores td {
      border: 1px solid #ddd;
      padding: 8px;
      text-align: left;
    }

    .tabela-setores th {
      background-color: #00284c;
      color: white;
    }

    .pesquisa-container {
      margin-bottom: 20px;
      text-align: left;
    }

    input[type="text"] {
      padding: 8px;
      font-size: 14px;
      border-radius: 5px;
    }

    .lupa-icon {
      cursor: pointer;
      margin-top: -30px;
      margin-left: 20px;
    }
  </style>
</head>
<body>
  <h1>Assistente de Atendimento - CEDI M</h1>

  <div class="categorias-container">
    <div class="exame-section" id="mamografia">
      <label>Mamografia</label>
      <button onclick="enviarExame('mamografia')">Enviar</button>
    </div>

    <div class="exame-section" id="raio-x">
      <label>Raio X</label>
      <button onclick="enviarExame('raio-x')">Enviar</button>
    </div>

    <div class="exame-section" id="ultrassom">
      <label>Ultrassom</label>
      <button onclick="enviarExame('ultrassom')">Enviar</button>
    </div>

    <div class="exame-section" id="tomografia">
      <label>TC</label>
      <button onclick="enviarExame('tomografia')">Enviar</button>
    </div>

    <div class="exame-section" id="densitometria">
      <label>DO</label>
      <button onclick="enviarExame('densitometria')">Enviar</button>
    </div>

    <div class="exame-section" id="angio-tc">
      <label>Angio TC</label>
      <button onclick="enviarExame('angio-tc')">Enviar</button>
    </div>

    <div class="exame-section" id="angio-rm">
      <label>Angio RM</label>
      <button onclick="enviarExame('angio-rm')">Enviar</button>
    </div>

    <div class="exame-section" id="rm-mamas">
      <label>RM Mamas</label>
      <button onclick="enviarExame('rm-mamas')">Enviar</button>
    </div>
  
    <div class="exame-section" id="RM">
      <label>RM</label>
      <button onclick="enviarExame('RM')">Enviar</button>
    </div>
  </div>

  <div class="pesquisa-container">
    <label for="pesquisa">Pesquisar por Setor:</label>
    <input type="text" id="pesquisa" placeholder="Digite o nome do setor">
    <span class="lupa-icon" onclick="pesquisarSetor()">🔍</span>
  </div>

  <div class="tabela-setores">
    <table>
      <tr>
        <th>Setor</th>
        <th>Ramais</th>
      </tr>
      <tr>
        <td>Resultados de exame - Unidade 01</td>
        <td>1226, 1217, 1281</td>
      </tr>
      <tr>
        <td>Resultados de exame - Unidade 02</td>
        <td>1329, 1332</td>
      </tr>
      <tr>
        <td>RH</td>
        <td>1205</td>
      </tr>
      <tr>
        <td>Resultado Rio das Ostras</td>
        <td>1465, 1467</td>
      </tr>
      <tr>
        <td>Marcela Coordenadora</td>
        <td>1275</td>
      </tr>
      <tr>
        <td>Compras</td>
        <td>1285</td>
      </tr>
      <tr>
        <td>T.I</td>
        <td>1232</td>
      </tr>
      <tr>
        <td>Ruan Autorização</td>
        <td>1110</td>
      </tr>
      <tr>
        <td>Angela Telefonista</td>
        <td>1200</td>
      </tr>
      <tr>
        <td>Cintilografia</td>
        <td>022992725979</td>
      </tr>
      <tr>
    </table>
  </div>

  <script>
    function enviarExame(categoria) {
      if (categoria === 'mamografia') {
        window.location.href = 'https://matheusfrutuoso.w3spaces.com/codigomamografia.html';
      } else if (categoria === 'raio-x') {
        window.location.href = 'https://matheusfrutuoso.w3spaces.com/raiox.html';
      } else if (categoria === 'ultrassom') {
        window.location.href = 'https://matheusfrutuoso.w3spaces.com/sistemaultrassom.html';
      } else if (categoria === 'densitometria') {
        window.location.href = 'https://matheusfrutuoso.w3spaces.com/codigoDO.html';
      } else {
        // Adicione aqui a lógica para redirecionar ou processar o envio para outras categorias
        alert('Enviando exame: ' + categoria);
      }
    }

    function pesquisarSetor() {
      const inputPesquisa = document.getElementById('pesquisa').value.toLowerCase();
      const linhasTabela = document.querySelectorAll('.tabela-setores tr');

      linhasTabela.forEach((linha) => {
        const nomeSetor = linha.cells[0].textContent.toLowerCase();
        if (nomeSetor.includes(inputPesquisa)) {
          linha.style.display = '';
        } else {
          linha.style.display = 'none';
        }
      });
    }

    function abrirLink(link) {
      window.open(link, '_blank');
    }
  </script>
</body>
</html>
