---
name: agendamento-com-claude
description: Cria eventos na Google Agenda conectada a partir de um pedido em linguagem natural. Use when the user asks to schedule something, "marca uma reuniao com fulano amanha as 10", "agenda um compromisso", "bota isso na minha agenda".
---

# Agendamento com Claude

Cria um evento na Google Agenda conectada a partir de um pedido em
linguagem natural, sempre confirmando antes de criar de verdade.

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
