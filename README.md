
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Crédito para Investimento | Rodlider</title>
  <meta name="description" content="Solicite crédito para investimento de forma rápida e segura. Imóvel, veículo, rural, construção e mais." />

  <style>
    * { box-sizing: border-box; }
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(rgba(0,0,0,.45), rgba(0,0,0,.45)),
        url('https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTaNxe4-U4K6IoRpn3suhzqypIjc8LYXsom8xhF7uKM2JRfmKtlYK4nRgtU&s=10') center/cover no-repeat fixed;
      margin: 0;
      padding: 20px;
    }
    .container {
      background: #fff;
      max-width: 520px;
      margin: auto;
      padding: 22px;
      border-radius: 14px;
      box-shadow: 0 10px 30px rgba(0,0,0,.2);
    }
    h2 { margin-top: 0; }
    label { display: block; margin-top: 12px; font-weight: bold; text-align: left; }
    input, select, button {
      width: 100%;
      padding: 12px;
      margin-top: 6px;
      font-size: 16px;
      border-radius: 8px;
      border: 1px solid #ccc;
    }

    @media (max-width: 768px) {
      body { padding: 10px; }
      .container { padding: 18px; }
      h2 { font-size: 22px; }
    }

    @media (min-width: 769px) {
      .container { max-width: 560px; }
    }
    }
    button {
      margin-top: 18px;
      background: #25D366;
      color: #fff;
      border: none;
      font-size: 18px;
      cursor: pointer;
    }
    button:disabled { background: #aaa; cursor: not-allowed; }
    .lgpd { font-size: 12px; color: #555; margin-top: 12px; }
  </style>
</head>
<body>
  <div class="container">
    <h2>Crédito para Investimento</h2>

    <form id="creditoForm">
      <label>Nome</label>
      <input type="text" id="nome" required />

      

      <label>WhatsApp</label>
      <input type="tel" id="telefone" placeholder="(99) 99999-9999" required />

      <label>Cidade</label>
      <input type="text" id="cidade" required />

      <label>Possui Entrada?</label>
      <select id="entrada">
        <option value="Sim">Sim</option>
        <option value="Não">Não</option>
      </select>

      <label>Valor da Entrada</label>
      <select id="valorEntrada">
        <option value="Não informado">Selecione</option>
        <option>R$ 2.000</option>
        <option>R$ 3.000</option>
        <option>R$ 5.000</option>
        <option>R$ 8.000</option>
        <option>R$ 10.000</option>
        <option>R$ 20.000</option>
        <option>R$ 30.000</option>
        <option>R$ 40.000</option>
      </select>

      <label>Renda Mensal</label>
      <select id="renda">
        <option>R$ 1.500</option>
        <option>R$ 2.000</option>
        <option>R$ 4.000</option>
        <option>R$ 5.000</option>
        <option>R$ 8.000</option>
        <option>R$ 10.000</option>
        <option>R$ 20.000</option>
        <option>R$ 30.000</option>
        <option>Mais de R$ 35.000</option>
      </select>

      <label>Previsão para Realizar o Investimento</label>
      <select id="previsao">
        <option>Em até 1 mês</option>
        <option>Em 2 meses</option>
        <option>Em 3 meses</option>
        <option>Em até 1 ano</option>
      </select>

      <label>Área de Investimento</label>
      <select id="investimento">
        <option>Área Rural</option>
        <option>Veículo</option>
        <option>Imóvel</option>
        <option>Construção</option>
        <option>Reforma</option>
        <option>Loja / Ponto Comercial</option>
      </select>

      <label>Valor do Crédito</label>
      <select id="valor">
        <option value="">Selecione</option>
        <option value="100000">R$ 100.000</option>
        <option value="150000">R$ 150.000</option>
        <option value="250000">R$ 250.000</option>
        <option value="350000">R$ 350.000</option>
        <option value="500000">R$ 500.000</option>
        <option value="750000">R$ 750.000</option>
        <option value="1000000">R$ 1.000.000</option>
      </select>

      <label>Parcela Estimada</label>
      <select id="parcela">
        <option value="">Selecione o valor acima</option>
      </select>

      <button type="button" id="btnEnviar" disabled>Solicitar via WhatsApp</button>

      <div class="lgpd">🔒 Seus dados são usados apenas para contato comercial.</div>
    </form>
  </div>

  <script>
    const parcelas = {
      100000: [750, 850, 900, 1000],
      150000: [850, 900, 1000, 1250],
      250000: [1000, 1250, 2300],
      350000: [1250, 2300, 3200],
      500000: [2300, 3200, 4500],
      750000: [3200, 4500, 5200],
      1000000: [4500, 5200]
    };

    const valor = document.getElementById('valor');
    const parcela = document.getElementById('parcela');
    const btn = document.getElementById('btnEnviar');

    valor.addEventListener('change', () => {
      parcela.innerHTML = '<option value="">Selecione</option>';
      btn.disabled = true;
      if (parcelas[valor.value]) {
        parcelas[valor.value].forEach(p => {
          const opt = document.createElement('option');
          opt.value = p;
          opt.textContent = `R$ ${p.toLocaleString('pt-BR')}`;
          parcela.appendChild(opt);
        });
      }
    });

    parcela.addEventListener('change', () => {
      btn.disabled = !parcela.value;
    });

    btn.addEventListener('click', () => {
      const msg = `Olá, meu nome é *${nome.value}*.%0A%0ATenho interesse em crédito para investimento:%0A📍 Cidade: ${cidade.value}%0A📞 WhatsApp: ${telefone.value}%0A🏡 Área: ${investimento.value}%0A💰 Crédito: R$ ${Number(valor.value).toLocaleString('pt-BR')}%0A💳 Parcela: R$ ${Number(parcela.value).toLocaleString('pt-BR')}%0A💵 Possui entrada: ${entrada.value}%0A💼 Valor da entrada: ${valorEntrada.value}%0A📊 Renda mensal: ${renda.value}%0A⏳ Previsão do investimento: ${previsao.value}`;
      window.open(`https://api.whatsapp.com/send?phone=5598985263537&text=${msg}`, '_blank');
    });
  </script>
</body>
</html>
