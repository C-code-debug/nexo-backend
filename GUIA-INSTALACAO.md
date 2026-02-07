# 🎮 GUIA COMPLETO - NEXO BACKEND

## 📋 O QUE VOCÊ VAI TER:

✅ Site profissional com backend real
✅ Banco de dados SQLite
✅ Sistema de autenticação JWT
✅ API REST completa
✅ Gerenciamento de posts, downloads e atualizações

---

## 📁 PASSO 1: ORGANIZAR AS PASTAS

Crie esta estrutura no seu computador:

```
📁 Nexo/
   📁 backend/
      📄 package.json
      📄 server.js
      📄 database.js
      📄 .env
      📁 public/
         📄 index.html
```

**IMPORTANTE:** Coloque cada arquivo na pasta correta!

---

## ⚙️ PASSO 2: INSTALAR NODE.JS

1. Acesse: https://nodejs.org
2. Baixe a versão **LTS** (recomendada)
3. Instale normalmente (Next, Next, Next...)
4. Reinicie o computador

**Como testar se instalou:**
```bash
node --version
```
Deve mostrar algo como: `v20.11.0`

---

## 📦 PASSO 3: INSTALAR AS DEPENDÊNCIAS

1. Abra o **Prompt de Comando** (CMD) ou **PowerShell**
2. Navegue até a pasta backend:
```bash
cd C:\Users\SeuNome\Desktop\Nexo\backend
```

3. Instale as dependências:
```bash
npm install
```

**Vai instalar:**
- express (servidor web)
- better-sqlite3 (banco de dados)
- bcrypt (criptografia de senhas)
- jsonwebtoken (autenticação)
- cors (permitir requisições)
- dotenv (variáveis de ambiente)

**AGUARDE!** Pode demorar 2-5 minutos.

---

## 🚀 PASSO 4: INICIAR O SERVIDOR

No terminal, dentro da pasta `backend`, rode:

```bash
npm start
```

**Você vai ver:**
```
╔════════════════════════════════════════╗
║     🚀 SERVIDOR NEXO INICIADO! 🚀     ║
╠════════════════════════════════════════╣
║  📍 URL: http://localhost:3000        ║
║  🔐 Login: admin / nexo2024            ║
╚════════════════════════════════════════╝
```

---

## 🌐 PASSO 5: ACESSAR O SITE

1. Abra seu navegador
2. Acesse: **http://localhost:3000**
3. Clique em **"Admin"**
4. Digite a senha: **nexo2024**
5. Pronto! Agora você pode adicionar posts, downloads e atualizações!

---

## 🎯 COMO FUNCIONA:

### **Quando você adiciona um post:**

1. Frontend (index.html) → envia dados para API
2. API (server.js) → verifica se você está logado
3. Banco de dados (database.js) → salva o post
4. API → retorna sucesso
5. Frontend → atualiza a lista de posts

### **Arquivos e suas funções:**

- **package.json** → Lista de dependências do projeto
- **server.js** → Servidor + API REST (rotas)
- **database.js** → Configuração do banco SQLite
- **.env** → Variáveis secretas (senha JWT, porta)
- **public/index.html** → Site (frontend)

---

## 🔧 PROBLEMAS COMUNS:

### ❌ "npm não é reconhecido"
**Solução:** Instale o Node.js

### ❌ "Port 3000 is already in use"
**Solução:** Mude a porta no arquivo `.env`:
```
PORT=3001
```

### ❌ "Cannot find module 'express'"
**Solução:** Rode `npm install` novamente

### ❌ "ENOENT: no such file or directory"
**Solução:** Você está na pasta errada. Use `cd` para ir até a pasta `backend`

---

## 📝 TESTAR A API (Opcional)

Você pode testar a API direto no navegador ou com ferramentas como **Postman**.

### **Listar todos os posts:**
```
GET http://localhost:3000/api/posts
```

### **Fazer login:**
```
POST http://localhost:3000/api/auth/login
Body: {"username":"admin","password":"nexo2024"}
```

---

## 🌐 COLOCAR ONLINE (GRÁTIS)

### **Opção 1: Render.com** (Recomendado)

1. Crie conta: https://render.com
2. Clique em **"New +"** → **"Web Service"**
3. Conecte ao GitHub (faça upload do projeto lá)
4. Configure:
   - **Build Command:** `npm install`
   - **Start Command:** `npm start`
5. Adicione variável de ambiente:
   - **JWT_SECRET**: `sua-chave-secreta-aqui`
6. Clique em **"Create Web Service"**

**Pronto!** Seu site estará online em alguns minutos!

### **Opção 2: Railway.app**

1. Crie conta: https://railway.app
2. **"New Project"** → **"Deploy from GitHub repo"**
3. Selecione o repositório
4. Adicione variável: **JWT_SECRET**
5. Deploy automático!

---

## 🎓 O QUE VOCÊ APRENDEU:

✅ Como funciona um servidor backend
✅ API REST (GET, POST, DELETE)
✅ Banco de dados SQLite
✅ Autenticação com JWT
✅ Comunicação Frontend ↔ Backend
✅ Deploy em produção

---

## 🔒 SEGURANÇA:

### **Mudar a senha admin:**

Edite o arquivo `database.js`, linha 54:
```javascript
const hashedPassword = bcrypt.hashSync('SUA-NOVA-SENHA', 10);
```

### **Mudar a chave JWT:**

Edite o arquivo `.env`:
```
JWT_SECRET=sua-chave-super-secreta-aqui
```

---

## 📚 PRÓXIMOS PASSOS:

1. ✅ Teste localmente
2. ✅ Adicione conteúdo
3. ✅ Customize o visual
4. ✅ Faça upload pro GitHub
5. ✅ Coloque online no Render/Railway

---

## 💡 DICAS:

- O banco de dados `nexo.db` é criado automaticamente
- Não delete esse arquivo ou você perde todos os dados
- Para "resetar" o banco, delete o arquivo `nexo.db` e reinicie o servidor
- O token JWT expira em 24 horas (você precisa fazer login de novo)

---

## 🆘 PRECISA DE AJUDA?

Se der algum erro, me mande:
1. A mensagem de erro completa
2. O comando que você rodou
3. Em qual passo você está

Boa sorte! 🚀
