# 📱 Guia de Compilação com Capacitor - Tabuada TechKadosh

Este projeto já está com toda a estrutura e configuração do **Capacitor 6** pronta para ser executada e compilada em aplicativo Android nativo (APK).

---

## 🚀 Pré-requisitos
Antes de compilar o app para Android, certifique-se de ter instalado no seu computador:
1. **Node.js** (versão 18 ou superior): [https://nodejs.org](https://nodejs.org)
2. **Android Studio** (com Android SDK e Command-line Tools instalados): [https://developer.android.com/studio](https://developer.android.com/studio)

---

## 🛠️ Passo a Passo para Gerar o App Android

Abra o seu terminal (PowerShell, Prompt de Comando ou terminal integrado do VSCode) na pasta do projeto:

```powershell
cd "c:\Users\Joao Paulo\Documents\Tabuada TechKadosh"
```

### 1. Instalar as dependências do Capacitor
Execute o comando para baixar e instalar as dependências declaradas no `package.json`:
```bash
npm install
```

---

### 2. Adicionar a plataforma Android ao projeto
Execute o comando para criar a pasta nativa `android/`:
```bash
npx cap add android
```

---

### 3. Sincronizar os arquivos web com o Android
Sempre que fizer alterações nos arquivos HTML, CSS ou JS da pasta `www/`, execute este comando para atualizar o projeto nativo:
```bash
npx cap sync
```

---

### 4. Abrir o projeto no Android Studio
Para compilar, testar em um emulador ou gerar o APK final:
```bash
npx cap open android
```
> O **Android Studio** será aberto automaticamente carregando o projeto completo.

---

## 📦 Como Gerar o APK no Android Studio

1. Aguarde o Android Studio finalizar o sincronismo do Gradle (barra de progresso no canto inferior).
2. No menu superior do Android Studio, vá em:
   **Build** > **Build Bundle(s) / APK(s)** > **Build APK(s)**.
3. Quando concluir, clique no aviso flutuante **locate** para abrir a pasta onde o arquivo `app-debug.apk` foi gerado.
4. Envie esse APK para o seu celular Android e instale!

---

## ⚡ Recursos Nativos já Integrados no Código:
- **Clipboard API**: Cópia nativa da chave Pix com compatibilidade total para web e app.
- **Haptics**: Feedback tátil / vibração nativa nos toques, acertos e erros.
- **Hardware Back Button**: O botão físico/virtual de "Voltar" do celular fecha o jogo e volta para o menu antes de sair do app.
- **Status Bar**: Barra de status do sistema estilizada com a cor de fundo do app (`#0f172a`).
