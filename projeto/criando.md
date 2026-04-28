# 📘 Exemplo completo — Deploy de um projeto real com Next.js no Vercel

Este guia mostra um fluxo **real do zero até produção**, criando uma aplicação funcional e publicando online.

---

# 🚀 1. Criar o projeto

No terminal:

```bash
npx create-next-app@latest meu-app-vercel
cd meu-app-vercel
```

Durante a criação, você pode aceitar os padrões (ou usar TypeScript se quiser).

---

# ▶️ 2. Rodar localmente

```bash
npm run dev
```

Abra no navegador:

```
http://localhost:3000
```

Você verá o projeto padrão do Next.js rodando.

---

# ✏️ 3. Criar uma página real

Vamos criar uma homepage simples com dados dinâmicos.

Edite o arquivo:

```
app/page.js
```

Substitua por:

```javascript
export default function Home() {
  const data = new Date().toLocaleString();

  return (
    <main style={{ padding: 20 }}>
      <h1>🚀 Meu App com Next.js</h1>
      <p>Deploy usando Vercel</p>

      <h2>Data atual:</h2>
      <p>{data}</p>
    </main>
  );
}
```

---

# 💾 4. Inicializar Git

```bash
git init
git add .
git commit -m "Projeto inicial Next.js"
```

---

# ☁️ 5. Subir para o GitHub

Crie um repositório no GitHub e rode:

```bash
git remote add origin https://github.com/seu-usuario/meu-app-vercel.git
git branch -M main
git push -u origin main
```

---

# 🌐 6. Fazer deploy no Vercel

1. Acesse: [https://vercel.com](https://vercel.com)
2. Clique em **"Add New Project"**
3. Conecte sua conta do GitHub
4. Selecione o repositório `meu-app-vercel`
5. Clique em **Deploy**

⏱️ Em poucos segundos, seu app estará online.

---

# 🔗 7. Resultado

Você receberá uma URL como:

```
https://meu-app-vercel.vercel.app
```

Cada novo `git push` → novo deploy automático.

---

# 🔄 8. Testando deploy automático

Altere o texto:

```javascript
<h1>🔥 Meu App Atualizado!</h1>
```

Depois rode:

```bash
git add .
git commit -m "Atualização de texto"
git push
```

➡️ O Vercel irá:

* Detectar a mudança
* Fazer build
* Publicar automaticamente

---

# ⚙️ 9. Adicionando uma API (exemplo real fullstack)

Crie o arquivo:

```
app/api/hello/route.js
```

Conteúdo:

```javascript
export async function GET() {
  return Response.json({
    message: "Olá do backend!",
    timestamp: new Date()
  });
}
```

Agora acesse:

```
https://seu-app.vercel.app/api/hello
```

🎉 Você criou um backend serverless!

---

# 🔐 10. Variáveis de ambiente

Se precisar de segredo (ex: API externa):

No painel do Vercel:

* Settings → Environment Variables

Exemplo:

```
API_KEY=123456
```

E use no código:

```javascript
process.env.API_KEY
```

---

# 📊 Estrutura final do projeto

```
meu-app-vercel/
├── app/
│   ├── api/
│   │   └── hello/
│   │       └── route.js
│   └── page.js
├── package.json
└── ...
```

---

# 🧠 O que você construiu

* ✅ Frontend com Next.js
* ✅ Backend serverless (API routes)
* ✅ Deploy automático
* ✅ CI/CD integrado
* ✅ App online real

---

# 💡 Próximos passos

Você pode evoluir esse projeto com:

* Banco de dados (MongoDB, PostgreSQL)
* Autenticação (NextAuth)
* Consumo de APIs externas
* UI com Tailwind CSS

---

# ✅ Conclusão

Com o Vercel + Next.js você consegue:

* Criar apps completos
* Fazer deploy em minutos
* Escalar sem gerenciar infraestrutura

---

