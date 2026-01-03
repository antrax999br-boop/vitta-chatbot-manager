# Deploy do Backend (WhatsApp Service)

O backend precisa estar acessível publicamente para que o QR Code funcione em outros dispositivos via internet.

## Opção 1: Railway (Recomendado - Gratuito/Barato)

1. Crie uma conta no [Railway.app](https://railway.app/).
2. Crie um novo projeto "Deploy from GitHub repo".
3. Selecione este repositório.
4. Configure o **Root Directory** para: `gochat/server`.
5. Adicione a variável de ambiente (Environment Variable):
   - `PORT`: `3001` (ou deixe o Railway atribuir e use a variável PORT no código, o que já é suportado).
6. Após o deploy, o Railway vai te dar uma URL pública (ex: `https://vitta-backend.up.railway.app`).

## Opção 2: Render (Gratuito para teste)

1. Crie conta no [Render.com](https://render.com/).
2. New Web Service -> Build from Git.
3. Root Directory: `gochat/server`.
4. Build Command: `npm install`.
5. Start Command: `node index.js`.
6. Pegue a URL gerada (ex: `https://vitta-backend.onrender.com`).

---

# Configurando o Frontend

Para que o site acesse o backend na nuvem:

1. Vá para o deploy do seu frontend (Vercel/Netlify).
2. Adicione a seguinte variável de ambiente:
   - `VITE_BACKEND_URL`: `URL_DO_SEU_BACKEND` (ex: `https://vitta-backend.up.railway.app`)
3. Faça um novo deploy (ou Redeploy).

**Nota:** Se estiver testando apenas na rede local (mesmo Wi-Fi), o sistema já foi ajustado para funcionar automaticamente sem configurações extras. Apenas acesse pelo IP do computador onde o servidor está rodando (ex: `http://192.168.x.x:3000`).
