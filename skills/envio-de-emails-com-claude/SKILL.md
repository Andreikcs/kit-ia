---
name: envio-de-emails-com-claude
description: Redige e envia e-mails pelo Gmail conectado, sempre mostrando o rascunho e pedindo confirmacao antes de enviar. Use when the user asks to send or reply to an email, "manda um e-mail pra fulano", "responde esse e-mail", "escreve e envia um e-mail sobre X".
---

# Envio de e-mails com Claude

Redige um e-mail (novo ou resposta) a partir do pedido do usuario e so
envia depois de confirmacao explicita — nunca envia direto.

## Pre-voo (Google)

1. Confira se ha ferramenta de Gmail. Se nao: oriente Conectores no
   claude.ai, peca `pronto, conectei` e pare.
2. Se houver: avise sobre a tela de **Permitir**. Se a autorizacao for
   pedida ao enviar, reexecute o envio **imediatamente** apos o Permitir
   — sem pedir o texto do e-mail de novo.
3. O preview do rascunho (abaixo) e obrigatorio e e independente da
   autorizacao Google.

## Como fazer

1. Identifique destinatario, assunto e o conteudo/intencao do e-mail (ou,
   se for resposta, a thread original).
2. Redija o e-mail completo: assunto e corpo, em tom adequado ao pedido
   (formal, casual, etc — pergunte se nao estiver claro).
3. **Mostre o rascunho inteiro** pro usuario: destinatario, assunto e
   corpo completo.
4. Pergunte "posso enviar assim?" — se o usuario pedir ajuste, reescreva e
   mostre de novo. So chame a ferramenta de envio do Gmail conectado
   (`send_message` / `reply` / equivalente disponivel) depois de
   confirmacao explicita.

## Regra

Nunca envia e-mail sem mostrar o rascunho completo e receber confirmacao
explicita do usuario nesta mesma conversa. Sem excecao, mesmo se o pedido
parecer simples ("manda um oi pra ela") — o preview e obrigatorio.
