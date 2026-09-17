---
name: ler-emails
description: Lista e le e-mails recentes do Gmail conectado (nao lidos, de um remetente, de hoje, etc). Use when the user asks to check inbox, "o que chegou no e-mail", "tem e-mail novo", "e-mails de hoje", "e-mails nao lidos".
---

# Ler e-mails

Le a caixa de entrada do Gmail conectado a esta conta e mostra os
e-mails relevantes de forma resumida e facil de escanear.

## Pre-voo (Google)

1. Confira se ha ferramenta de Gmail nesta sessao.
2. Se nao houver: oriente Configuracoes → Conectores → Gmail no site da
   conta, peca `pronto, conectei` e pare. Nao invente e-mail.
3. Se houver: avise que pode abrir tela de autorizacao da Google — a pessoa
   deve clicar em **Permitir**. Em seguida chame a ferramenta **na hora**.
4. Se falhar por falta de autorizacao: espere o Permitir e **reexecute a
   mesma chamada imediatamente**.

## Como fazer

1. Se o pedido nao disser o filtro, pergunte rapido: nao lidos, de hoje, ou
   de uma pessoa/assunto especifico?
2. Use a ferramenta de busca do Gmail conectado (`search_threads` /
   `list_message` / equivalente disponivel) com o filtro certo.
3. Para cada e-mail relevante, mostre: remetente, assunto, um resumo de uma
   linha do conteudo, e se esta lido ou nao.
4. Ordene do mais recente pro mais antigo. Nao mostre mais que 15 por vez —
   se tiver mais, diga quantos tem no total e pergunte se quer ver o resto.

## Regra

Nunca abra/marque como lido ou apague nada sem o usuario pedir
explicitamente — essa skill so **le e mostra**, nao executa acoes.

## Se o Gmail nao estiver conectado

Siga o Pre-voo. Nunca simule conteudo de e-mail.
