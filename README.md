# TikTok Hub

Painel completo para gerenciar sua operação no TikTok Shop — tudo em um único arquivo HTML, sem instalação.

## Funcionalidades

- **Organizador de Prompts** — salve e acesse seus prompts de IA favoritos
- **Controle Financeiro** — registre entradas e custos, com suporte a custos fixos mensais automáticos e gráfico de desempenho
- **Calculadora de Backlog** — calcule o backlog de produção por produto, formato e cenas
- **Sincronização em nuvem** — dados salvos automaticamente via Firebase Realtime Database

## Como usar

1. Baixe o arquivo `tiktokhub.html`
2. Abra no navegador (duplo clique)
3. Pronto — todos os dados são salvos localmente e sincronizados na nuvem se o Firebase estiver configurado

## Configurar o Firebase (sincronização entre computadores)

1. Acesse [console.firebase.google.com](https://console.firebase.google.com) e crie um projeto gratuito
2. Vá em **Realtime Database** → Criar banco de dados → Modo de teste
3. Clique em **Configurações do projeto** → **Seus apps** → Adicionar app Web
4. Copie o objeto `firebaseConfig`
5. No `tiktokhub.html`, localize o trecho:
   ```js
   const firebaseConfig = { ... }
   ```
   e substitua pelos seus dados

Após isso, todos os dados sincronizam automaticamente entre dispositivos.

## Tecnologias

- HTML + CSS + JavaScript puro (sem frameworks)
- Firebase Realtime Database (opcional, para sincronização)
