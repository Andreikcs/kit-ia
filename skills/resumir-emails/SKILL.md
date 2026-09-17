---
name: resumir-emails
description: Resume o conteudo de um e-mail especifico ou de uma thread inteira do Gmail conectado. Use when the user asks to summarize an email, "resume esse e-mail", "do que se trata essa thread", "me explica esse e-mail rapido".
---

# Resumir e-mails

Pega um e-mail ou thread do Gmail conectado e devolve um resumo curto,
direto ao ponto.

## Como fazer

1. Identifique qual e-mail/thread o usuario quer resumir (pelo assunto,
   remetente, ou se ele ja esta olhando um resultado de `ler-emails`).
2. Busque o conteudo completo da thread com a ferramenta do Gmail
   conectado (`get_thread` / `get_message` / equivalente disponivel).
3. Devolva um resumo em ate 5 linhas com este formato:
   - **De/Assunto:** quem mandou e sobre o que e
   - **Resumo:** os pontos principais, sem enrolacao
   - **Acao esperada:** o que a pessoa precisa fazer (responder, aprovar,
     nada) — se nao houver acao clara, diga "sem acao pendente"

## Regra

Se a thread tiver varias mensagens, resuma a conversa inteira (nao so a
ultima mensagem) — inclua se houve mudanca de assunto ou decisao no meio.
