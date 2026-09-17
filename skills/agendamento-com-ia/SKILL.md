---
name: agendamento-com-ia
description: Cria eventos na Google Agenda conectada a partir de um pedido em linguagem natural. Use when the user asks to schedule something, "marca uma reuniao com fulano amanha as 10", "agenda um compromisso", "bota isso na minha agenda".
---

# Agendamento com IA

Cria um evento na Google Agenda conectada a partir de um pedido em
linguagem natural, sempre confirmando antes de criar de verdade.

## Pre-voo (Google)

1. Confira se ha ferramenta de Google Calendar. Se nao: oriente
   Configuracoes → Conectores no site da conta, peca `pronto, conectei` e pare.
2. Se houver: avise sobre a tela de **Permitir** (leitura/escrita na
   agenda). Chame ferramentas de checagem na hora; se pedir autorizacao,
   reexecute imediatamente apos o Permitir.
3. A confirmacao do **preview do evento** (passo 4 abaixo) e separada da
   autorizacao Google — uma nao substitui a outra.

## Como fazer

1. Extraia do pedido: titulo, data, horario, duracao (assuma 1h se nao
   disser), e participantes (se mencionados).
2. Se faltar informacao critica (data ou horario ambiguo, por exemplo),
   pergunte antes de seguir — nao chute.
3. Se o horario pedido bater com outro compromisso existente, avise o
   conflito antes de criar (use a ferramenta de checagem/sugestao de
   horario da Agenda conectada, se disponivel).
4. **Mostre um preview** com titulo, data, horario e participantes, e
   pergunte "posso criar esse evento?" — so chame a ferramenta de criacao
   (`create_event` / equivalente disponivel) depois de confirmacao
   explicita ("sim", "pode", "confirma", etc).

## Regra

Nunca cria evento sem mostrar o preview e receber confirmacao explicita do
usuario. Se o usuario corrigir algo no preview, mostre a versao corrigida
de novo antes de criar.
