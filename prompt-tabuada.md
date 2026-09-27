# Prompt para app de Tabuada TechKadosh 

Preciso que você crie o código completo de um aplicativo mobile de Tabuada e Matemática interativo, responsivo e moderno, utilizando Vue.js e Tailwind CSS (via CDN ou classes utilitárias). O app deve ser totalmente funcional em um único arquivo (ou estruturado de forma limpa) para ser integrado facilmente em um projeto Capacitor.

Aqui estão os requisitos detalhados:

1. TELAS E ESTADOS DO APLICÁVEL (Gerenciados por reatividade no Vue):
- O app deve ter 3 telas principais controladas por estado ('menu', 'jogo', 'resultado'):

A) TELA INICIAL (MENU):
- Seleção de Operação: Botões interativos para escolher entre Adição (+), Subtração (-), Multiplicação (×), Divisão (÷) ou Misto (aleatório).
- Seleção de Dificuldade (define a quantidade de questões):
  * Fácil: 25 questões (com números base de 1 a 10).
  * Médio: 50 questões.
  * Difícil: 100 questões.
- Botão "Iniciar Jogo" (valida se operação e dificuldade foram selecionadas).
- Seção de Apoio / Rodapé:
  * Botão de Doação Pix: Utiliza a API nativa do navegador (navigator.clipboard.writeText) para copiar a chave "joaopaulojpsp@gmail.com" para a área de transferência, exibindo um alerta visual temporário ("Chave Pix copiada com sucesso!").
  * Link/Botão para o canal do WhatsApp: "TechKadosh TTM" Link https://whatsapp.com/channel/0029Va4nf3i2P59nZly64121 (abrindo o link correspondente em nova aba).
  * Link tambem do meu canal do youtube https://www.youtube.com/@JoaoPauloTechKadoshTTM  (abrindo o link correspondente em nova aba).


B) TELA DE JOGO (EXERCÍCIOS):
- Contador de progresso (ex: Questão X de Y).
- Exibição clara da operação matemática atual (ex: "2 × 4 = ?").
- 3 botões de múltipla escolha com as opções de resposta (1 correta e 2 distratores gerados dinamicamente de forma lógica).
- Feedback visual imediato ao clicar na resposta (destaque verde para certo, vermelho para errado) e transição automática após 1 segundo para a próxima questão.
- Contagem em tempo real de acertos e erros.

C) TELA DE RESULTADO:
- Resumo do desempenho (Total de acertos, erros e aproveitamento em %).
- Botões para "Jogar Novamente" e "Voltar ao Menu Principal".

2. REQUISITOS TÉCNICOS E NATIVOS:
- Utilizar Vue.js 3 com reatividade limpa (ref, computed).
- Usar a API nativa do navegador para a área de transferência (Clipboard API).
- Design Mobile-First, responsivo, bonito, com Tailwind CSS, focado em boa experiência do usuário em telas touch.
- Código comentado, limpo e estruturado para fácil compilação via Capacitor.

💡 O que mudou nesta versão:
 * Vue.js 3: O prompt agora direciona o uso da Composition API (<script setup>), que é o padrão moderno e mais limpo do Vue.
 * APIs Nativas: Especifica o uso da Clipboard API nativa (navigator.clipboard.writeText) para garantir que o botão do Pix copie o e-mail instantaneamente para a área de transferência do celular.
