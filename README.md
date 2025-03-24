# BackScan

BackScan é um sistema desenvolvido para capturar a localização do usuário e enviá-la para um bot do Telegram por meio de um servidor Express.

## Tecnologias Utilizadas

- **HTML + JavaScript** - Interface simples para captura da localização
- **Express.js** - Backend para receber e processar os dados
- **Axios** - Comunicação com a API do Telegram
- **Ngrok** - Expor o servidor local para acesso externo

## Como Rodar o Projeto

### Requisitos

- Node.js 16+
- Ngrok (para expor o servidor)
- Conta no Telegram e um bot configurado

### Passos

1. **Clone o repositório:**

   ```sh
   git clone https://github.com/seu-usuario/backscan.git
   cd backscan
   ```

2. **Instale as dependências:**

   ```sh
   npm install
   ```

3. **Configure as variáveis de ambiente:**

   No arquivo `server.js`, substitua `BOT-TOKEN` pelo token do seu bot Telegram.
   
   Substitua `CHAT-TOKEN` pelo ID do chat ou grupo onde quer receber as mensagens.

4. **Inicie o servidor:**

   ```sh
   node server.js
   ```

5. **Exponha o servidor com Ngrok:**

   ```sh
   ngrok http 8088
   ```

6. **Copie a URL gerada pelo Ngrok** (por exemplo, `https://abc123.ngrok.io`).

7. **Atualize a URL no arquivo `index.html`**:

   ```js
   fetch("https://abc123.ngrok.io/send-location", {
   ```

8. **Salve as alterações no arquivo.**

9. **Abra o arquivo `index.html` em um navegador e permita o acesso à localização.**

## Como Criar e Configurar um Bot no Telegram

1. No Telegram, procure pelo `@BotFather`.
2. Envie o comando `/newbot` e siga as instruções para criar um novo bot.
3. Anote o token fornecido pelo `BotFather`.
4. Para obter o ID do chat/grupo:
   - Adicione o bot a um grupo.
   - Envie uma mensagem no grupo.
   - Acesse:
     ```
     https://api.telegram.org/botSEU_BOT_TOKEN/getUpdates
     ```
   - Encontre o `chat_id`.

## Estrutura de Pastas

```
backscan/
│-- index.html   # Página para capturar a localização
│-- server.js    # Servidor Express para processar e enviar os dados
│-- package.json # Dependências do projeto
│-- README.md    # Documentação do projeto
```

## Contribuição

Se você deseja contribuir com o BackScan:

1. **Fork este repositório**
2. **Crie uma branch para sua feature:**
   ```sh
   git checkout -b minha-feature
   ```
3. **Faça commit das mudanças:**
   ```sh
   git commit -m 'Adiciona nova funcionalidade'
   ```
4. **Envie o push para a branch:**
   ```sh
   git push origin minha-feature
   ```
5. **Abra um Pull Request**

---

Sinta-se à vontade para sugerir melhorias ou reportar problemas! 🚀

