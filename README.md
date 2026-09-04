# Dashboard Gerencial — Pedidos de Água (PWA)

PWA instalável do dashboard do Complexo da Imbiribeira, com vídeo no cabeçalho.

## Estrutura

```
├── index.html          → página principal do dashboard
├── manifest.json        → manifesto do PWA (nome, ícones, cores)
├── sw.js                 → service worker (funcionamento offline)
├── icons/
│   ├── icon-192.png
│   └── icon-512.png
└── assets/
    └── header-video.mp4  → vídeo do cabeçalho
```

## Como publicar no GitHub Pages

1. Crie um repositório novo no GitHub (ex: `agua-imbiribeira-dashboard`).
2. Suba TODOS os arquivos desta pasta para a raiz do repositório (mantendo as subpastas `icons/` e `assets/`).
3. No repositório, vá em **Settings → Pages**.
4. Em **Source**, selecione a branch (ex: `main`) e a pasta `/ (root)`.
5. Salve. Em alguns minutos o GitHub fornecerá uma URL como:
   `https://SEU-USUARIO.github.io/agua-imbiribeira-dashboard/`
6. Acesse essa URL pelo celular ou computador — o navegador vai oferecer a opção **"Instalar app"** / **"Adicionar à tela inicial"**.

## Observações importantes

- O GitHub Pages serve tudo via HTTPS automaticamente, o que é **obrigatório** para o service worker e a instalação como PWA funcionarem.
- Se o repositório for público, o vídeo (~1,6 MB) ficará hospedado normalmente pelo GitHub (sem limite relevante).
- Para trocar o vídeo do cabeçalho no futuro, basta substituir o arquivo `assets/header-video.mp4` por outro `.mp4` com o mesmo nome.
- O `manifest.json` e o `sw.js` usam caminhos relativos — por isso é importante que o site fique na **raiz** do domínio/subdomínio do GitHub Pages (ou ajustar `start_url`/`scope` caso publique em subpasta).
