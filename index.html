<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DRE - Demonstração do Resultado do Exercício com Análise Vertical</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/js/all.min.js"></script>
    <!-- Firebase SDKs para sincronização em nuvem gratuita -->
    <script src="https://www.gstatic.com/firebasejs/9.22.0/firebase-app-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/9.22.0/firebase-database-compat.js"></script>
</head>
<body class="bg-slate-50 text-slate-800 font-sans">

    <!-- Cabeçalho -->
    <header class="bg-slate-900 text-white shadow-md">
        <div class="max-w-7xl mx-auto px-4 py-4 flex flex-col md:flex-row justify-between items-center">
            <div class="flex items-center space-x-3 mb-3 md:mb-0">
                <div class="bg-emerald-600 p-2.5 rounded-lg text-white">
                    <i class="fa-solid fa-chart-line text-xl"></i>
                </div>
                <div>
                    <h1 class="text-xl font-bold tracking-tight">DRE & Análise Vertical</h1>
                    <p class="text-xs text-slate-400">Painel de Gestão e Acompanhamento em Tempo Real</p>
                </div>
            </div>
            <div class="flex items-center space-x-3">
                <span id="sync-status" class="text-xs bg-amber-500/20 text-amber-300 px-3 py-1 rounded-full border border-amber-500/30">
                    <i class="fa-solid fa-circle text-[8px] mr-1"></i> Modo Local / Aguardando Nuvem
                </span>
                <button onclick="toggleAdminModal()" id="btn-admin" class="bg-emerald-600 hover:bg-emerald-700 text-white px-4 py-2 rounded-lg text-sm font-medium transition shadow-sm flex items-center space-x-2">
                    <i class="fa-solid fa-plus-circle"></i>
                    <span>Novo Lançamento</span>
                </button>
            </div>
        </div>
    </header>

    <!-- Conteúdo Principal -->
    <main class="max-w-7xl mx-auto px-4 py-8">
        
        <!-- Filtros e Resumo Rápido -->
        <div class="grid grid-cols-1 md:grid-cols-4 gap-4 mb-6">
            <div class="bg-white p-4 rounded-xl shadow-sm border border-slate-200">
                <p class="text-xs font-semibold text-slate-500 uppercase tracking-wider">Receita Bruta</p>
                <p id="card-rec-bruta" class="text-xl font-bold text-slate-900 mt-1">R$ 0,00</p>
            </div>
            <div class="bg-white p-4 rounded-xl shadow-sm border border-slate-200">
                <p class="text-xs font-semibold text-slate-500 uppercase tracking-wider">Receita Líquida</p>
                <p id="card-rec-liq" class="text-xl font-bold text-blue-600 mt-1">R$ 0,00</p>
            </div>
            <div class="bg-white p-4 rounded-xl shadow-sm border border-slate-200">
                <p class="text-xs font-semibold text-slate-500 uppercase tracking-wider">Lucro Bruto</p>
                <p id="card-lucro-bruto" class="text-xl font-bold text-emerald-600 mt-1">R$ 0,00</p>
            </div>
            <div class="bg-white p-4 rounded-xl shadow-sm border border-slate-200">
                <p class="text-xs font-semibold text-slate-500 uppercase tracking-wider">EBITDA</p>
                <p id="card-ebitda" class="text-xl font-bold text-indigo-600 mt-1">R$ 0,00</p>
            </div>
        </div>

        <!-- Tabela DRE -->
        <div class="bg-white rounded-xl shadow-sm border border-slate-200 overflow-hidden">
            <div class="px-6 py-4 border-b border-slate-200 flex justify-between items-center bg-slate-50/50">
                <h2 class="font-bold text-slate-800"><i class="fa-solid fa-table text-slate-500 mr-2"></i> Demonstração do Resultado do Exercício</h2>
                <div class="text-xs text-slate-500">Base A.V.: Receita Líquida (100%)</div>
            </div>
            <div class="overflow-x-auto">
                <table class="w-full text-left border-collapse text-sm">
                    <thead>
                        <tr class="bg-slate-100/70 text-slate-700 font-semibold border-b border-slate-200">
                            <th class="py-3 px-6">Conta / Descrição</th>
                            <th class="py-3 px-6 text-right">Valor (R$)</th>
                            <th class="py-3 px-6 text-right">A.V. (%)</th>
                        </tr>
                    </thead>
                    <tbody id="dre-table-body" class="divide-y divide-slate-100 text-slate-700">
                        <!-- Preenchido via JavaScript -->
                    </tbody>
                </table>
            </div>
        </div>
    </main>

    <!-- Modal de Lançamentos -->
    <div id="admin-modal" class="fixed inset-0 bg-slate-900/50 backdrop-blur-sm hidden flex items-center justify-center p-4 z-50">
        <div class="bg-white rounded-2xl shadow-xl max-w-lg w-full overflow-hidden">
            <div class="px-6 py-4 bg-slate-900 text-white flex justify-between items-center">
                <h3 class="font-bold text-base"><i class="fa-solid fa-pen-to-square mr-2"></i> Novo Lançamento na DRE</h3>
                <button onclick="toggleAdminModal()" class="text-slate-400 hover:text-white"><i class="fa-solid fa-xmark text-lg"></i></button>
            </div>
            <div class="p-6 space-y-4">
                <div>
                    <label class="block text-xs font-semibold text-slate-600 uppercase mb-1">Selecione a Conta Contábil</label>
                    <select id="lanc-conta" class="w-full border border-slate-300 rounded-lg p-2.5 text-sm focus:ring-2 focus:ring-emerald-500 focus:outline-none">
                        <option value="3.1.1.01.001">Receita com revenda de Mercadoria (E)</option>
                        <option value="3.1.3.01.002">PIS (E)</option>
                        <option value="3.1.3.01.001">ICMS (E)</option>
                        <option value="3.1.3.01.003">COFINS (E)</option>
                        <option value="4.1.1.01.001">Custo de Mercadoria Vendida</option>
                        <!-- SG&A - Pessoal -->
                        <option value="4.2.1.02.001">Salários e Proventos</option>
                        <option value="4.2.1.02.002">Contribuição Previdenciária (INSS)</option>
                        <option value="4.2.1.02.003">FGTS</option>
                        <option value="4.2.1.02.004">13. Salário/Grat.Natalina</option>
                        <option value="4.2.1.02.005">Férias</option>
                        <option value="4.2.1.02.008">Alimentação do Trabalhador</option>
                        <option value="4.2.1.02.009">Transporte do Trabalhador (VT)</option>
                        <option value="4.2.1.02.010">Planos de Saúde e Assit.Médica</option>
                        <option value="4.2.1.02.016">Produtividade</option>
                        <option value="4.2.1.02.018">Ajuda de Custo</option>
                        <!-- SG&A - Comerciais -->
                        <option value="4.2.1.01.002">Gastos com embalagens</option>
                        <option value="4.2.1.01.006">Viagens e estadias comerciais</option>
                        <option value="4.2.1.01.008">Comissão iFood</option>
                        <option value="4.2.1.01.115">Frete Entrega Cliente</option>
                        <option value="4.2.1.01.119">Chargeback</option>
                        <option value="4.2.1.01.121">Licenciamento APP</option>
                        <option value="4.2.1.06.005">Assessorias de Marketing</option>
                        <option value="4.2.1.06.009">Midia de Performance</option>
                        <option value="4.2.1.09.007">Comissões Mercado Livre</option>
                        <option value="4.3.1.02.001">Comissões Cartões de Débito/Crédito</option>
                        <!-- SG&A - Administrativas -->
                        <option value="4.2.1.03.003">Telefone e Internet</option>
                        <option value="4.2.1.03.007">Segurança e Vigilância Instalações</option>
                        <option value="4.2.1.07.003">Material de Expediente e Escritório</option>
                        <option value="4.2.1.07.010">Assessoria e Consultoria em Gestão</option>
                        <option value="4.2.1.07.012">Assessoria e Consultoria Tecnologia da Informação</option>
                        <!-- SG&A - Tributárias -->
                        <option value="4.2.1.08.017">FUMACOP - Fundo Combate à Pobreza</option>
                        <!-- Outras -->
                        <option value="3.1.7.03.002">Recuperações de Despesas (Receita)</option>
                        <option value="4.3.1.01.003">Descontos obtidos (Receita)</option>
                    </select>
                </div>
                <div>
                    <label class="block text-xs font-semibold text-slate-600 uppercase mb-1">Valor (R$)</label>
                    <input type="number" id="lanc-valor" step="0.01" class="w-full border border-slate-300 rounded-lg p-2.5 text-sm focus:ring-2 focus:ring-emerald-500 focus:outline-none" placeholder="0.00">
                </div>
                <div>
                    <label class="block text-xs font-semibold text-slate-600 uppercase mb-1">Descrição / Histórico</label>
                    <input type="text" id="lanc-desc" class="w-full border border-slate-300 rounded-lg p-2.5 text-sm focus:ring-2 focus:ring-emerald-500 focus:outline-none" placeholder="Ex: Faturamento quinzenal ou nota fiscal...">
                </div>
                <div class="pt-2 flex justify-end space-x-3">
                    <button onclick="toggleAdminModal()" class="px-4 py-2 border border-slate-300 text-slate-600 rounded-lg text-sm font-medium hover:bg-slate-50">Cancelar</button>
                    <button onclick="adicionarLancamento()" class="px-4 py-2 bg-emerald-600 text-white rounded-lg text-sm font-medium hover:bg-emerald-700 shadow-sm">Salvar Lançamento</button>
                </div>
            </div>
            <div class="px-6 py-4 bg-slate-50 border-t border-slate-100">
                <h4 class="text-xs font-bold text-slate-500 uppercase mb-2">Lançamentos Recentes</h4>
                <div id="lista-lancamentos-recentes" class="max-h-32 overflow-y-auto space-y-1 text-xs text-slate-600">
                    <!-- Preenchido via JS -->
                </div>
            </div>
        </div>
    </div>

    <!-- Lógica da Aplicação -->
    <script>
        // Mapeamento de Contas e Estrutura DRE
        const estruturaContas = {
            "3.1.1.01.001": { nome: "3.1.1.01.001-Receita com revenda de Mercadoria (E)", tipo: "rec_bruta", pai: "Receita com Revenda de Mercadorias" },
            "3.1.3.01.002": { nome: "3.1.3.01.002-PIS (E)", tipo: "imposto", pai: "PIS" },
            "3.1.3.01.001": { nome: "3.1.3.01.001-ICMS (E)", tipo: "imposto", pai: "ICMS" },
            "3.1.3.01.003": { nome: "3.1.3.01.003-COFINS (E)", tipo: "imposto", pai: "COFINS" },
            "4.1.1.01.001": { nome: "4.1.1.01.001-Custo de Mercadoria Vendida", tipo: "cmv", pai: "Custo das Mercadorias Vendidas" },
            
            // Pessoal
            "4.2.1.02.001": { nome: "4.2.1.02.001-Salários e Proventos", tipo: "sga_pessoal", pai: "Gastos com Pessoal - SG&A" },
            "4.2.1.02.002": { nome: "4.2.1.02.002-Contribuição Previdenciária (INSS)", tipo: "sga_pessoal", pai: "Gastos com Pessoal - SG&A" },
            "4.2.1.02.003": { nome: "4.2.1.02.003-FGTS", tipo: "sga_pessoal", pai: "Gastos com Pessoal - SG&A" },
            "4.2.1.02.004": { nome: "4.2.1.02.004-13. Salário/Grat.Natalina", tipo: "sga_pessoal", pai: "Gastos com Pessoal - SG&A" },
            "4.2.1.02.005": { nome: "4.2.1.02.005-Férias", tipo: "sga_pessoal", pai: "Gastos com Pessoal - SG&A" },
            "4.2.1.02.008": { nome: "4.2.1.02.008-Alimentação do Trabalhador", tipo: "sga_pessoal", pai: "Gastos com Pessoal - SG&A" },
            "4.2.1.02.009": { nome: "4.2.1.02.009-Transporte do Trabalhador (VT)", tipo: "sga_pessoal", pai: "Gastos com Pessoal - SG&A" },
            "4.2.1.02.010": { nome: "4.2.1.02.010-Planos de Saúde e Assit.Médica ao Trab", tipo: "sga_pessoal", pai: "Gastos com Pessoal - SG&A" },
            "4.2.1.02.016": { nome: "4.2.1.02.016-Produtividade", tipo: "sga_pessoal", pai: "Gastos com Pessoal - SG&A" },
            "4.2.1.02.018": { nome: "4.2.1.02.018-Ajuda de Custo", tipo: "sga_pessoal", pai: "Gastos com Pessoal - SG&A" },

            // Comerciais
            "4.2.1.01.002": { nome: "4.2.1.01.002-Gastos com embalagens", tipo: "sga_comercial", pai: "Despesas Comerciais" },
            "4.2.1.01.006": { nome: "4.2.1.01.006-Viagens e estadias comerciais", tipo: "sga_comercial", pai: "Despesas Comerciais" },
            "4.2.1.01.008": { nome: "4.2.1.01.008-Comissão iFood", tipo: "sga_comercial", pai: "Despesas Comerciais" },
            "4.2.1.01.115": { nome: "4.2.1.01.115-Frete Entrega Cliente", tipo: "sga_comercial", pai: "Despesas Comerciais" },
            "4.2.1.01.119": { nome: "4.2.1.01.119-Chargeback", tipo: "sga_comercial", pai: "Despesas Comerciais" },
            "4.2.1.01.121": { nome: "4.2.1.01.121-Licenciamento APP", tipo: "sga_comercial", pai: "Despesas Comerciais" },
            "4.2.1.06.005": { nome: "4.2.1.06.005-Assessorias de Marketing", tipo: "sga_comercial", pai: "Despesas Comerciais" },
            "4.2.1.06.009": { nome: "4.2.1.06.009-Midia de Performance", tipo: "sga_comercial", pai: "Despesas Comerciais" },
            "4.2.1.09.007": { nome: "4.2.1.09.007-Comissões Mercado Livre", tipo: "sga_comercial", pai: "Despesas Comerciais" },
            "4.3.1.02.001": { nome: "4.3.1.02.001-Comissões Cartões de Débito e Crédito", tipo: "sga_comercial", pai: "Despesas Comerciais" },

            // Administrativas
            "4.2.1.03.003": { nome: "4.2.1.03.003-Telefone e Internet", tipo: "sga_admin", pai: "Despesas Administrativas" },
            "4.2.1.03.007": { nome: "4.2.1.03.007-Segurança e Vigilância Instalações", tipo: "sga_admin", pai: "Despesas Administrativas" },
            "4.2.1.07.003": { nome: "4.2.1.07.003-Material de Expediente e Escritório", tipo: "sga_admin", pai: "Despesas Administrativas" },
            "4.2.1.07.010": { nome: "4.2.1.07.010-Assessoria e Consultoria em Gestão", tipo: "sga_admin", pai: "Despesas Administrativas" },
            "4.2.1.07.012": { nome: "4.2.1.07.012-Assessoria e Consultoria Tecnologia da Informação", tipo: "sga_admin", pai: "Despesas Administrativas" },

            // Tributárias
            "4.2.1.08.017": { nome: "4.2.1.08.017-FUMACOP - Repasse Fundo Combate à Pobreza", tipo: "sga_tributaria", pai: "Despesas Tributárias" },

            // Outras
            "3.1.7.03.002": { nome: "3.1.7.03.002-Recuperações de Despesas", tipo: "outras_rec", pai: "Outras Receitas Operacionais" },
            "4.3.1.01.003": { nome: "4.3.1.01.003-Descontos obtidos", tipo: "outras_rec", pai: "Outras Receitas Operacionais" }
        };

        let lancamentos = JSON.parse(localStorage.getItem('dre_lancamentos')) || [
            { id: 1, conta: "3.1.1.01.001", valor: 10950856.90, desc: "Faturamento Anual Inicial" },
            { id: 2, conta: "3.1.3.01.002", valor: 148077.62, desc: "PIS Apurado" },
            { id: 3, conta: "3.1.3.01.001", valor: 440407.30, desc: "ICMS Apurado" },
            { id: 4, conta: "3.1.3.01.003", valor: 683805.96, desc: "COFINS Apurado" },
            { id: 5, conta: "4.1.1.01.001", valor: 7419766.91, desc: "CMV Anual" },
            { id: 6, conta: "4.2.1.02.001", valor: 102175.38, desc: "Salários" },
            { id: 7, conta: "4.2.1.01.008", valor: 294766.58, desc: "iFood" },
            { id: 8, conta: "4.2.1.01.115", valor: 586760.85, desc: "Frete Clientes" }
        ];

        function toggleAdminModal() {
            const modal = document.getElementById('admin-modal');
            modal.classList.toggle('hidden');
            renderizarLancamentosRecentes();
        }

        function formatarMoeda(valor) {
            return valor.toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' });
        }

        function formatarPercentual(valor) {
            return valor.toFixed(2).replace('.', ',') + '%';
        }

        function adicionarLancamento() {
            const conta = document.getElementById('lanc-conta').value;
            const valor = parseFloat(document.getElementById('lanc-valor').value);
            const desc = document.getElementById('lanc-desc').value;

            if (isNaN(valor) || valor <= 0) {
                alert('Por favor, informe um valor válido.');
                return;
            }

            lancamentos.push({ id: Date.now(), conta, valor, desc: desc || 'Lançamento manual' });
            localStorage.setItem('dre_lancamentos', JSON.stringify(lancamentos));
            
            document.getElementById('lanc-valor').value = '';
            document.getElementById('lanc-desc').value = '';
            toggleAdminModal();
            calcularEExibirDRE();
        }

        function renderizarLancamentosRecentes() {
            const container = document.getElementById('lista-lancamentos-recentes');
            container.innerHTML = '';
            [...lancamentos].reverse().slice(0, 5).forEach(l => {
                const infoConta = estruturaContas[l.conta] ? estruturaContas[l.conta].nome : l.conta;
                container.innerHTML += `<div class="flex justify-between items-center bg-white p-2 rounded border border-slate-200">
                    <span class="truncate max-w-[200px]" title="${infoConta}">${infoConta}</span>
                    <span class="font-semibold text-slate-800">${formatarMoeda(l.valor)}</span>
                </div>`;
            });
        }

        function calcularEExibirDRE() {
            // Agrupar somatórios por conta
            let totaisContas = {};
            Object.keys(estruturaContas).forEach(k => totaisContas[k] = 0);

            lancamentos.forEach(l => {
                if (totaisContas[l.conta] !== undefined) {
                    totaisContas[l.conta] += l.valor;
                }
            });

            // Cálculos sintéticos
            let recBruta = totaisContas["3.1.1.01.001"];
            let pis = totaisContas["3.1.3.01.002"];
            let icms = totaisContas["3.1.3.01.001"];
            let cofins = totaisContas["3.1.3.01.003"];
            let totalImpostos = pis + icms + cofins;
            
            let recLiquida = recBruta - totalImpostos;
            let baseAV = recLiquida !== 0 ? recLiquida : 1; // Evita divisão por zero

            let cmv = totaisContas["4.1.1.01.001"];
            let lucroBruto = recLiquida - cmv;

            // SG&A Subtotais
            let sgaPessoal = ["4.2.1.02.001","4.2.1.02.002","4.2.1.02.003","4.2.1.02.004","4.2.1.02.005","4.2.1.02.008","4.2.1.02.009","4.2.1.02.010","4.2.1.02.016","4.2.1.02.018"]
                .reduce((acc, k) => acc + totaisContas[k], 0);

            let sgaComercial = ["4.2.1.01.002","4.2.1.01.006","4.2.1.01.008","4.2.1.01.115","4.2.1.01.119","4.2.1.01.121","4.2.1.06.005","4.2.1.06.009","4.2.1.09.007","4.3.1.02.001"]
                .reduce((acc, k) => acc + totaisContas[k], 0);

            let sgaAdmin = ["4.2.1.03.003","4.2.1.03.007","4.2.1.07.003","4.2.1.07.010","4.2.1.07.012"]
                .reduce((acc, k) => acc + totaisContas[k], 0);

            let sgaTributaria = totaisContas["4.2.1.08.017"];
            let totalSGA = sgaPessoal + sgaComercial + sgaAdmin + sgaTributaria;

            let outrasRecDesp = totaisContas["3.1.7.03.002"] + totaisContas["4.3.1.01.003"];

            let ebitda = lucroBruto - totalSGA + outrasRecDesp;

            // Atualizar Cards no Topo
            document.getElementById('card-rec-bruta').innerText = formatarMoeda(recBruta);
            document.getElementById('card-rec-liq').innerText = formatarMoeda(recLiquida);
            document.getElementById('card-lucro-bruto').innerText = formatarMoeda(lucroBruto);
            document.getElementById('card-ebitda').innerText = formatarMoeda(ebitda);

            // Montar Tabela HTML
            const tbody = document.getElementById('dre-table-body');
            tbody.innerHTML = '';

            function adicionarLinha(titulo, valor, av, ehSintetico = false, corDestaque = '') {
                const classeTr = ehSintetico ? 'bg-slate-50 font-bold text-slate-900 border-t border-b border-slate-200' : 'hover:bg-slate-50/50';
                const corTexto = corDestaque ? corDestaque : '';
                tbody.innerHTML += `
                    <tr class="${classeTr}">
                        <td class="py-2.5 px-6 ${ehSintetico ? 'pl-6' : 'pl-10'}">${titulo}</td>
                        <td class="py-2.5 px-6 text-right ${corTexto}">${formatarMoeda(valor)}</td>
                        <td class="py-2.5 px-6 text-right ${corTexto}">${formatarPercentual(av)}</td>
                    </tr>
                `;
            }

            adicionarLinha("Receita Bruta", recBruta, (recBruta / baseAV) * 100, true);
            adicionarLinha("Receita com Revenda de Mercadorias", recBruta, (recBruta / baseAV) * 100);
            
            adicionarLinha("Impostos S/ Vendas (-)", -totalImpostos, (-totalImpostos / baseAV) * 100, true, "text-red-600");
            adicionarLinha("PIS", -pis, (-pis / baseAV) * 100, false, "text-red-600");
            adicionarLinha("ICMS", -icms, (-icms / baseAV) * 100, false, "text-red-600");
            adicionarLinha("COFINS", -cofins, (-cofins / baseAV) * 100, false, "text-red-600");

            adicionarLinha("Receita Líquida", recLiquida, 100.00, true, "text-blue-600");

            adicionarLinha("CMV & CSP (-)", -cmv, (-cmv / baseAV) * 100, true, "text-red-600");
            adicionarLinha("Custo das Mercadorias Vendidas", -cmv, (-cmv / baseAV) * 100, false, "text-red-600");

            adicionarLinha("Lucro Bruto", lucroBruto, (lucroBruto / baseAV) * 100, true, "text-emerald-600");
            adicionarLinha("Lucro Bruto Ajustado", lucroBruto, (lucroBruto / baseAV) * 100, true, "text-emerald-600");

            adicionarLinha("SG&A (-)", -totalSGA, (-totalSGA / baseAV) * 100, true, "text-red-600");
            adicionarLinha("Gastos com Pessoal - SG&A", -sgaPessoal, (-sgaPessoal / baseAV) * 100, false, "text-red-600");
            adicionarLinha("Despesas Comerciais", -sgaComercial, (-sgaComercial / baseAV) * 100, false, "text-red-600");
            adicionarLinha("Despesas Administrativas", -sgaAdmin, (-sgaAdmin / baseAV) * 100, false, "text-red-600");
            adicionarLinha("Despesas Tributárias", -sgaTributaria, (-sgaTributaria / baseAV) * 100, false, "text-red-600");

            adicionarLinha("Outras Receitas/Despesas Operacionais", outrasRecDesp, (outrasRecDesp / baseAV) * 100, true);
            adicionarLinha("EBITDA", ebitda, (ebitda / baseAV) * 100, true, "text-indigo-600 text-base");
        }

        // Executar ao carregar
        calcularEExibirDRE();
    </script>
</body>
</html>
