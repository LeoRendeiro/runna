# Runna — App de Corrida

## Como publicar e gerar o APK (sem instalar nada)

### Passo 1 — Publicar no GitHub Pages

1. Crie uma conta em **github.com** (se não tiver)
2. Crie um repositório novo:
   - **New repository** → nome: `runna` → **Public** → **Create**
3. Faça upload de **todos os arquivos** desta pasta:
   - Clique em **"uploading an existing file"**
   - Selecione todos os arquivos: `index.html`, `manifest.json`, `sw.js`, `icon-192.svg`, `icon-512.svg`
   - Clique em **Commit changes**
4. Ative o GitHub Pages:
   - Vá em **Settings → Pages**
   - Em **Source**, selecione **GitHub Actions**
   - Salve
5. O workflow `deploy.yml` vai publicar automaticamente
6. Aguarde ~1 minuto → em **Actions** você vê a URL do app

A URL ficará no formato: `https://SEU_USUARIO.github.io/runna/`

---

### Passo 2 — Gerar o APK no PWABuilder

1. Acesse **https://www.pwabuilder.com**
2. Cole a URL do seu app (ex: `https://seu-usuario.github.io/runna/`)
3. Clique em **Start**
4. Aguarde a análise (~10 segundos)
5. Clique em **Android**
6. Clique em **Download Package**
7. Extraia o ZIP baixado — dentro está o `runna.apk`

---

### Passo 3 — Instalar no celular

1. Transfira o `.apk` para o celular (WhatsApp, Drive, cabo)
2. Abra o arquivo no celular
3. Se pedir permissão: **Configurações → Segurança → Fontes desconhecidas**
4. Toque em **Instalar**

---

### Atualizar o app no futuro

1. Substitua o `index.html` por uma versão nova
2. Commit no GitHub → publica automaticamente
3. Volte ao PWABuilder com a mesma URL → gere novo APK

---

## Arquivos

| Arquivo | Função |
|---------|--------|
| `index.html` | Todo o app Runna |
| `manifest.json` | Metadados do PWA (nome, ícones, cores) |
| `sw.js` | Service Worker (cache offline) |
| `icon-192.svg` | Ícone 192×192 |
| `icon-512.svg` | Ícone 512×512 |
| `.github/workflows/deploy.yml` | Deploy automático no GitHub Pages |
