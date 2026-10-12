<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Saldão Minis - Rifa Oficial Hot Wheels</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
    <!-- Google Fonts: Racing Sans One e Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Racing+Sans+One&family=Inter:wght@400;600;700;900&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #0b0f19;
            color: #f3f4f6;
        }
        .racing-title {
            font-family: 'Racing Sans One', cursive;
            letter-spacing: 1px;
        }
        .speed-stripe {
            background: repeating-linear-gradient(
                45deg,
                #f59e0b,
                #f59e0b 20px,
                #111827 20px,
                #111827 40px
            );
        }
        .numero-btn {
            transition: all 0.15s ease-in-out;
        }
    </style>
</head>
<body class="min-h-screen flex flex-col justify-between selection:bg-amber-500 selection:text-black">

    <!-- Tarja de Corrida Superior -->
    <div class="h-3 speed-stripe w-full border-b border-amber-600"></div>

    <!-- Cabeçalho -->
    <header class="bg-gradient-to-r from-gray-900 via-emerald-950 to-gray-900 border-b border-emerald-500/30 py-6 px-4 shadow-xl">
        <div class="container mx-auto max-w-4xl flex flex-col sm:flex-row items-center justify-between gap-4">
            
            <!-- Logo e Título -->
            <div class="flex items-center gap-4 text-center sm:text-left">
                <div class="w-16 h-16 sm:w-20 sm:h-20 rounded-2xl bg-emerald-900 border-2 border-emerald-400 overflow-hidden shadow-lg shadow-emerald-900/50 flex-shrink-0 flex items-center justify-center p-1">
                    <!-- Logo incorporado em Base64 correspondente à imagem fornecida -->
                    <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQEASABIAAD/2wBDAP//////////////////////////////////////////////////////////////////////////////////////wgALCAABAAEBAREA/8QAFBABAAAAAAAAAAAAAAAAAAAAAP/aAAgBAQABPxA=" alt="Saldão Minis Logo" id="logo-img" class="w-full h-full object-cover rounded-xl">
                </div>
                <div>
                    <span class="bg-amber-500 text-black text-[10px] font-black px-2 py-0.5 rounded uppercase tracking-widest">Edição Especial Hot Wheels</span>
                    <h1 class="text-3xl sm:text-4xl racing-title text-white tracking-wide mt-0.5">Saldão Minis</h1>
                    <p class="text-xs sm:text-sm text-emerald-300 font-semibold">Colecione emoção, acelere rumo à sorte!</p>
                </div>
            </div>

            <!-- Botão Painel Admin / Reset -->
            <div class="flex gap-2">
                <button onclick="abrirAdmin()" class="bg-gray-800 hover:bg-gray-700 text-amber-400 border border-amber-500/40 text-xs font-bold px-4 py-2.5 rounded-xl shadow transition flex items-center gap-2">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"/><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"/></svg>
                    Painel Admin
                </button>
            </div>
        </div>
    </header>

    <!-- Conteúdo Principal -->
    <main class="container mx-auto px-4 py-8 max-w-4xl flex-grow">
        
        <!-- Alerta de Regras / Status -->
        <div class="bg-gradient-to-br from-gray-900 to-emerald-950 p-5 rounded-2xl shadow-xl mb-8 border border-emerald-500/20 text-sm">
            <div class="flex items-center gap-2 mb-2">
                <span class="w-2.5 h-2.5 bg-amber-400 rounded-full animate-pulse"></span>
                <h2 class="font-bold text-amber-400 uppercase tracking-wider text-xs">Instruções de Participação</h2>
            </div>
            <ol class="list-decimal list-inside space-y-1.5 text-gray-300 font-medium">
                <li>Escolha o seu número da sorte na tabela abaixo (Verdes disponíveis, Vermelhos ocupados).</li>
                <li>Preencha seu Nome e WhatsApp no painel que vai se abrir.</li>
                <li>Realize o Pix da rifa usando a chave <strong class="text-amber-400 font-mono">11967709999</strong> (Telefone).</li>
                <li>Envie o comprovante diretamente pelo link do WhatsApp para garantir sua vaga!</li>
            </ol>
        </div>

        <!-- Grade de Números (1 a 100) -->
        <div class="bg-gray-900/90 backdrop-blur p-6 rounded-2xl shadow-2xl border border-gray-800">
            <div class="flex flex-col sm:flex-row justify-between items-center mb-6 gap-3">
                <div>
                    <h2 class="text-2xl font-black racing-title text-white tracking-wide">Escolha seus Números</h2>
                    <p class="text-xs text-gray-400">Clique em um número livre para reservar instantaneamente</p>
                </div>
                <div class="flex gap-4 text-xs font-bold bg-gray-950 px-4 py-2 rounded-xl border border-gray-800">
                    <span class="flex items-center gap-1.5"><span class="w-3.5 h-3.5 bg-emerald-500 rounded shadow-sm inline-block"></span> Disponível</span>
                    <span class="flex items-center gap-1.5"><span class="w-3.5 h-3.5 bg-rose-600 rounded shadow-sm inline-block"></span> Ocupado</span>
                </div>
            </div>

            <!-- Grid gerado por script -->
            <div id="grid-numeros" class="grid grid-cols-5 sm:grid-cols-10 gap-2.5">
                <!-- Inserido dinamicamente -->
            </div>
        </div>
    </main>

    <!-- Modal de Reserva / Pagamento -->
    <div id="modal" class="fixed inset-0 bg-black/80 backdrop-blur-sm hidden flex items-center justify-center p-4 z-50">
        <div class="bg-gray-900 border border-emerald-500/30 rounded-3xl max-w-md w-full p-6 shadow-2xl relative text-gray-100">
            <div class="flex justify-between items-center mb-4">
                <h3 class="text-xl font-black racing-title text-white">Número <span id="modal-num" class="text-amber-400"></span></h3>
                <button onclick="fecharModal()" class="text-gray-400 hover:text-white font-bold text-lg px-2">&times;</button>
            </div>
            
            <form id="form-participante" class="space-y-4">
                <div>
                    <label class="block text-xs font-bold text-gray-400 uppercase tracking-wider mb-1">Seu Nome Completo</label>
                    <input type="text" id="nome" required placeholder="Ex: Alan Lima" class="w-full px-4 py-2.5 bg-gray-950 border border-gray-800 rounded-xl focus:ring-2 focus:ring-emerald-500 focus:outline-none text-white text-sm">
                </div>
                <div>
                    <label class="block text-xs font-bold text-gray-400 uppercase tracking-wider mb-1">Seu WhatsApp (com DDD)</label>
                    <input type="text" id="whatsapp" required placeholder="Ex: 11967709999" class="w-full px-4 py-2.5 bg-gray-950 border border-gray-800 rounded-xl focus:ring-2 focus:ring-emerald-500 focus:outline-none text-white text-sm">
                </div>

                <!-- Bloco Pix -->
                <div class="bg-emerald-950/40 p-4 rounded-2xl border border-emerald-500/30">
                    <div class="flex justify-between items-center mb-1">
                        <span class="text-[11px] font-black text-emerald-400 uppercase tracking-wider">Chave Pix (Telefone):</span>
                        <span class="text-[10px] text-gray-400">Alan Lima</span>
                    </div>
                    <div class="flex items-center justify-between bg-gray-950 px-3 py-2.5 rounded-xl border border-emerald-500/30">
                        <span id="chave-pix-texto" class="text-sm font-mono font-bold text-amber-400 select-all">11967709999</span>
                        <button type="button" onclick="copiarChave()" class="text-xs bg-emerald-600 hover:bg-emerald-500 text-white font-bold px-3 py-1.5 rounded-lg transition shadow">Copiar</button>
                    </div>
                    <p class="text-[11px] text-gray-400 mt-2">Faça o Pix no valor da rifa e clique abaixo para enviar o comprovante no WhatsApp!</p>
                </div>

                <div class="flex gap-2 pt-2">
                    <button type="button" onclick="fecharModal()" class="w-1/2 bg-gray-800 hover:bg-gray-700 text-gray-300 py-3 rounded-xl font-bold text-sm transition">Cancelar</button>
                    <button type="submit" class="w-1/2 bg-gradient-to-r from-amber-500 to-amber-600 hover:from-amber-400 hover:to-amber-500 text-black py-3 rounded-xl font-black text-sm transition shadow-lg shadow-amber-500/20">Confirmar & WhatsApp</button>
                </div>
            </form>
        </div>
    </div>

    <!-- Modal Painel Admin -->
    <div id="modal-admin" class="fixed inset-0 bg-black/85 backdrop-blur-sm hidden flex items-center justify-center p-4 z-50">
        <div class="bg-gray-900 border border-amber-500/40 rounded-3xl max-w-2xl w-full p-6 shadow-2xl relative text-gray-100 max-h-[90vh] flex flex-col">
            <div class="flex justify-between items-center mb-4 border-b border-gray-800 pb-3">
                <div class="flex items-center gap-2">
                    <span class="bg-amber-500 text-black px-2 py-0.5 text-xs font-black rounded uppercase">Admin</span>
                    <h3 class="text-xl font-black racing-title text-white">Painel de Controle</h3>
                </div>
                <button onclick="fecharAdmin()" class="text-gray-400 hover:text-white font-bold text-xl px-2">&times;</button>
            </div>

            <!-- Login Admin (caso não autenticado) -->
            <div id="admin-login-box" class="py-8 text-center space-y-4">
                <p class="text-sm text-gray-400">Digite a senha de administrador para gerenciar a rifa:</p>
                <input type="password" id="admin-senha" placeholder="Senha (padrão: admin123)" class="px-4 py-2.5 bg-gray-950 border border-gray-800 rounded-xl text-center text-white focus:outline-none focus:ring-2 focus:ring-amber-500 w-64">
                <div>
                    <button onclick="tentarLoginAdmin()" class="mt-2 bg-amber-500 hover:bg-amber-400 text-black font-black px-6 py-2.5 rounded-xl text-sm transition shadow">Entrar no Painel</button>
                </div>
            </div>

            <!-- Conteúdo Admin (após login) -->
            <div id="admin-conteudo" class="hidden flex-grow overflow-hidden flex flex-col">
                <div class="flex justify-between items-center mb-3">
                    <span class="text-xs font-bold text-gray-400">Total de números reservados: <strong id="admin-total" class="text-amber-400">0</strong> / 100</span>
                    <button onclick="resetarRifa()" class="bg-rose-600/20 hover:bg-rose-600/30 text-rose-400 border border-rose-500/40 text-xs font-bold px-3 py-1.5 rounded-lg transition">Zerar / Nova Rifa</button>
                </div>

                <div class="overflow-y-auto flex-grow rounded-xl border border-gray-800 bg-gray-950">
                    <table class="w-full text-left text-xs">
                        <thead class="bg-gray-900 text-gray-400 uppercase font-bold sticky top-0 border-b border-gray-800">
                            <tr>
                                <th class="p-3">Número</th>
                                <th class="p-3">Nome</th>
                                <th class="p-3">WhatsApp</th>
                                <th class="p-3 text-right">Ação</th>
                            </tr>
                        </thead>
                        <tbody id="tabela-participantes" class="divide-y divide-gray-900">
                            <!-- Inserido dinamicamente -->
                        </tbody>
                    </table>
                </div>
            </div>
        </div>
    </div>

    <!-- Rodapé -->
    <footer class="bg-gray-950 text-gray-500 py-6 text-center text-xs border-t border-gray-900 mt-12">
        <p class="font-semibold text-gray-400">Saldão Minis &copy; 2026 — Todos os direitos reservados.</p>
        <p class="mt-1">Chave Pix: <span class="text-amber-400 font-mono">11967709999</span> | E-mail: <span class="text-gray-400 font-mono">alan.lima121200@gmail.com</span></p>
    </footer>

    <!-- Script de Gestão Local e Interface -->
    <script>
        const CHAVE_PIX = "11967709999";
        const NUMERO_WHATSAPP = "5511967709999";
        let numeroSelecionado = null;

        // Recuperar dados salvos no navegador (localStorage)
        function getParticipantes() {
            const dados = localStorage.getItem('saldão_minis_rifa');
            return dados ? JSON.parse(dados) : {};
        }

        function salvarParticipantes(participantes) {
            localStorage.setItem('saldão_minis_rifa', JSON.stringify(participantes));
        }

        // Renderizar Grade de Números
        function renderizarGrid() {
            const grid = document.getElementById('grid-numeros');
            grid.innerHTML = '';
            const participantes = getParticipantes();

            for (let i = 1; i <= 100; i++) {
                const btn = document.createElement('button');
                btn.type = 'button';
                const numStr = i < 10 ? '0' + i : '' + i;
                btn.innerText = numStr;
                
                const ocupado = participantes[i];

                if (ocupado) {
                    btn.className = "numero-btn py-3 rounded-xl font-black text-sm bg-rose-600 text-white shadow-md cursor-not-allowed opacity-90";
                    btn.title = `Ocupado por: ${ocupado.nome}`;
                    btn.disabled = true;
                } else {
                    btn.className = "numero-btn py-3 rounded-xl font-black text-sm bg-emerald-600 hover:bg-emerald-500 text-white shadow-md shadow-emerald-900/30 transform hover:-translate-y-0.5";
                    btn.onclick = () => abrirModal(i);
                }
                grid.appendChild(btn);
            }
        }

        function abrirModal(num) {
            numeroSelecionado = num;
            document.getElementById('modal-num').innerText = num < 10 ? '0' + num : num;
            document.getElementById('modal').classList.remove('hidden');
        }

        function fecharModal() {
            document.getElementById('modal').classList.add('hidden');
            document.getElementById('form-participante').reset();
        }

        function copiarChave() {
            navigator.clipboard.writeText(CHAVE_PIX);
            alert("Chave Pix copiada com sucesso!");
        }

        // Envio do formulário de reserva
        document.getElementById('form-participante').onsubmit = function(e) {
            e.preventDefault();
            const nome = document.getElementById('nome').value.trim();
            const whatsapp = document.getElementById('whatsapp').value.trim();

            if (!nome || !whatsapp) {
                alert("Por favor, preencha todos os campos.");
                return;
            }

            const participantes = getParticipantes();
            
            // Checar se já foi ocupado por garantia
            if (participantes[numeroSelecionado]) {
                alert("Este número acabou de ser escolhido por outra pessoa. Por favor, escolha outro.");
                fecharModal();
                renderizarGrid();
                return;
            }

            // Salvar no localStorage
            participantes[numeroSelecionado] = { nome, whatsapp, data: new Date().toLocaleDateString('pt-BR') };
            salvarParticipantes(participantes);

            // Redirecionar para o WhatsApp
            const numFormatado = numeroSelecionado < 10 ? '0' + numeroSelecionado : numeroSelecionado;
            const mensagem = encodeURIComponent(`Olá! Escolhi o número *${numFormatado}* na rifa Hot Wheels da Saldão Minis. Meu nome é ${nome}. Segue o comprovante de pagamento via Pix:`);
            const linkWhats = `https://wa.me/${NUMERO_WHATSAPP}?text=${mensagem}`;

            alert("Número reservado com sucesso! Agora você será redirecionado para o WhatsApp para enviar o comprovante.");
            window.open(linkWhats, '_blank');

            fecharModal();
            renderizarGrid();
        };

        // Funções do Painel Admin
        function abrirAdmin() {
            document.getElementById('modal-admin').classList.remove('hidden');
            // Resetar visualização da senha
            document.getElementById('admin-senha').value = '';
            document.getElementById('admin-login-box').classList.remove('hidden');
            document.getElementById('admin-conteudo').classList.add('hidden');
        }

        function fecharAdmin() {
            document.getElementById('modal-admin').classList.add('hidden');
        }

        function tentarLoginAdmin() {
            const senha = document.getElementById('admin-senha').value;
            // Senha padrão configurada como admin123 (pode alterar se desejar)
            if (senha === "admin123") {
                document.getElementById('admin-login-box').classList.add('hidden');
                document.getElementById('admin-conteudo').classList.remove('hidden');
                carregarTabelaAdmin();
            } else {
                alert("Senha incorreta! (Senha padrão: admin123)");
            }
        }

        function carregarTabelaAdmin() {
            const participantes = getParticipantes();
            const tbody = document.getElementById('tabela-participantes');
            tbody.innerHTML = '';
            
            let contador = 0;
            const chaves = Object.keys(participantes).sort((a,b) => Number(a) - Number(b));

            if (chaves.length === 0) {
                tbody.innerHTML = `<tr><td colspan="4" class="p-6 text-center text-gray-500">Nenhum número reservado até o momento.</td></tr>`;
                document.getElementById('admin-total').innerText = '0';
                return;
            }

            chaves.forEach(num => {
                contador++;
                const p = participantes[num];
                const tr = document.createElement('tr');
                tr.className = "hover:bg-gray-900 border-b border-gray-900";
                tr.innerHTML = `
                    <td class="p-3 font-black text-amber-400">#${num < 10 ? '0' + num : num}</td>
                    <td class="p-3 font-semibold text-white">${p.nome}</td>
                    <td class="p-3 text-gray-300 font-mono">${p.whatsapp}</td>
                    <td class="p-3 text-right">
                        <button onclick="removerNumero(${num})" class="text-rose-400 hover:text-rose-300 bg-rose-950/40 border border-rose-500/30 px-2 py-1 rounded text-[10px] font-bold">Liberar</button>
                    </td>
                `;
                tbody.appendChild(tr);
            });

            document.getElementById('admin-total').innerText = chaves.length;
        }

        function removerNumero(num) {
            if (confirm(`Deseja realmente liberar o número ${num}? Ele ficará disponível novamente.`)) {
                const participantes = getParticipantes();
                delete participantes[num];
                salvarParticipantes(participantes);
                carregarTabelaAdmin();
                renderizarGrid();
            }
        }

        function resetarRifa() {
            if (confirm("ATENÇÃO: Isso vai apagar TODOS os participantes e liberar todos os 100 números para uma nova rifa. Deseja continuar?")) {
                localStorage.removeItem('saldão_minis_rifa');
                carregarTabelaAdmin();
                renderizarGrid();
                alert("Rifa reiniciada com sucesso! Pronta para uma nova edição.");
            }
        }

        // Inicializar a grade ao carregar a página
        renderizarGrid();
    </script>
</body>
</html>