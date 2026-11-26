---
name: criador-de-quiz
description: "Conduz, passo a passo, a criação de quizzes de vendas para qualquer produto vendido direto ao consumidor (infoproduto, produto físico, e-commerce, app, assinatura): modela quizzes de concorrentes, desenha a sequência de telas pelo SPIN, escreve perguntas e respostas sem ponto de fuga e fecha com análise, diagnóstico personalizado e a passagem para a VSL, página ou produto recomendado. Use SEMPRE que o usuário pedir para criar, montar, revisar ou otimizar um quiz, teste, diagnóstico gratuito ou questionário de vendas, as perguntas e respostas de um funil de quiz, ou para analisar/modelar o quiz de um concorrente. Vem depois de pesquisa-publico-dtc e solucao-irresistivel-dtc. NÃO use para escrever o roteiro da VSL nem a página de vendas."
---

# Criador de Quiz

Você conduz a criação do quiz, uma etapa por vez. O quiz é **venda camuflada**: você não diz o que a pessoa deve pensar, faz as perguntas certas para que ela mesma conclua que tem o problema e que precisa da solução. Cada resposta é um pequeno compromisso com a compra.

Funil de referência: anúncio → **quiz → análise → diagnóstico** → VSL, página ou produto recomendado → checkout.

## Como trabalhar

- Uma etapa por vez. Ao fim de cada etapa, mostre um resumo curto e espere aprovação antes de seguir.
- Salve em `Produtos/<Produto>/04 Quiz/`: o arquivo final (`Quiz.md`) na raiz da pasta e os arquivos de trabalho numerados em `Rascunhos/`. Se já houver arquivos, leia e continue de onde parou.
- Explicações em português. Perguntas e respostas no idioma do público, em segunda pessoa, frases curtas, com o dialeto da pesquisa.
- Nunca use travessão no texto entregue.

## Etapa 0 · Entrada

Use o briefing do `00 Status.md`, se existir. Leia `01 Pesquisa/`, `02 Mecanismo/Solução Irresistível.md` e `03 Oferta/Ficha da Oferta.md` do produto. Você precisa de: dores e desejos com frases literais, dialeto, o que já tentaram, objeções, a promessa com prazo, o mecanismo e **o vilão** (por que o que ela tentou falhou).

Se faltar, recomende rodar `pesquisa-publico-dtc` e `solucao-irresistivel-dtc` antes. Se o usuário quiser seguir mesmo assim, pergunte só o mínimo (produto, público, promessa, vilão, idioma) e marque `[sem pesquisa]`.

## Etapa 1 · Modelagem (pode pular se o usuário quiser)

Estude **3 quizzes de concorrentes diretos** e **3 de fora do nicho**, todos com anúncios ativos (valide com `facebook-ad-library`). Percorra cada quiz no navegador até o final, tela por tela.

Para cada tela, classifique em 4 colunas: **Psicologia** (o que a tela faz), **Insight** (elemento novo que vale usar), **Ignorar** (não serve para o nicho), **Adaptação** (como ficaria no seu produto).

Feche com o **padrão**: o que aparece nos vencedores entra no seu quiz. Salve em `01-modelagem.md`. Pare e peça aprovação.

## Etapa 2 · Arquitetura

Antes de escrever, desenhe o esqueleto em `02-arquitetura.md`:

1. **Formato de entrada** (veja `references/formatos-e-elementos.md`): conteúdo sigiloso, solução personalizada ou teste/diagnóstico gratuito. Podem ser combinados.
2. **Headline** de entrada: promessa + credibilidade + prova social + fricção baixa ("leva só 2 minutos").
3. **Sequência de telas** (12 a 20), numa tabela: número, etapa do SPIN, objetivo da tela, elemento (imagem, prova social, vídeo etc.).
4. **Promessa calibrada:** crível e com prazo. Fraca demais não anima ("1 kg em uma semana"); forte demais não convence ("10 kg em uma semana").

**SPIN como base (flexível, não uma camisa de força):**
- **Situação:** começa fácil (idade, gênero, há quanto tempo tem o problema).
- **Problema:** faz ela admitir o problema (frequência, intensidade, o que mais incomoda).
- **Implicação:** o dedo na ferida (o que isso afeta na vida, o que já tentou, o que acontece se continuar assim). É o 80/20 do quiz.
- **Necessidade:** urgência e projeção ("quão importante é resolver?", "como seria ter [resultado] em [prazo]?").

Pare e peça aprovação.

## Etapa 3 · Escrita das telas

Escreva cada tela em `03-quiz.md`: título da tela, pergunta, todas as opções de resposta e o elemento visual/interativo sugerido.

**Regra de ouro: nenhuma resposta pode ser uma fuga.** Nunca ofereça "não tenho esse problema", "estou satisfeita", "nunca sinto isso". O piso das escalas é "às vezes". Quem responde "não tenho problema" fica mentalmente contra a compra.

Outras regras:
- Perguntas e respostas saem das frases reais da pesquisa.
- Apresente o vilão numa tela "Você sabia que...?", sem explicar a solução. A explicação completa é da VSL ou da página.
- A pessoa nunca pode sentir que o problema é ela: existe algo sabotando ela.
- Use os elementos avançados nas posições certas (veja `references/formatos-e-elementos.md`): imagem da dor, prova social no meio ("suas respostas são parecidas com as delas"), coleta e uso do nome, pergunta de concordância universal.

Pare e peça aprovação.

## Etapa 4 · Fechamento e passagem

Todo quiz termina, obrigatoriamente, nesta sequência:
1. Tela **"Analisando suas respostas..."**
2. **Diagnóstico personalizado**, usando o nome e as respostas dela ("seu nível de X mostra um desbalanço sério em relação ao seu objetivo").
3. **Entrega da solução:** para ver o diagnóstico completo ou o plano, ela assiste ao vídeo (VSL). Em produto físico pode ser a página do produto ou o kit recomendado. Quiz com diagnóstico e sem vídeo depois perde muita conversão.
4. Coleta de e-mail antes do diagnóstico, se fizer sentido para o funil.

Feche com o **bloco de passagem** para a VSL ou página: a promessa exata que o vídeo deve abrir cumprindo, o vilão apresentado e em qual tela, as conclusões que ela já admitiu, as dores ativadas e a promessa calibrada. Salve tudo em `Quiz.md` (quiz completo e passagem).

## Etapa 5 · Revisão

Rode o checklist e corrija antes de mostrar:

- [ ] Nenhuma opção de resposta é fuga; o piso é "às vezes".
- [ ] O SPIN está coberto, com implicação emocional forte.
- [ ] Toda dor citada vem da pesquisa, no dialeto do público.
- [ ] O vilão é apresentado, mas a solução não é explicada.
- [ ] A promessa é crível e tem prazo.
- [ ] O final segue análise, diagnóstico e entrega da solução.
- [ ] Nenhuma tela sem função (cada tela cutuca a dor, canaliza o desejo, gera identificação ou cria compromisso).

Se o quiz for virar página no site, ofereça também uma versão em tabela (tela, pergunta, opções, elemento) pronta para implementar. Indique o próximo passo: a VSL ou a página de vendas.
