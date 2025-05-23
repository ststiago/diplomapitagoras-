<!DOCTYPE html><html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Diploma Validado</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #f9f9f9;
    }
    .valido-container {
      display: none;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background-color: #fff;
      flex-direction: column;
      text-align: center;
      padding: 2rem;
    }
    .valido-container h1 {
      color: #2c3e50;
      font-size: 2rem;
    }
    .valido-container p {
      font-size: 1.1rem;
      margin: 0.5rem 0;
    }
    .valido-container .qr {
      margin-top: 1.5rem;
    }
    .valido-container img {
      width: 180px;
      height: 180px;
    }
    .valido-container .legislacao {
      margin-top: 2rem;
      font-size: 0.9rem;
      color: #555;
      max-width: 600px;
    }
    .form-container {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      background: #f3f3f3;
    }
    .box {
      background: white;
      padding: 2rem;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      width: 100%;
      max-width: 400px;
    }
    input, button {
      width: 100%;
      margin-top: 1rem;
      padding: 0.7rem;
      border-radius: 4px;
      border: 1px solid #ccc;
    }
    button {
      background-color: #003366;
      color: white;
      border: none;
      cursor: pointer;
    }
    .erro {
      color: red;
      margin-top: 1rem;
    }
  </style>
</head>
<body>
  <div class="form-container" id="formulario">
    <div class="box">
      <h1>Validador de Diploma</h1>
      <input type="text" id="codigo" placeholder="Digite o código de validação">
      <button onclick="validarCodigo()">Validar</button>
      <div id="erro" class="erro"></div>
    </div>
  </div>  <div class="valido-container" id="valido">
    <h1>Diploma Validado com Sucesso</h1>
    <p><strong>Nome:</strong> Thiago dos Santos Paula</p>
    <p><strong>Curso:</strong> Licenciatura em Educação Física</p>
    <p><strong>Instituição:</strong> Universidade Pitágoras Unopar Anhanguera</p>
    <p><strong>Conclusão:</strong> 14/12/2024</p>
    <p><strong>Colação de Grau:</strong> 13/01/2025</p>
    <p><strong>Data de Emissão:</strong> 22/01/2025</p>
    <p><strong>Código:</strong> 298.298.45fc10485046</p>
    <div class="qr">
      <img src="https://api.qrserver.com/v1/create-qr-code/?data=https://diplomas.somosd4.com.br/validacao/298.298.45fc10485046&size=180x180" alt="QR Code">
    </div>
    <div class="legislacao">
      Este diploma digital está de acordo com a <strong>Portaria MEC nº 1.095/2018</strong>, que regulamenta a emissão e o registro de diplomas digitais.
      Sua autenticidade pode ser verificada conforme o disposto no <strong>Decreto nº 9.235/2017</strong> e demais normas vigentes do Ministério da Educação.
    </div>
  </div>  <script>
    function validarCodigo() {
      const codigo = document.getElementById('codigo').value.trim();
      const formulario = document.getElementById('formulario');
      const valido = document.getElementById('valido');
      const erro = document.getElementById('erro');

      if (codigo === '298.298.45fc10485046') {
        formulario.style.display = 'none';
        valido.style.display = 'flex';
      } else {
        erro.innerText = 'Código inválido ou não encontrado.';
      }
    }
  </script></body>
</html>
