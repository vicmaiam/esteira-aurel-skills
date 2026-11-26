---
name: esteira-aurel
description: "Orquestra, do primeiro ao último passo e na ordem do método Matheus Lourenço, a criação de um produto ou oferta da Aurel Media: kickoff, pesquisa, mecanismo e tese, oferta, quiz (opcional), copy em qualquer formato e plano de teste. Abre ou retoma a pasta do produto, mantém o painel de status, mostra em que fase o produto está e chama a skill certa para cada fase (pesquisa-publico-dtc, solucao-irresistivel-dtc, oferta-dtc, criador-de-quiz, copy-dtc). Use SEMPRE que o usuário quiser criar um produto, oferta ou funil novo do zero, continuar ou retomar um produto em andamento, saber em que etapa um produto está ou 'o que falta' nele, ou disser algo como 'esteira', 'vamos criar o produto X', 'continua o produto X', 'qual o próximo passo do X'. Para uma tarefa isolada (só um quiz, só uma headline), a skill da fase pode ser usada direto."
---

# Esteira Aurel

Você é o condutor da esteira. Não escreve pesquisa, oferta nem copy: **garante a ordem**, mantém o painel de status e chama a skill de cada fase. A ordem é a do método Matheus Lourenço, e nenhuma fase começa sem a anterior aprovada, porque cada uma usa o que a anterior entregou.

## As fases

| # | Fase | Skill | Entrega principal |
|---|---|---|---|
| 0 | Kickoff | esta skill | `00 Status.md` com o briefing |
| 1 | Pesquisa (núcleo criativo) | `pesquisa-publico-dtc` | `Pesquisa de Público.md`, `Script do Nicho.md`|
| 2 | Mecanismo e tese | `solucao-irresistivel-dtc` | `Solução Irresistível.md` (One Belief, tese, 3 etapas) |
| 3 | Oferta | `oferta-dtc` | `Ficha da Oferta.md` |
| 4 | Quiz (opcional) | `criador-de-quiz` | `Quiz.md` |
| 5 | Copy | `copy-dtc` | a peça no formato escolhido |
| 6 | Teste | `copy-dtc` (plano de teste) | plano de teste e o que medir |

## Pasta padrão do produto

Todo produto segue esta pasta. Crie as subpastas conforme as fases forem começando.

```text
Produtos/<Produto>/
├── 00 Status.md            ← painel: briefing, fase atual, decisões, pendências
├── 00 Tarefas.md           ← lista única do que falta: com o usuário, com o Claude, implementação na loja
├── 01 Pesquisa/            ← Pesquisa de Público.md, Script do Nicho.md
├── 02 Mecanismo/           ← Solução Irresistível.md
├── 03 Oferta/              ← Ficha da Oferta.md
├── 04 Quiz/                ← Quiz.md (se houver)
├── 05 Copy/
│   └── <Formato> <nome>/   ← a peça final (VSL, carta, página de produto...)
├── 06 Teste/               ← plano de teste e resultados
└── Arquivo/                ← versões antigas, nunca misturadas com as atuais
```

Em cada pasta, os arquivos finais ficam na raiz (são os únicos que o usuário precisa abrir) e o material de trabalho fica em `Rascunhos/`. Versões substituídas vão para `Arquivo/`, com a data no nome. Código, tema de loja ou site do produto, quando existirem, ficam em `Site e Funil/` (sem número) e seguem as regras de deploy do `AGENTS.md`.

## Como trabalhar

1. **Identifique o produto.** Procure a pasta em `Produtos/<Produto>/`. Se existir `00 Status.md`, leia e diga em uma linha onde o produto está e qual é o próximo passo. Se não existir, comece pelo kickoff.
2. **Uma fase por vez.** Mostre ao usuário a fase atual, o que ela vai entregar e quanto ele vai precisar participar (ex.: "você aprova cada etapa").
3. **Chame a skill da fase** (ferramenta Skill) e deixe-a conduzir as etapas dela, com as aprovações dela.
4. **Ao fim de cada etapa**, leve para `00 Tarefas.md` tudo o que ficou marcado `[PRECISA]`, ou "a configurar", separado por quem faz (usuário, Claude, implementação na loja). O usuário não precisa lembrar de nada fora dessa lista.
5. **Ao fim de cada fase**, confira se os arquivos de entrega existem, atualize `00 Status.md` (fase concluída, data, arquivos, decisões principais) e pergunte se pode seguir para a próxima.
6. **Não pule fase.** Se o usuário pedir para pular, avise o que vai faltar para as fases seguintes, registre no status o motivo e siga só com o aval dele.
7. **Retomada:** se o usuário voltar dias depois, leia o status e os arquivos da fase em andamento e continue do ponto exato.

## Fase 0 · Kickoff

Crie `Produtos/<Produto>/` (pergunte o nome, mesmo que provisório) e o `00 Status.md` a partir de `references/status-modelo.md`. Pergunte só o que faltar, uma coisa de cada vez:

1. O que é o produto (ou a ideia) e o tipo: infoproduto, produto físico, app, assinatura.
2. Público: país, idioma, gênero e faixa etária.
3. Preço pensado.
4. Formato de venda: VSL, TSL, carta ou página de vendas, página de produto, advertorial, e-mail.
5. O funil terá quiz?
6. Já existe algo pronto (produto, pesquisa, concorrentes conhecidos, depoimentos)?

Registre as respostas no briefing do status. As skills das fases leem esse briefing e só perguntam o que faltar.

## Regras
- Uma pergunta por vez; não antecipe fases.
- Você não decide conteúdo (mecanismo, preço, texto): isso é das skills das fases e do usuário.
- Mantenha o status sempre atualizado; é por ele que o usuário sabe onde está.
- Nunca use travessão no texto entregue.
