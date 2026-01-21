# n8n-ai-news-curator

# 📰 Daily AI News Digest (n8n + Gemini)

Automação criada com **n8n** que coleta notícias via **RSS do portal G1 (Economia e Tecnologia)**, utiliza a **IA Gemini (Google)** para selecionar e resumir as notícias mais relevantes e envia automaticamente um **resumo diário por e-mail**, todos os dias às **06:00 da manhã**.

Projeto focado em **produtividade, curadoria de informação e uso prático de IA em automações reais**.


## 🚀 Funcionalidades

- ⏰ Execução automática diária via **Schedule Trigger**
- 🌐 Coleta de notícias via **RSS Feed**
- 🧠 Curadoria inteligente com **Gemini (LLM)**
- ✂️ Seleção automática das notícias mais relevantes
- 📝 Resumos curtos e objetivos (até 50 palavras)
- 📬 Envio automático para o **Gmail**
- 📊 Organização em **Tech** e **Economia**
- 📄 Formatação em **Markdown**, pronta para leitura no e-mail


## 🛠️ Tecnologias Utilizadas

- **n8n** – Plataforma de automação low-code
- **Google Gemini API** – Processamento e resumo das notícias
- **RSS Feed (G1 Globo)** – Fonte de dados
- **Gmail API** – Envio automático de e-mails
- **Markdown** – Formatação do resumo diário


## 🔄 Fluxo da Automação

1. **Schedule Trigger**
   - Dispara diariamente às 06:02

2. **RSS Read**
   - Economia: `https://g1.globo.com/rss/g1/economia/`
   - Tecnologia/Carros: `https://g1.globo.com/rss/g1/carros/`

3. **Limit**
   - Limita a quantidade de notícias analisadas

4. **Merge + Split Out**
   - Une os feeds e prepara os dados (título, conteúdo e link)

5. **Aggregate**
   - Consolida todas as notícias em um único payload

6. **Gemini (LLM)**
   - Analisa as notícias
   - Seleciona no máximo **3 mais relevantes**
   - Gera um resumo estruturado em Markdown

7. **Gmail**
   - Envia automaticamente o resumo diário para o e-mail configurado

## 🧠 Prompt Utilizado na IA

A IA é instruída a atuar como um **editor de notícias especializado em tecnologia e economia**, com regras claras:

- Selecionar apenas notícias relevantes
- Limitar o resumo a 50 palavras por notícia
- Separar em seções: **Tech** e **Economia**
- Gerar saída pronta para e-mail em **Markdown**
- Incluir links diretos para as notícias originais


## 📅 Exemplo de Assunto do E-mail

