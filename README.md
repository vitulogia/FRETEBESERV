# Calculadora de Pallets & Lucro de Frete (v2.2)

Este pacote contém duas opções de publicação online:

- `index.html` → versão **localStorage** (funciona 100% estática). 
- `index-firebase.html` → versão com **sincronização em tempo real** (Firebase Firestore). 

## Publicar no GitHub Pages (grátis)

1. Crie um repositório no GitHub (ex.: `calculadora-frete`).
2. Suba os arquivos deste pacote (`index.html`, `index-firebase.html`, `README.md`, `.nojekyll`).
3. Vá em **Settings → Pages** e, em **Build and deployment**, escolha **Deploy from a branch** e selecione a branch `main` e a pasta `/root` (ou a branch `gh-pages`).
4. Aguarde o build (alguns segundos). Sua URL ficará algo como:
   - `https://SEU_USUARIO.github.io/calculadora-frete/`

> Dica: você pode renomear `index.html` para ser a versão padrão que abrirá na raiz.

## Usar a versão com sincronização em tempo real

Você pode hospedar `index-firebase.html` **no GitHub Pages** e ainda assim usar o Firebase (o app é cliente, não requer servidor).

Passos:

1. Crie um projeto no [Firebase Console](https://console.firebase.google.com/).
2. Em **Firestore Database**, crie o banco (modo de teste para desenvolvimento). 
3. Em **Configurações do projeto → Seus apps (Web)**, gere a **config do app** e copie o JSON (contendo `apiKey`, `projectId`, `authDomain`, `appId`, etc.).
4. Abra a página publicada (`index-firebase.html`), informe um **Espaço** (ex.: `time-vendas`) — todos que usarem o mesmo **Espaço** verão as alterações **em tempo real**.
5. Cole a **config Firebase (JSON)** no campo e clique **Conectar**. 

> Segurança: em produção, ajuste suas **Rules** do Firestore para restringir leitura/escrita por espaço e/ou autenticação.

## Dúvidas rápidas

- **Funciona no celular?** Sim, o layout é responsivo. 
- **Posso ter vários produtos e veículos?** Sim, tudo fica salvo no espaço. 
- **Sem Firebase, cada dispositivo vê seus próprios dados?** Sim (via `localStorage`). 

---

© 2026
