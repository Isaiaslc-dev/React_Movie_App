# 🎬 Movie Search App

> Aplicação web para buscar e descobrir filmes usando a API do TMDB, com rastreamento de buscas populares via Appwrite.

## 📋 Sobre o Projeto

Movie Search App é uma aplicação moderna de busca de filmes que permite aos usuários:

- 🔍 Buscar filmes em tempo real com debounce
- 🎯 Visualizar filmes populares
- 📊 Ver os filmes mais buscados (trending)
- ⭐ Conferir avaliações, ano de lançamento e idioma original
- 🎨 Interface moderna e responsiva com gradientes e animações

## ✨ Funcionalidades

- **Busca com Debounce**: Busca otimizada que aguarda 1 segundo após o usuário parar de digitar
- **Trending Movies**: Top 5 filmes mais buscados pelos usuários, armazenados no Appwrite
- **Filmes Populares**: Exibe filmes populares quando não há busca ativa
- **Design Responsivo**: Funciona perfeitamente em desktop, tablet e mobile
- **Loading States**: Feedback visual durante carregamento
- **Error Handling**: Tratamento adequado de erros da API

## 🚀 Tecnologias Utilizadas

### Frontend
- **React 19.2** - Biblioteca JavaScript para interfaces
- **Vite 7.2** - Build tool ultra-rápido
- **TailwindCSS v4** - Framework CSS utility-first
- **React Hooks** - useState, useEffect, useDebounce

### Backend & Database
- **Appwrite** - Backend-as-a-Service para armazenar buscas
- **TMDB API** - The Movie Database API para dados de filmes

### Bibliotecas Adicionais
- **react-use** - Hooks utilitários para React (useDebounce)
- **appwrite SDK** - Cliente JavaScript para Appwrite

## 📦 Instalação

### Pré-requisitos

- Node.js 18+ 
- npm ou yarn
- Conta no TMDB (https://www.themoviedb.org/)
- Conta no Appwrite Cloud (https://cloud.appwrite.io/)

### Passo a Passo

1. **Clone o repositório**
   
git clone [https://github.com/seu-usuario/movie-search-app.git](https://github.com/Isaiaslc-dev/React_Movie_App)


3. **Instale as dependências**
```bash
npm install
```

3. **Configure as variáveis de ambiente**

Crie um arquivo `.env` na raiz do projeto:

```env
# TMDB API
VITE_TMDB_API_KEY=seu_bearer_token_aqui

# Appwrite
VITE_APPWRITE_PROJECT_ID=seu_project_id
VITE_APPWRITE_DATABASE_ID=seu_database_id
VITE_APPWRITE_COLLECTION_ID=seu_collection_id
```

4. **Configure o Appwrite**

Crie um database e collection com os seguintes atributos:

| Atributo    | Tipo    | Tamanho | Obrigatório | Default Value
|-------------|---------|---------|-------------|
| searchTerm  | String  | 1000     | ✅ Sim    |
| count       | Integer | -       | ❌ Não     |  1
| movie_id    | Integer | -       | ✅ Sim     |
| poster_url  | String  | -     | ✅ Sim       |

**Permissões**: Role `Any` com permissões de Read, Create, Update

5. **Execute o projeto**
```bash
npm run dev
```

Acesse: http://localhost:5173

## 🎨 Estrutura do Projeto

```
movie-search-app/
├── public/
│   ├── hero-img.png          # Banner principal
│   ├── hero-bg.png           # Background pattern
│   ├── search.svg            # Ícone de busca
│   ├── star.svg              # Ícone de estrela
│   └── No-Poster.png         # Placeholder
├── src/
│   ├── components/
│   │   ├── Search.jsx        # Input de busca
│   │   ├── Spinner.jsx       # Loading spinner
│   │   └── MovieCard.jsx     # Card de filme
│   ├── App.jsx               # Componente principal
│   ├── appwrite.js           # Config Appwrite
│   ├── index.css             # Estilos globais
│   └── main.jsx              # Entry point
├── .env                      # Variáveis de ambiente
├── .env.example              # Exemplo de variáveis
├── .gitignore
├── package.json
└── vite.config.js
```

## 🔑 Obtendo as API Keys

### TMDB API Key

1. Crie uma conta em https://www.themoviedb.org/
2. Vá em **Settings** → **API**
3. Solicite uma API Key (escolha Developer)
4. Copie o **API Read Access Token** (Bearer Token)
5. Cole no `.env` em `VITE_TMDB_API_KEY`

### Appwrite Setup

1. Crie uma conta em https://cloud.appwrite.io/
2. Crie um novo projeto
3. Crie um Database
4. Crie uma Collection com os atributos mencionados acima
5. Configure as permissões para `Any` (Read, Create, Update)
6. Copie os IDs para o `.env`

## 🛠️ Scripts Disponíveis

```bash
# Desenvolvimento
npm run dev

# Build para produção
npm run build

# Preview da build
npm run preview

# Lint
npm run lint
```




## 👨‍💻 Autor

**Isaias Lourenço da Costa**
- GitHub: [@Isaiaslc-dev](https://github.com/Isaiaslc-dev)
- LinkedIn: [Isaias Lourenço da Costa](www.linkedin.com/in/isaiascostadev)

## 🙏 Agradecimentos

- [TMDB](https://www.themoviedb.org/) pela API gratuita de filmes
- [Appwrite](https://appwrite.io/) pela plataforma BaaS
- [React](https://react.dev/) pela incrível biblioteca
- [Vite](https://vitejs.dev/) pelo build tool ultra-rápido
- [TailwindCSS](https://tailwindcss.com/) pelo framework CSS

## 📚 Documentação

- [TMDB API Docs](https://developer.themoviedb.org/docs)
- [Appwrite Docs](https://appwrite.io/docs)
- [React Docs](https://react.dev)
- [Vite Docs](https://vitejs.dev)
