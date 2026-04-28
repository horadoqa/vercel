# Vercel

## 🚀 Visão geral

O [**Vercel**](https://vercel.com/) é uma plataforma de hospedagem focada em aplicações frontend (especialmente com frameworks como Next.js), que permite fazer deploy rápido, automático e escalável diretamente a partir de repositórios Git.

---

## 📦 Pré-requisitos

Antes de começar, você precisa ter:

* Conta no GitHub, GitLab ou Bitbucket
* Node.js instalado (opcional, para desenvolvimento local)
* Conta no Vercel (gratuita)

---

## 🔧 Instalação da CLI (opcional)

Você pode usar o Vercel via interface web, mas a CLI facilita bastante:

```bash
npm install -g vercel
```

Depois, faça login:

```bash
vercel login
```

---

## 📁 Criando ou usando um projeto

Você pode:

### 1. Usar um projeto existente

Se já tem um projeto (React, Next.js, etc.):

```bash
cd meu-projeto
vercel
```

A CLI vai:

* Detectar o framework
* Configurar automaticamente
* Fazer o deploy

---

### 2. Criar um novo projeto (exemplo com Next.js)

```bash
npx create-next-app@latest
cd nome-do-projeto
vercel
```

---

## 🌐 Deploy com Git (método recomendado)

1. Suba seu projeto para o GitHub/GitLab/Bitbucket
2. Acesse o painel do Vercel
3. Clique em **"Add New Project"**
4. Conecte seu repositório
5. Clique em **Deploy**

✨ Pronto! O Vercel fará:

* Build automático
* Deploy contínuo a cada commit
* Preview de cada branch

---

## ⚙️ Configurações importantes

### Variáveis de ambiente

No painel do Vercel:

* Vá em **Settings → Environment Variables**
* Adicione variáveis como:

```
API_KEY=123456
```

---

### Arquivo `vercel.json` (opcional)

Permite customizar o comportamento:

```json
{
  "routes": [
    { "src": "/api/(.*)", "dest": "/api/$1" }
  ]
}
```

---

## 🔄 Deploy automático (CI/CD)

Toda vez que você fizer:

```bash
git push
```

O Vercel automaticamente:

* Faz build
* Roda testes (se configurado)
* Publica nova versão

---

## 🌍 URLs geradas

Cada deploy cria:

* URL de produção:

  ```
  https://meu-projeto.vercel.app
  ```

* URLs de preview:

  ```
  https://meu-projeto-git-branch.vercel.app
  ```

---

## 📊 Benefícios

* Deploy instantâneo ⚡
* CDN global 🌎
* SSL automático 🔒
* Integração com Git 🔄
* Preview por branch 👀

---

## 🧠 Dicas

* Use **Next.js** para melhor integração
* Configure variáveis de ambiente para segurança
* Use preview deployments para revisar mudanças

---

## 📚 Recursos úteis

* Documentação oficial: [https://vercel.com/docs](https://vercel.com/docs)
* CLI help:

```bash
vercel --help
```

---

## ✅ Conclusão

O Vercel é uma das formas mais rápidas e simples de colocar projetos frontend no ar, com foco em produtividade e automação. Ideal tanto para projetos pessoais quanto aplicações em produção.

---


