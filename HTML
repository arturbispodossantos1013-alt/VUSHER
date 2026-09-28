<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>REX Chat</title>

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
    }

    body {
      background: #e9eef5;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .chat {
      width: 100%;
      max-width: 600px;
      height: 100vh;
      max-height: 850px;
      background: white;
      display: flex;
      flex-direction: column;
      box-shadow: 0 0 20px #0002;
    }

    .topo {
      background: #1473e6;
      color: white;
      padding: 18px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .topo h1 {
      font-size: 21px;
    }

    .limpar {
      border: none;
      background: #ffffff22;
      color: white;
      padding: 8px 12px;
      border-radius: 8px;
      cursor: pointer;
    }

    .mensagens {
      flex: 1;
      overflow-y: auto;
      padding: 15px;
      background: #f4f7fb;
    }

    .mensagem {
      max-width: 80%;
      margin-bottom: 12px;
      padding: 10px 12px;
      border-radius: 14px;
      position: relative;
      word-wrap: break-word;
    }

    .minha {
      margin-left: auto;
      background: #1473e6;
      color: white;
      border-bottom-right-radius: 3px;
    }

    .outra {
      margin-right: auto;
      background: white;
      color: #222;
      border-bottom-left-radius: 3px;
      box-shadow: 0 1px 4px #0001;
    }

    .nome {
      font-size: 12px;
      font-weight: bold;
      margin-bottom: 4px;
      opacity: .8;
    }

    .texto {
      font-size: 16px;
      padding-right: 5px;
    }

    .hora {
      font-size: 10px;
      opacity: .65;
      margin-top: 5px;
      text-align: right;
    }

    .acoes {
      display: flex;
      gap: 5px;
      margin-top: 6px;
      justify-content: flex-end;
    }

    .acoes button {
      border: none;
      background: transparent;
      color: inherit;
      cursor: pointer;
      font-size: 12px;
      opacity: .8;
    }

    .entrada {
      display: flex;
      gap: 8px;
      padding: 12px;
      background: white;
      border-top: 1px solid #ddd;
    }

    #mensagemInput {
      flex: 1;
      border: 1px solid #ccc;
      border-radius: 20px;
      padding: 12px 15px;
      outline: none;
      font-size: 15px;
    }

    #mensagemInput:focus {
      border-color: #1473e6;
    }

    .enviar {
      width: 48px;
      height: 48px;
      border: none;
      border-radius: 50%;
      background: #1473e6;
      color: white;
      cursor: pointer;
      font-size: 20px;
    }

    .enviar:hover {
      background: #0d5fc2;
    }

    @media (max-width: 600px) {
      body {
        align-items: stretch;
      }

      .chat {
        max-height: none;
      }
    }
  </style>
</head>

<body>

  <div class="chat">

    <div class="topo">
      <h1>💬 REX Chat</h1>
      <button class="limpar" onclick="limparChat()">Limpar</button>
    </div>

    <div class="mensagens" id="mensagens"></div>

    <div class="entrada">
      <input
        type="text"
        id="mensagemInput"
        placeholder="Digite uma mensagem..."
        autocomplete="off"
      >

      <button class="enviar" onclick="enviarMensagem()">➤</button>
    </div>

  </div>

  <script>
    const input = document.getElementById("mensagemInput");
    const mensagensDiv = document.getElementById("mensagens");

    let mensagens = JSON.parse(localStorage.getItem("rexChat")) || [];

    function salvar() {
      localStorage.setItem("rexChat", JSON.stringify(mensagens));
    }

    function horarioAtual() {
      const agora = new Date();

      return agora.toLocaleTimeString("pt-BR", {
        hour: "2-digit",
        minute: "2-digit"
      });
    }

    function mostrarMensagens() {
      mensagensDiv.innerHTML = "";

      mensagens.forEach((msg, index) => {

        const div = document.createElement("div");

        div.className =
          "mensagem " + (msg.eu ? "minha" : "outra");

        div.innerHTML = `
          <div class="nome">${escapar(msg.nome)}</div>

          <div class="texto">
            ${escapar(msg.texto)}
          </div>

          <div class="hora">
            ${msg.hora}
          </div>

          <div class="acoes">
            ${
              msg.eu
              ? `<button onclick="editarMensagem(${index})">✏️ Editar</button>`
              : ""
            }

            <button onclick="apagarMensagem(${index})">
              🗑️ Apagar
            </button>
          </div>
        `;

        mensagensDiv.appendChild(div);
      });

      mensagensDiv.scrollTop = mensagensDiv.scrollHeight;
    }

    function enviarMensagem() {
      const texto = input.value.trim();

      if (!texto) return;

      mensagens.push({
        nome: "Você",
        texto: texto,
        hora: horarioAtual(),
        eu: true
      });

      salvar();
      mostrarMensagens();

      input.value = "";
      input.focus();
    }

    function apagarMensagem(index) {
      if (confirm("Apagar esta mensagem?")) {
        mensagens.splice(index, 1);

        salvar();
        mostrarMensagens();
      }
    }

    function editarMensagem(index) {
      const novoTexto = prompt(
        "Edite sua mensagem:",
        mensagens[index].texto
      );

      if (novoTexto === null) return;

      const texto = novoTexto.trim();

      if (!texto) return;

      mensagens[index].texto = texto;
      mensagens[index].hora = horarioAtual();

      salvar();
      mostrarMensagens();
    }

    function limparChat() {
      if (mensagens.length === 0) return;

      if (confirm("Tem certeza que deseja apagar toda a conversa?")) {
        mensagens = [];

        salvar();
        mostrarMensagens();
      }
    }

    function escapar(texto) {
      return texto
        .replace(/&/g, "&amp;")
        .replace(/</g, "&lt;")
        .replace(/>/g, "&gt;")
        .replace(/"/g, "&quot;")
        .replace(/'/g, "&#039;");
    }

    input.addEventListener("keydown", function(event) {
      if (event.key === "Enter") {
        enviarMensagem();
      }
    });

    mostrarMensagens();
  </script>

</body>
</html>
