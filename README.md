
# Passo a Passo: Clonando Projeto Laravel com Autenticação e Mix

## 1. Clonar o Repositório
Se você já tem o repositório do Laravel hospedado, use o comando `git clone` para clonar o projeto:

```bash
git clone https://github.com/matheushsouto/Biblioteca
cd Biblioteca
```

## 2. Instalar Dependências do Laravel
Instale as dependências do PHP e do Laravel usando o Composer:

```bash
composer install
```

## 3. Configurar Variáveis de Ambiente
Crie o arquivo `.env`:

```bash
cp .env.example .env
```

Abra o arquivo `.env` e configure as variáveis do banco de dados e outras configurações conforme necessário.

Gere uma chave de aplicação:

```bash
php artisan key:generate
```

## 4. Instalar Dependências do Node.js
Laravel Mix é uma ferramenta para compilar assets front-end como CSS e JS. Primeiro, instale as dependências:

```bash
npm install
```

## 5. Compilar os Assets
Depois de instalar as dependências do Node.js, use o Laravel Mix para compilar os arquivos CSS e JS:

```bash
npm run dev
```

## 6. Rodar Migrações e Seeders
Execute as migrações para criar as tabelas no banco de dados:

```bash
php artisan migrate
```

Se o projeto já tiver seeders configurados:

```bash
php artisan db:seed
```

## 7. Instalar o Breeze para Autenticação

Instale o Breeze:

```bash
composer require laravel/breeze --dev
```

Instale os arquivos de autenticação:

```bash
php artisan breeze:install
```

Compile os assets de autenticação:

```bash
npm install && npm run dev
```

Rode novamente as migrações:

```bash
php artisan migrate
```

## 8. Rodar o Servidor
Para rodar o servidor local:

```bash
php artisan serve
```

Agora você pode acessar o projeto em `http://localhost:8000`.

---

**Resumo do Processo:**
1. Clonar o repositório.
2. Instalar dependências (Composer e NPM).
3. Configurar `.env` e gerar chave de aplicação.
4. Compilar assets com Laravel Mix.
5. Rodar migrações e seeders.
6. Instalar Breeze (se necessário).
7. Rodar o servidor.
