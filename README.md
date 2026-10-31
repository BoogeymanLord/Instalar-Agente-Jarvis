# Instalar-Agente-Jarvis

🛠️ Como instalar o Jarvis Agent (o "Jarvis" mais completo)

Este pacote foi feito para ser um assistente residente no computador, com suporte a voz (inclusive conversa em tempo real) e mais de 100 ferramentas para controlar o sistema .

Pré-requisitos: Você vai precisar do Python 3.11+ e do Node.js 18+ instalados no seu PC .

Passo 1: Instalação
Abra o terminal (Prompt de Comando ou PowerShell no Windows) e execute o comando abaixo. Ele instala o Jarvis e todas as dependências de voz e automação:
bash

pip install "jarvis-agent[all]"

(Se preferir usar o npm, o comando é npm install -g @acefelix/jarvis, mas a versão via pip costuma ser mais direta para o núcleo em Python) .

Passo 2: Configuração inicial
Após instalar, rode o comando de inicialização. Ele vai te guiar na escolha do provedor de IA (como OpenAI, DeepSeek, ou até modelos locais) e pedir a chave de API (API Key) correspondente:
bash

jarvis --init

Passo 3: Uso
Para iniciar o assistente no modo texto (chat), basta digitar:
bash

jarvis

Para usar a voz, dentro do chat você pode usar o comando /voice (para conversa por turnos) ou /talk (para conversa em tempo real, onde você pode interromper a IA falando) .
🏷️ Como mudar o nome dele

Como o nome "Jarvis" é o comando do programa em si, mudar o nome que a IA "atende" ou se apresenta depende de como o projeto foi construído.

    Mudar a identidade (o que a IA fala): A maioria desses assistentes lê a personalidade de um arquivo de configuração ou de sistema. No caso do Jarvis Agent, as configurações ficam na pasta ~/.jarvis/ (na sua pasta de usuário). Você pode procurar por um arquivo como settings.toml ou similar e adicionar uma instrução no campo de sistema (System Prompt), algo como: "Seu nome é [Novo Nome]. Você é meu assistente pessoal."

    Mudar o comando de ativação: Se você quer digitar meuassistente em vez de jarvis no terminal, isso é mais complexo e envolve criar um "alias" (apelido) no seu sistema operacional ou editar o script de inicialização do pacote. Uma solução mais simples é apenas usar o comando original (jarvis) e, dentro da conversa, ele responder ao novo nome que você definiu na personalidade.

💡 Alternativa focada em "Criar Projetos" (Código)

Se o seu foco principal for programar e criar projetos (e não tanto a conversa por voz), o Open Interpreter pode ser mais interessante. Ele é um agente de terminal que lê seus arquivos, edita código e executa comandos com sua aprovação .

Instalação no Windows (PowerShell):
powershell

irm https://www.openinterpreter.com/install.ps1 | iex

Depois de instalar, entre na pasta do seu projeto e digite i ou interpreter para começar a conversar com ele sobre o código . Ele não tem um sistema de voz nativo tão elaborado quanto o Jarvis Agent, mas é muito eficiente para desenvolvimento.

Resumo: Se você quer o pacote completo com voz e ferramentas, vá de Jarvis Agent. Se o foco for só codar, o Open Interpreter resolve.
