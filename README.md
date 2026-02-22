
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
  <title>Crédito para Investimento | Rodlider</title>
  <meta name="description" content="Solicite crédito para investimento de forma rápida e segura." />

  <style>
    /* Reset e Fontes */
    * { box-sizing: border-box; outline: none; }
    
    body {
      font-family: 'Segoe UI', 'Roboto', Helvetica, Arial, sans-serif;
      background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.8)),
        url('https://i.imgur.com/aPLuDmc.jpeg') center/cover no-repeat fixed;
      margin: 0;
      padding: 20px;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      color: #333;
    }

    .container {
      background: #ffffff;
      width: 100%;
      max-width: 500px;
      padding: 35px;
      border-radius: 16px;
      box-shadow: 0 20px 40px rgba(0,0,0,0.4);
      animation: fadeIn 0.5s ease-in-out;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    h2 { 
      margin-top: 0; 
      color: #1a1a1a;
      text-align: center;
      margin-bottom: 25px;
      font-size: 26px;
      font-weight: 700;
    }

    label { 
      display: block; 
      margin-top: 16px; 
      font-weight: 600; 
      color: #444;
      font-size: 14px;
      margin-bottom: 6px;
    }

    input, select {
      width: 100%;
      padding: 14px;
      font-size: 16px;
      border-radius: 8px;
      border: 1px solid #ddd;
      background-color: #f8f9fa;
      transition: all 0.3s ease;
      -webkit-appearance: none;
    }

    select {
      background-image: url("data:image/svg+xml;charset=US-ASCII,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20width%3D%22292.4%22%20height%3D%22292.4%22%3E%3Cpath%20fill%3D%22%23333%22%20d%3D%22M287%2069.4a17.6%2017.6%200%200%200-13-5.4H18.4c-5%200-9.3%201.8-12.9%205.4A17.6%2017.6%200%200%200%200%2082.2c0%205%201.8%209.3%205.4%2012.9l128%20127.9c3.6%203.6%207.8%205.4%2012.8%205.4s9.2-1.8%2012.8-5.4L287%2095c3.5-3.5%205.4-7.8%205.4-12.8%200-5-1.9-9.2-5.5-12.8z%22%2F%3E%3C%2Fsvg%3E");
      background-repeat: no-repeat;
      background-position: right 1rem center;
      background-size: .65em auto;
    }

    input:focus, select:focus {
      border-color: #25D366;
      box-shadow: 0 0 0 3px rgba(37, 211, 102, 0.2);
      background-color: #fff;
    }

    .hidden {
      display: none;
    }

    button {
      width: 100%;
      margin-top: 30px;
      padding: 16px;
      background: #25D366;
      color: #fff;
      border: none;
      border-radius: 8px;
      font-size: 18px;
      font-weight: bold;
      cursor: pointer;
      transition: background 0.3s, transform 0.1s;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      box-shadow: 0 4px 6px rgba(37, 211, 102, 0.3);
    }

    button:hover:not(:disabled) {
      background: #20bd5a;
      transform: translateY(-2px);
    }

    button:disabled { 
      background: #ccc; 
      cursor: not-allowed; 
      opacity: 0.7;
    }

    .lgpd { 
      font-size: 11px; 
      color: #888; 
      margin-top: 20px; 
      text-align: center; 
      line-height: 1.4;
      padding-top: 10px;
      border-top: 1px solid #eee;
    }

    .icon-wa::before {
      content: "💬"; 
      margin-right: 8px;
    }

    @media (max-width: 480px) {
      body { padding: 10px; align-items: flex-start; }
      .container { padding: 25px 20px; border-radius: 12px; margin-top: 10px; }
      h2 { font-size: 22px; }
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>Simulador Rodlider</h2>

    <form id="creditoForm">
      <label for="nome">Nome Completo</label>
      <input type="text" id="nome" placeholder="Digite seu nome" required />

      <label for="telefone">WhatsApp</label>
      <input type="tel" id="telefone" placeholder="99 99999-9999" maxlength="13" required />

      <label for="cidade">Cidade/Estado</label>
      <input type="text" id="cidade" placeholder="Ex: São Luís - MA" required />

      <label for="renda">Renda Mensal Aproximada</label>
      <select id="renda">
        <option value="">Selecione sua renda</option>
        <option>Até R$ 1.500</option>
        <option>R$ 2.500 a R$ 5.000</option>
        <option>R$ 5.000 a R$ 10.000</option>
        <option>R$ 10.000 a R$ 20.000</option>
        <option>Acima de R$ 20.000</option>
      </select>

      <label for="previsao">Previsão para Realizar</label>
      <select id="previsao">
        <option value="">Selecione o prazo</option>
        <option>Até 30 Dias</option>
        <option>Em até 2 meses</option>
        <option>De 3 a 4 meses</option>
        <option>De 4 a 6 meses</option>
        <option>Até em 1 ano</option>
      </select>

      <label for="investimento">Objetivo do Investimento</label>
      <select id="investimento">
        <option>Área Rural / Maquinários Agrícolas</option>
        <option>Veículo (Carro/Caminhão/Máquinas)</option>
        <option>Imóvel / Construção / Terreno</option>
        <option>Loja / Capital de Giro</option>
        <option>Outros</option>
      </select>

      <!-- Nova Pergunta Adicionada -->
      <label for="historico">Já fez Financiamento ou Consórcio?</label>
      <select id="historico">
        <option value="">Selecione uma opção</option>
        <option value="Nenhum">Não, nunca fiz</option>
        <option value="Financiamento">Já fiz Financiamento</option>
        <option value="Consórcio">Já fiz Consórcio</option>
        <option value="Ambos">Já fiz Ambos</option>
      </select>

      <label for="valor">Valor do Crédito Desejado</label>
      <select id="valor">
        <option value="">Selecione o valor</option>
        <option value="70000">R$ 70.000</option>
        <option value="100000">R$ 100.000</option>
        <option value="220000">R$ 220.000</option>
        <option value="350000">R$ 350.000</option>
        <option value="400000">R$ 400.000</option>
        <option value="500000">R$ 500.000</option>
        <option value="700000">R$ 700.000</option>
        <option value="800000">R$ 800.000</option>
        <option value="900000">R$ 900.000</option>
        <option value="1000000">R$ 1.000.000</option>
        <option value="2000000">R$ 2.000.000</option>
        <option value="3000000">R$ 3.000.000</option>
        <option value="5000000">R$ 5.000.000</option>
        <option value="6000000">Acima de R$ 6.000.000</option>
      </select>

      <label for="parcela">Sugestão de Parcela</label>
      <select id="parcela" disabled>
        <option value="">Selecione o crédito primeiro</option>
      </select>

      <label for="possuiEntrada">Você Possui Entrada?</label>
      <select id="possuiEntrada">
        <option value="Nao">Não</option>
        <option value="Sim">Sim</option>
      </select>

      <div id="containerValorEntrada" class="hidden">
        <label for="valorEntrada">Valor Disponível para Entrada</label>
        <select id="valorEntrada">
          <option value="">Selecione o crédito primeiro</option>
        </select>
      </div>

      <button type="button" id="btnEnviar" disabled>
        <span class="icon-wa"></span> Solicitar Simulação
      </button>

      <div class="lgpd">🔒 Seus dados estão seguros e serão utilizados apenas para esta simulação comercial.</div>
    </form>
  </div>

  <script>
    // Tabela oficial Rodlider
    const tabelaCredito = {
      "70000": { p: [790, 870, 950], e: [4100, 4420, 5200] },
      "100000": { p: [1130, 1240, 1360], e: [5860, 6320, 7430] },
      "220000": { p: [2480, 2730, 2990], e: [12900, 13880, 16340] },
      "350000": { p: [3950, 4350, 4750], e: [20500, 22100, 26000] },
      "400000": { p: [4520, 4980, 5430], e: [23400, 25280, 29700] },
      "500000": { p: [5650, 6210, 6780], e: [29300, 31600, 37150] },
      "700000": { p: [7900, 8690, 9500], e: [41000, 44200, 52000] },
      "800000": { p: [9040, 9950, 10860], e: [46900, 50560, 59400] },
      "900000": { p: [10170, 11190, 12210], e: [52700, 56900, 66800] },
      "1000000": { p: [11300, 12430, 13570], e: [58600, 63200, 74300] },
      "2000000": { p: [22600, 24860, 27140], e: [117200, 126400, 148600] },
      "3000000": { p: [33900, 37290, 40710], e: [175800, 189600, 222900] },
      "5000000": { p: [56500, 62150, 67850], e: [293000, 316000, 371500] },
      "6000000": { p: ["67.800,00 (A partir)"], e: ["351.600,00 (A partir)"] }
    };

    const nomeInput = document.getElementById('nome');
    const telefoneInput = document.getElementById('telefone');
    const cidadeInput = document.getElementById('cidade');
    const rendaSelect = document.getElementById('renda');
    const previsaoSelect = document.getElementById('previsao');
    const investimentoSelect = document.getElementById('investimento');
    const historicoSelect = document.getElementById('historico'); // Nova variável
    const valorSelect = document.getElementById('valor');
    const parcelaSelect = document.getElementById('parcela');
    const possuiEntradaSelect = document.getElementById('possuiEntrada');
    const containerValorEntrada = document.getElementById('containerValorEntrada');
    const entradaSelect = document.getElementById('valorEntrada');
    const btn = document.getElementById('btnEnviar');

    function formatarMoeda(valor) {
      if (typeof valor === 'string') return valor;
      return valor.toLocaleString('pt-BR', { minimumFractionDigits: 2 });
    }

    // Gerenciador de visibilidade do campo de entrada
    possuiEntradaSelect.addEventListener('change', () => {
      if (possuiEntradaSelect.value === 'Sim') {
        containerValorEntrada.classList.remove('hidden');
      } else {
        containerValorEntrada.classList.add('hidden');
        entradaSelect.value = "";
      }
      validarBotao();
    });

    // Atualização das opções dinâmicas
    valorSelect.addEventListener('change', () => {
      parcelaSelect.innerHTML = '<option value="">Selecione a parcela</option>';
      entradaSelect.innerHTML = '<option value="">Selecione a entrada</option>';
      
      const dados = tabelaCredito[valorSelect.value];
      
      if (dados) {
        parcelaSelect.disabled = false;
        entradaSelect.disabled = false;

        dados.p.forEach(p => {
          const opt = document.createElement('option');
          opt.value = p;
          opt.textContent = p.toString().includes('partir') ? p : `R$ ${formatarMoeda(p)}`;
          parcelaSelect.appendChild(opt);
        });

        dados.e.forEach(e => {
          const opt = document.createElement('option');
          opt.value = e;
          opt.textContent = e.toString().includes('partir') ? e : `R$ ${formatarMoeda(e)}`;
          entradaSelect.appendChild(opt);
        });
      } else {
        parcelaSelect.disabled = true;
        entradaSelect.disabled = true;
      }
      validarBotao();
    });

    function validarBotao() {
      const obrigatorios = [
        nomeInput.value.length >= 3,
        telefoneInput.value.length >= 12,
        cidadeInput.value.length >= 2,
        rendaSelect.value !== "",
        previsaoSelect.value !== "",
        historicoSelect.value !== "", // Validando o novo campo
        valorSelect.value !== "",
        parcelaSelect.value !== ""
      ];

      let entradaValida = true;
      if (possuiEntradaSelect.value === 'Sim') {
        entradaValida = entradaSelect.value !== "";
      }

      btn.disabled = !(obrigatorios.every(v => v === true) && entradaValida);
    }

    // Listeners para validação em tempo real
    [nomeInput, telefoneInput, cidadeInput, rendaSelect, previsaoSelect, historicoSelect, parcelaSelect, entradaSelect].forEach(el => {
      el.addEventListener('input', validarBotao);
      el.addEventListener('change', validarBotao);
    });

    // Máscara WhatsApp
    telefoneInput.addEventListener('input', (e) => {
      let x = e.target.value.replace(/\D/g, '');
      if (x.length > 11) x = x.slice(0, 11);
      const match = x.match(/^(\d{0,2})(\d{0,5})(\d{0,4})$/);
      if (match) {
        e.target.value = !match[2] ? match[1] 
                         : match[1] + ' ' + match[2] + (match[3] ? '-' + match[3] : '');
      }
    });

    btn.addEventListener('click', () => {
      const valorCreditoTexto = valorSelect.options[valorSelect.selectedIndex].text;
      const parcelaTexto = parcelaSelect.options[parcelaSelect.selectedIndex].text;
      const historicoTexto = historicoSelect.options[historicoSelect.selectedIndex].text; // Captura do novo campo
      
      let entradaFinalMsg = "Não possui entrada no momento";
      if (possuiEntradaSelect.value === 'Sim') {
        entradaFinalMsg = `Sim (${entradaSelect.options[entradaSelect.selectedIndex].text})`;
      }

      const msg = 
        `Olá! Me chamo *${nomeInput.value}*.%0A%0A` +
        `Gostaria de uma simulação de crédito:%0A` +
        `--------------------------------%0A` +
        `📍 *Cidade:* ${cidadeInput.value}%0A` +
        `📞 *Contato:* ${telefoneInput.value}%0A` +
        `📊 *Renda:* ${rendaSelect.value}%0A` +
        `⏳ *Previsão:* ${previsaoSelect.value}%0A` +
        `🏡 *Objetivo:* ${investimentoSelect.value}%0A` +
        `📜 *Histórico:* ${historicoTexto}%0A` +
        `💰 *Crédito:* ${valorCreditoTexto}%0A` +
        `💳 *Parcela:* ${parcelaTexto}%0A` +
        `💵 *Entrada:* ${entradaFinalMsg}`;

      window.open(`https://api.whatsapp.com/send?phone=5598984533013&text=${msg}`, '_blank');
    });
  </script>
</body>
</html>

