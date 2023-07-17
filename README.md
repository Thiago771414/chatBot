# Chat Bot

Para criar um chatbot no Telegram que envia a mensagem "Bom dia" utilizando JavaScript, você precisará seguir os seguintes passos:

Crie um bot no Telegram:

Abra o aplicativo do Telegram e pesquise por "@BotFather".
Inicie uma conversa com o BotFather e siga as instruções para criar um novo bot.
Anote o token do bot gerado pelo BotFather. Você precisará dele posteriormente.
Configure o ambiente de desenvolvimento:

Certifique-se de ter o Node.js instalado em seu sistema.
Crie um diretório para o seu projeto e abra-o em seu editor de código.
Instale as dependências:
Abra o terminal na pasta do projeto e execute o seguinte comando para criar um arquivo package.json:

```csharp
npm init -y
```
##Instale a biblioteca node-telegram-bot-api executando o seguinte comando:

```csharp
npm install node-telegram-bot-api
```
Crie o arquivo JavaScript:

Crie um arquivo chamado bot.js (ou qualquer nome que preferir) dentro do seu diretório de projeto.

Abra o arquivo bot.js no seu editor de código e adicione o seguinte código:
```csharp
const TelegramBot = require('node-telegram-bot-api');

// Substitua 'TOKEN_DO_SEU_BOT' pelo token do seu bot gerado pelo BotFather
const token = 'TOKEN_DO_SEU_BOT';

// Cria uma instância do bot
const bot = new TelegramBot(token, { polling: true });

// Manipula o comando '/start'
bot.onText(/\/start/, (msg) => {
  const chatId = msg.chat.id;
  bot.sendMessage(chatId, 'Bom dia!');
});
```
Inicie o chatbot:
No terminal, execute o seguinte comando para iniciar o chatbot:
```csharp
node bot.js
```
Agora você tem um chatbot básico que responderá com "Bom dia!" sempre que receber o comando /start no Telegram. Você pode personalizar as mensagens e adicionar mais comandos de acordo com suas necessidades. Certifique-se de substituir 'TOKEN_DO_SEU_BOT' pelo token real do seu bot gerado pelo BotFather.

##bot
![Imagem](https://github.com/Thiago771414/imagensProjetos/commit/fef7ec266048873f0dff3d7edd088dcb026c0502)
