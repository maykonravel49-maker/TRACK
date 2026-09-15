# TRACK 1.0

Versão instalável do TRACK para iPhone, Android e desktop.

## Arquivos
- `index.html` — aplicativo.
- `manifest.webmanifest` — configuração de instalação.
- `service-worker.js` — cache/offline e base para atualizações.
- `icons/` — ícones do aplicativo.
- `CHANGELOG.md` — histórico das versões.
- `ROADMAP.md` — espaço para planejar futuras atualizações.

## Publicar no GitHub Pages
1. Crie um repositório chamado `TRACK`.
2. Envie **todo o conteúdo desta pasta** para a raiz do repositório.
3. Abra Settings → Pages.
4. Em **Build and deployment**, escolha `Deploy from a branch`.
5. Selecione `main` e `/ (root)` e salve.
6. Aguarde o GitHub gerar o endereço público.

## Atualizações futuras
O código já possui `APP_VERSION`, `DATA_SCHEMA_VERSION` e `runMigrations()`.
Ao adicionar novos recursos, preserve a chave `trackBeta2` do `localStorage` ou faça
a migração em `runMigrations()` para manter os dados existentes.

Ao publicar uma nova versão, altere também `CACHE_NAME` em `service-worker.js`
(ex.: `track-v1.1.0`) para que os dispositivos recebam os arquivos novos.
