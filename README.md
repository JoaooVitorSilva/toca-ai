# Toca Aí — player de música offline

App web instalável (PWA). Você importa as músicas do celular uma vez; elas ficam guardadas dentro do app e tocam sem internet. No carro, o celular toca pelo Bluetooth normalmente, e os botões do volante/rádio (próxima, anterior, pausar) funcionam.

## Arquivos
- `index.html` — o app inteiro
- `sw.js` — faz o app abrir sem internet
- `manifest.webmanifest` + ícones — permitem instalar na tela inicial

## Publicar (GitHub Pages, grátis)
Um PWA precisa estar num endereço `https://` para poder ser instalado. Abrir o `index.html` direto do celular não funciona.

1. No GitHub, crie um repositório novo chamado `toca-ai` (público).
2. Envie estes arquivos para a raiz do repositório (botão **Add file → Upload files**, arraste tudo, **Commit changes**).
3. Vá em **Settings → Pages**. Em *Branch*, escolha `main` e pasta `/ (root)` → **Save**.
4. Aguarde 1–2 minutos. O endereço será `https://SEU-USUARIO.github.io/toca-ai/`.

## Instalar no celular
- **Android (Chrome):** abra o endereço → menu ⋮ → **Instalar app** (ou "Adicionar à tela inicial").
- **iPhone (Safari):** abra o endereço → botão Compartilhar → **Adicionar à Tela de Início**.

Depois de instalado, abra uma vez com internet. A partir daí funciona offline.

## Usar
1. Toque em **Adicionar** e selecione os arquivos de música (dá para marcar vários de uma vez).
2. Título, artista, álbum e capa são lidos das tags do MP3. Sem tags, o nome do arquivo é usado (formato `Artista - Título.mp3` funciona melhor). Dá para corrigir em ⋮ → **Editar informações**.
3. Depois de importadas, você pode apagar os arquivos originais da pasta Downloads se quiser economizar espaço — o app guarda a própria cópia.

## Bom saber
- As músicas ficam no armazenamento do navegador. **Não limpe os dados do site/app no navegador**, senão a biblioteca é apagada (os arquivos originais, se você mantiver, podem ser importados de novo).
- Músicas repetidas (mesmo nome e tamanho) são ignoradas na importação.
- Ao atualizar o app no GitHub, troque `tocaai-v1` para `tocaai-v2` no `sw.js` para os celulares pegarem a versão nova.
