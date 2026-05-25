# IBDM Radar 360° — Deploy na Vercel

Este pacote contém o app **completo, autocontido e instalável como PWA**.

## 📦 Conteúdo

| Arquivo | Função |
|---|---|
| `index.html` | App completo bundled (1,3 MB · funciona offline) |
| `manifest.json` | Metadados do PWA (nome, ícones, cores) |
| `sw.js` | Service worker para funcionamento offline |
| `icon-192.png` / `icon-512.png` | Ícones do app |
| `icon-maskable-512.png` | Ícone adaptativo Android |
| `apple-touch-icon.png` | Ícone iOS (tela inicial) |
| `icon.svg` | Ícone vetorial |

## 🚀 Deploy na Vercel (3 caminhos)

### Opção A — Drag & drop (mais rápido · 2 min)

1. Acesse https://vercel.com/new
2. Arraste a pasta `deploy/` inteira para a área de upload
3. Clique em **Deploy** (sem alterar configurações)
4. Pronto — Vercel detecta como static site

### Opção B — Vercel CLI

```bash
cd deploy
npx vercel deploy --prod
```

### Opção C — GitHub → Vercel (recomendado para iterar)

1. Crie um repo no GitHub e suba o conteúdo da pasta `deploy/`
2. Em https://vercel.com/new conecte o repo
3. Vercel detecta automaticamente e faz deploy a cada push

## 🌐 Conectar o domínio `mercadoibdm.zynex-ia.tech`

Na Vercel (após o deploy):

1. Abra o projeto → **Settings** → **Domains**
2. Clique em **Add** e cole `mercadoibdm.zynex-ia.tech`
3. Vercel valida o CNAME automaticamente (já apontado para `cname.vercel-dns.com`)
4. SSL/HTTPS é emitido automático em ~1 min

## 📱 Instalação no celular (PWA)

Depois que o domínio estiver ativo:

**iOS (Safari):**
- Abra `mercadoibdm.zynex-ia.tech`
- Toque no botão **Compartilhar** (ícone de seta)
- Selecione **Adicionar à Tela de Início**
- App aparece como ícone nativo

**Android (Chrome):**
- Banner automático "Instalar app" aparece
- Ou Menu (⋮) → **Instalar app**

## 🔧 Atualizações futuras

Quando quiser publicar uma nova versão, basta substituir os arquivos (drag & drop novamente ou `git push`). O service worker cuida do cache.

---

*IBDM Radar 360° · Inteligência produzida por KNA Consultoria com tecnologia Command IA*
