# 🤠 Streamer.bot Interactive Duel Widget

A fully automated, chat-triggered Western duel mini-game for your live stream. Viewers can challenge each other in chat, triggering an interactive on-screen standoff in OBS complete with custom animations, dynamic avatars, randomized outcomes, and synchronized sound effects.

This repository contains two versions:
*   `duel.rar` (English)
*   `duel-twitch-enUS.rar` (English and TWITCH)
*   `duelo.rar` (Portuguese / PT-BR)

---

## 🇺🇸 English Installation

### 1. Extract the Files
Download `duel.rar` and extract all contents into a permanent folder on your PC where you keep your OBS assets. Ensure the `.html` file, fonts, audio files, and images all remain in the exact same folder.

### 2. OBS Setup
*   Add a new **Browser Source** in your OBS scene.
*   Check the box for **Local file** and select the `duelArena.html` file you just extracted.
*   Set dimensions to **1920** (Width) x **1080** (Height).
*   *(Optional)* Check **Control audio via OBS** if you want to mix the gunshot and music volumes directly in your OBS audio mixer (-18.5db is good).

### 3. Streamer.bot Import
*   Open Streamer.bot and click the **Import** button at the top.
*   Drag and drop the provided Streamer.bot import file into the window and click import.

### 4. Compile the C# Scripts
*   Navigate to the newly imported Duel actions.
*   There are **3** "Execute C# Code" sub-actions in total across these actions. 
*   Double-click each one, click the **Compile** button, wait for the "Compiled Successfully" message, and click **Save and Compile** or **OK**.

### 5. Bot Account Protection
In the **Challenge** (`!duel`) action, there is an `If/Else` sub-action. This prevents viewers from triggering a duel against your automated bot account.
*   Double-click this `If/Else` sub-action.
*   Change the target name to your actual Bot's username.
*   *Alternatively: If you do not care if people duel your bot, you can simply disable or delete this sub-action.*

### 6. Enable the Commands
Commands are disabled by default when you import actions. Go to the **Commands** tab in Streamer.bot, right-click, and enable both the Duel Challenge and Duel Accept commands.

---

## 🇧🇷 Instalação em Português (PT-BR)

### 1. Extrair os Arquivos
Baixe o arquivo `duelo.rar` e extraia todo o conteúdo para uma pasta permanente no seu PC, onde você guarda os arquivos do seu OBS. Certifique-se de que o arquivo `.html`, as fontes, os áudios e as imagens fiquem na mesma pasta.

### 2. Configuração no OBS
*   Adicione uma nova **Fonte de Navegador** (Browser Source) na sua cena do OBS.
*   Marque a caixa **Arquivo local** (Local file) e selecione o arquivo `duelo.html` que você acabou de extrair.
*   Defina as dimensões para **1920** (Largura) x **1080** (Altura).
*   *(Opcional)* Marque **Controlar áudio via OBS** se quiser ajustar o volume dos tiros e da música diretamente no mixer de áudio do OBS.

### 3. Importação para o Streamer.bot
*   Abra o Streamer.bot e clique no botão **Import** na parte superior.
*   Arraste e solte o arquivo de importação do Streamer.bot fornecido na janela e clique em importar.

### 4. Compilar os Códigos C#
*   Vá até as ações de Duelo recém-importadas.
*   Existem **3** sub-ações "Execute C# Code" no total.
*   Clique duas vezes em cada uma delas, clique no botão **Compile**, aguarde a mensagem "Compiled Successfully" e clique em **Save and Close**.

### 5. Proteção da Conta do Bot
Na ação de **Desafio** (`!duelo`), há uma sub-ação `If/Else`. Ela serve para evitar que os espectadores desafiem a conta do seu bot automatizado.
*   Clique duas vezes nesta sub-ação `If/Else`.
*   Altere o nome do alvo para o nome de usuário real do seu Bot.
*   *Alternativa: Se você não se importa que os espectadores duelem com seu bot, basta desativar ou excluir essa sub-ação.*

### 6. Ativar os Comandos
Os comandos vêm desativados por padrão quando você importa novas ações. Vá até a aba **Commands** no Streamer.bot, clique com o botão direito e ative os comandos de desafio e aceite do duelo.
---

## ⚙️ WebSocket Port Configuration / Configuração de Porta WebSocket

To communicate properly, the HTML file needs to listen to the correct Streamer.bot WebSocket port. You can change this by opening the HTML file in any text editor (like Notepad).

*   **English (`duel.html`):** Defaults to port **8080**. If you need to change this, edit **Line 147**.
*   **Portuguese (`duelo.html`):** Defaults to port **8081** (often necessary to avoid conflicts with software like NVIDIA Broadcast). If you need to change this, edit **Line 144**.

Para que a comunicação funcione corretamente, o arquivo HTML precisa estar conectado à porta WebSocket correta do Streamer.bot. Você pode alterar isso abrindo o arquivo HTML em qualquer editor de texto (como o Bloco de Notas).

*   **Inglês (`duel.html`):** O padrão é a porta **8080**. Se precisar alterar, edite a **Linha 147**.
*   **Português (`duelo.html`):** O padrão é a porta **8081** (muito útil para evitar conflitos com programas como o NVIDIA Broadcast). Se precisar alterar, edite a **Linha 144**.
