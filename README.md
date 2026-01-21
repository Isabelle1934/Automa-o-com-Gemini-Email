# n8n-ai-news-curator

📰 **Daily AI News Digest (n8n + Gemini)**

Automação desenvolvida com **n8n** que coleta notícias via **RSS do portal G1**, processa o conteúdo com a **IA Gemini (Google)** para selecionar e resumir as notícias mais relevantes de **tecnologia e economia**, e envia automaticamente um **resumo diário por e-mail** às **06:00 da manhã**.

Projeto focado em **produtividade, curadoria inteligente de informações e aplicação prática de IA em automações reais**.

---

## 🚀 Funcionalidades

- ⏰ Execução automática diária via **Schedule Trigger**
- 🌐 Coleta de notícias por **RSS Feed**
- 🧠 Análise e curadoria com **Gemini (LLM)**
- ✂️ Seleção das notícias mais relevantes
- 📝 Resumos objetivos com limite de 50 palavras
- 📊 Organização por categorias: **Tech** e **Economia**
- 📄 Formatação em **Markdown**, otimizada para e-mail
- 📬 Envio automático via **Gmail**

---

## 🛠️ Tecnologias Utilizadas

- **n8n** – Plataforma de automação low-code
- **Google Gemini API** – Processamento e resumo de conteúdo
- **RSS Feed (G1 Globo)** – Fonte das notícias
- **Gmail API** – Envio de e-mails
- **Markdown** – Estruturação do conteúdo

---

## 🔄 Fluxo da Automação

1. **Schedule Trigger**  
   Executa o fluxo diariamente às 06:02.

2. **RSS Read**  
   Coleta notícias dos feeds:
   - Economia: `https://g1.globo.com/rss/g1/economia/`
   - Tecnologia: `https://g1.globo.com/rss/g1/carros/`

3. **Limit**  
   Restringe a quantidade de notícias processadas.

4. **Merge + Split Out**  
   Unifica os feeds e extrai título, conteúdo e link.

5. **Aggregate**  
   Consolida todas as notícias em um único payload.

6. **Gemini (LLM)**  
   Analisa o conteúdo, seleciona até **3 notícias relevantes** e gera um resumo estruturado em **Markdown**.

7. **Gmail**  
   Envia automaticamente o resumo diário para o e-mail configurado.

---

## 🧠 Estratégia de Prompt

A IA atua como um **editor especializado em tecnologia e economia**, seguindo as diretrizes:

- Priorizar apenas notícias relevantes
- Limitar os resumos a 50 palavras
- Separar o conteúdo em **Tech** e **Economia**
- Gerar saída pronta para leitura em e-mail
- Incluir links diretos para as fontes originais

---

## 📌 Objetivo do Projeto

- Demonstrar o uso de **IA aplicada à automação**
- Integrar **LLMs em fluxos reais**
- Criar uma solução reutilizável e escalável
- Compor um **projeto de portfólio** em automação, IA e engenharia de software

---

## ⚠️ Observações

- As credenciais da **Google Gemini API** e do **Gmail** não estão incluídas no repositório.
- É necessário configurar:
  - Google Gemini API
  - OAuth do Gmail
- O fluxo pode ser adaptado para:
  - Outras fontes RSS
  - Diferentes horários de execução
  - Integrações com Slack, WhatsApp ou Telegram

---

## 📄 Licença

Projeto de uso educacional, com livre adaptação.

