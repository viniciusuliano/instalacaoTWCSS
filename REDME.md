# GUIA DE INSTALAÇÃO TAILWIND CSS
# WARING - NECESSARIO NODE.JS

## PASSO A PASSO

- PASSO 1: No terminal do VScode - npm install -D tailwindcss postcss autoprefixer // Instala todos os pacotes

- PASSO 2: npx tailwindcss init -> //Inicia o Tailwind criando um arquivo tailwind.config.js

- PASSO 3: Inserir esse comando no tailwind.config.js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}

- PASSO 4: Criar pasta .src/tailwind.css (input) e dentro de /src criar uma pasta css com o arquivo styles.css(output)

- PASSO 5: Dentro do Package JSON inserir script de automatização para iniciar o Tailwind
{
  "devDependencies": {
    "autoprefixer": "^10.4.18",
    "postcss": "^8.4.35",
    "tailwindcss": "^3.4.1"
  },
  "scripts": {
    "dev": "npx tailwindcss -i ./src/tailwind.css -o ./src/css/styles.css --watch" // esse comando automatiza a inicialização do Tailwind e faz o direcionamento de pastas
  }
}

- PASSO 6: npm run dev