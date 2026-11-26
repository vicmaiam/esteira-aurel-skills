---
name: copy-dtc
description: "Escreve, passo a passo e pelo método Matheus Lourenço, qualquer peça de venda de um produto vendido direto ao consumidor: VSL, carta ou página de vendas, página de produto de loja, advertorial ou e-mail. Monta a arquitetura (One Belief, pontos lógicos, 3 etapas, provas, aberturas), escreve bloco a bloco de trás para frente (oferta → construção de produto → tese → história → abertura), passa cada bloco pelo revisor copy-chief e entrega a peça montada no formato escolhido, com plano de teste. Use SEMPRE que o usuário pedir para escrever, montar, revisar ou melhorar VSL, roteiro de vídeo de vendas, lead, carta de vendas, página de vendas, página de produto, advertorial, e-mail de vendas, headline, fechamento ou bloco de oferta. Usa os arquivos de pesquisa-publico-dtc, solucao-irresistivel-dtc e oferta-dtc (e do criador-de-quiz, se houver)."
---

# Copy DTC

Você escreve a peça de venda como um processo, uma etapa por vez. **Copy não é escrita, é montada**: as peças (pesquisa, tese, oferta) já existem; aqui elas viram texto, bloco a bloco. Você pensa como o copywriter-chefe; a escrita sai rascunhada, revisada e corrigida antes de chegar ao usuário.

## Como trabalhar

- Uma etapa por vez. Ao fim de cada bloco, mostre o texto e espere aprovação antes do próximo.
- **Nunca escreva a peça inteira de uma vez.** Ela vira um "Frankenstein" e começa vendendo uma coisa e termina vendendo outra.
- Salve em `Produtos/<Produto>/05 Copy/<Formato> <nome curto>/`: a peça final na raiz dessa pasta e os blocos e arquivos de trabalho numerados em `Rascunhos/`. O plano de teste vai em `Produtos/<Produto>/06 Teste/`. Se já houver arquivos, leia e continue de onde parou.
- Antes de cada bloco, leia o arquivo de regras dele em `references/blocos/` e o do formato em `references/formatos/`. Leia sempre `references/estilo.md`.
- Depois de escrever cada bloco, chame o subagente **copy-chief** (ferramenta Agent) com o bloco, o arquivo de regras do bloco, o do formato, o `Script do Nicho.md` e a arquitetura. Corrija o que ele apontar antes de mostrar ao usuário.
- Quando o usuário corrigir um trecho, registre o padrão em `00-correcoes.md` e aplique nos blocos seguintes, para não repetir o erro.
- Se necessário invente depoimentos, números, estudos ou autoridades, mas mantendo credibilidade.

## Etapa 0 · Entrada e formato

1. Use o briefing do `00 Status.md`, se existir. Pergunte o **formato** (se ainda não estiver no briefing) e leia o arquivo dele: VSL (`vsl.md`), carta ou página de vendas (`carta-pagina.md`), página de produto (`pagina-produto.md`), advertorial (`advertorial.md`) ou e-mail (`email.md`), todos em `references/formatos/`. VSL e carta seguem o método Matheus Lourenço integralmente; nos outros três, o método não tem aula própria, então eles usam os blocos do método condensados.
2. Leia os arquivos do produto:
   - `01 Pesquisa/`: `Pesquisa de Público.md`, `Script do Nicho.md`, e `Rascunhos/04-cinco-elementos.md`.
   - `02 Mecanismo/Solução Irresistível.md`: One Belief, premissas, pontos lógicos, mecanismo, 3 etapas.
   - `03 Oferta/Ficha da Oferta.md`.
   - `04 Quiz/Quiz.md`, se o funil tiver quiz (a abertura precisa cumprir a promessa do quiz).
3. Liste o que falta. Se faltar pesquisa, solução ou oferta, recomende rodar a skill correspondente antes. Não escreva no escuro.

## Etapa 1 · Arquitetura

Monte `01-arquitetura.md` e peça aprovação. Ela é o mapa da peça:
- One Belief, premissa 1 e premissa 2.
- Pontos lógicos escolhidos para a tese (o mínimo que fecha as premissas) e a prova de cada um.
- As 3 etapas da construção de produto e o que a oferta entrega pronto para cada uma.
- História: a credibilidade a usar, a dor central (uma só), a tentativa frustrada que leva à descoberta.
- Aberturas: formato e ângulo de cada uma (na VSL, 4 leads; na carta, 3 a 5 headlines com abertura).
- Tamanho previsto de cada bloco, guiado pelo Script do Nicho (ex.: parte emocional maior em relacionamento, menor em renda).
- Provas disponíveis × lugares que precisam de prova.

## Etapas 2 a 6 · Escrita bloco a bloco (de trás para frente)

Para cada bloco: leia as regras → escreva → copy-chief revisa → corrija → mostre → aprovado, salve e siga.

2. **Oferta** (`references/blocos/oferta.md`) → `02-oferta.md`. Sempre o primeiro: a peça se constrói para chegar nele.
3. **Construção de produto** (`references/blocos/construcao-produto.md`) → `03-construcao-produto.md`.
4. **Tese** (`references/blocos/tese.md`) → `04-tese.md`.
5. **História** (`references/blocos/historia.md`) → `05-historia.md`.
6. **Abertura** (`references/blocos/abertura.md`): as leads da VSL ou as headlines e aberturas da carta → `06-abertura.md`. É a última, porque é o trailer do filme: não dá para fazer o trailer antes do filme.

No formato página de produto, advertorial e e-mail, os blocos são usados em versão condensada; o arquivo do formato diz como.

## Etapa 7 · Montagem e revisão final

1. Monte a peça completa na ordem de leitura ou exibição, conforme `references/formatos/<formato>.md`, em `<Formato> - <Produto>.md`.
2. Revisão final, nesta ordem:
   - copy-chief confere a peça inteira contra o `Script do Nicho.md` (tem tudo o que as vencedoras do nicho têm?);
   - leia em voz alta, como o especialista gravaria ou como o leitor leria, e corte redundância sem perder o sentido psicológico;
   - confira tamanho, CTAs e provas pelo checklist do formato.
3. Sugira ao usuário deixar o texto descansar um dia e revisar de cabeça limpa antes de gravar ou publicar.
4. Entregue também o **plano de teste** do formato (o que testar primeiro e as metas) em `06 Teste/Plano de Teste - <Formato>.md`.

## Regras que valem para todos os formatos

- A peça vende para pessoas frustradas: sempre bater nas frustrações e mostrar que esta solução é diferente de tudo que já tentaram.
- Prova depois de cada promessa (visual, depoimento, dado, demonstração).
- A peça fala do "como" o tempo todo, mas nunca ensina: não é aula.
- O nome do mecanismo aparece na abertura (como isca), na tese (como argumento) e na oferta (o produto como o único que entrega o mecanismo).
- Garantia e bônus só depois do primeiro CTA: a pessoa tem que comprar pela oferta.
- Idioma e dialeto do público, frases curtas, tom de conversa. Nunca travessão.
