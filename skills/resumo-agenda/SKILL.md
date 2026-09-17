---
name: resumo-agenda
description: Resume os compromissos do dia ou da semana na Google Agenda conectada. Use when the user asks about their schedule, "o que eu tenho hoje", "minha agenda da semana", "tenho reuniao hoje?".
---

# Resumo de agenda

Le a Google Agenda conectada e devolve um resumo cronologico dos
compromissos do periodo pedido (hoje, por padrao).

## Como fazer

1. Se o usuario nao especificar o periodo, assuma "hoje". Se pedir
   "semana", cubra de hoje ate domingo.
2. Use a ferramenta de listagem de eventos da Agenda conectada
   (`list_events` / equivalente disponivel) pro periodo certo.
3. Liste em ordem cronologica: horario, titulo do compromisso, e
   participantes (se houver). Se um evento tiver link de reuniao, inclua.
4. Se o dia/semana estiver vazio, diga isso claramente — nao invente
   compromisso nenhum.

## Regra

So le e mostra. Nao cria, edita nem cancela nada aqui — isso e a skill
`agendamento-com-claude`.
