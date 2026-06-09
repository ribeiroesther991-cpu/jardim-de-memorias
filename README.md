# Jardim de Memórias

Um jardim digital romântico e imersivo para compartilhar memórias especiais.

## 🌸 Características

- ✨ Interface elegante e romântica
- 🔐 Sistema de autenticação seguro
- 📝 Gerenciamento de capítulos, cartas e fotos
- 🎵 Player de música integrado
- ⭐ Mapa interativo de estrelas (memórias)
- ⏰ Contador de tempo juntos
- 💌 Sistema de mensagens surpresa
- 📱 Totalmente responsivo

## 🚀 Quick Start

### Pré-requisitos
- Node.js 18+
- npm ou yarn
- Conta Supabase

### Instalação

```bash
# Clonar repositório
git clone https://github.com/seu-usuario/jardim-de-memorias.git
cd jardim-de-memorias

# Instalar dependências
npm install

# Configurar variáveis de ambiente
cp .env.example .env.local
```

### Variáveis de Ambiente

Criar arquivo `.env.local`:

```
NEXT_PUBLIC_SUPABASE_URL=sua_url_supabase
NEXT_PUBLIC_SUPABASE_ANON_KEY=sua_anon_key
```

### Executar

```bash
npm run dev
```

Abrir [http://localhost:3000](http://localhost:3000)

## 📚 Estrutura do Projeto

```
jardim-de-memorias/
├── app/
│   ├── api/              # Rotas da API
│   ├── components/       # Componentes React
│   ├── pages/           # Páginas
│   ├── layout.tsx       # Layout principal
│   └── globals.css      # Estilos globais
├── lib/
│   ├── supabase.ts      # Configuração Supabase
│   ├── types.ts         # Tipos TypeScript
│   └── auth-store.ts    # Store de autenticação
├── public/              # Assets estáticos
└── package.json
```

## 🔐 Autenticação

### Login
- Acesse `/login`
- Digite seu usuário e senha
- Será redirecionado para o painel administrativo

### Credenciais Padrão
```
Usuário: admin
Senha: admin123
```

**Importante:** Altere a senha na seção de configurações assim que fizer login!

## 🛠️ Guia de Uso - Administrador

### 📖 Gerenciar Capítulos

1. Vá para **Painel Admin → Capítulos**
2. Clique em **Novo Capítulo**
3. Preencha:
   - Título
   - Descrição
   - Conteúdo (markdown suportado)
   - Marque se deseja bloquear
4. Clique em **Salvar**

### 💌 Adicionar Cartas

1. Vá para **Painel Admin → Cartas**
2. Clique em **Nova Carta**
3. Preencha:
   - Título
   - Conteúdo
   - Selecione música (opcional)
   - Marque se deseja bloquear
4. Clique em **Salvar**

### 📸 Gerenciar Fotos

1. Vá para **Painel Admin → Galeria**
2. Clique em **Adicionar Foto**
3. Selecione o arquivo do seu dispositivo
4. Adicione descrição (opcional)
5. Clique em **Salvar**

### ⭐ Criar Estrelas (Memórias)

1. Vá para **Painel Admin → Nosso Céu**
2. Clique em **Nova Estrela**
3. Preencha:
   - Nome da memória
   - Descrição
   - Conteúdo
   - Foto (opcional)
4. Clique em **Salvar**

### 🎵 Adicionar Músicas

1. Vá para **Painel Admin → Músicas**
2. Clique em **Nova Música**
3. Preencha:
   - Título
   - Artista
   - URL do arquivo de áudio
   - Capa (opcional)
4. Clique em **Salvar**

### ⏰ Configurar Contador de Tempo

1. Vá para **Painel Admin → Configurações**
2. Clique em **Editar Data**
3. Selecione a data do primeiro encontro
4. Clique em **Salvar**

## 📖 Gerenciamento de Conteúdo

### Alterar Textos Sem Programação

Todos os textos podem ser editados pelo painel administrativo. Não é necessário tocar em nenhum código!

### Upload de Fotos

- Formatos suportados: JPG, PNG, WebP
- Tamanho máximo: 5MB
- Upload automático para Supabase Storage

### Adicionar Músicas

Você pode:
1. Fazer upload de arquivos de áudio (MP3, WAV, OGG)
2. Usar URLs de streams (com suporte adequado)

## 🌐 Publicar o Site

### Opção 1: Vercel (Recomendado)

```bash
# Instalar Vercel CLI
npm i -g vercel

# Fazer deploy
vercel
```

### Opção 2: Netlify

1. Conectar repositório GitHub em netlify.com
2. Adicionar variáveis de ambiente
3. Deploy automático

### Opção 3: Seu Próprio Servidor

```bash
# Build para produção
npm run build

# Iniciar servidor
npm start
```

## 📱 Atualizar Apenas com Celular

1. Instale uma app de Git (como GitHub Mobile)
2. Vá para o repositório
3. Edite os arquivos diretamente via interface web
4. O site será atualizado automaticamente em alguns minutos

**Ou:**

Use o painel administrativo (recomenaddo) - funciona 100% no celular!

## 🗄️ Banco de Dados

O projeto utiliza Supabase com as seguintes tabelas:

- `users` - Credenciais de acesso
- `chapters` - Capítulos da história
- `letters` - Cartas românticas
- `photos` - Galeria de fotos
- `music` - Músicas
- `stars` - Memórias (Nosso Céu)
- `surprise_messages` - Mensagens surpresa
- `settings` - Configurações do site

## 🎨 Personalizar Cores

Edite `app/globals.css` para alterar as cores:

```css
:root {
  --color-primary: #ffc0e0;    /* Rosa claro */
  --color-secondary: #f0e6ff;  /* Lilás suave */
  --color-accent: #ffd700;     /* Dourado */
  /* ... */
}
```

## 🐛 Solução de Problemas

### "Erro ao conectar com banco de dados"
- Verifique as variáveis de ambiente
- Confirme que as chaves Supabase estão corretas

### "Login não funciona"
- Certifique-se de que a tabela `users` existe
- Verifique as credenciais padrão

### "Fotos não salvam"
- Confirme permissões no Storage do Supabase
- Verifique tamanho do arquivo

## 📞 Suporte

Para dúvidas ou problemas, consulte a seção de Issues do repositório.

## 💝 Licença

Criado com amor ❤️
