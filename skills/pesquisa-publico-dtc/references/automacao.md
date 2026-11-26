# Automação da coleta

O objetivo é o Claude fazer sozinho quase toda a coleta, com o usuário só aprovando o resultado de cada etapa.

## Navegador
- Use o Claude in Chrome (carregue de uma vez as ferramentas de abas, navegar, ler página, javascript e computer). Trabalhe em abas novas, feche as abas ao terminar.
- Para ler muito texto, prefira `get_page_text` ou JavaScript que monta o texto e devolve em partes. Screenshot só quando precisar ver layout.
- Se a página exigir login, CAPTCHA ou bloquear, peça ao usuário para desbloquear.

## Receitas que funcionam
- **Transcrição de vídeo do YouTube** (para modelar leads e estudar VSLs publicadas): abra o vídeo, expanda a descrição, clique em "Mostrar transcrição" e leia o painel de transcrição. Se o texto for longo, cole num elemento da página e leia com `get_page_text` em partes.
- **Comentários do YouTube:** abra o vídeo, role a página algumas vezes para carregar os comentários e extraia com JavaScript os textos e as curtidas dos comentários; ordene pelos mais curtidos.
- **Vídeos mais vistos:** busque o termo no YouTube e aplique o filtro de ordenação por visualizações antes de escolher os vídeos.
- **Google ABC:** abra o Google, digite o termo seguido de cada letra e leia as sugestões do autocompletar. Faça em lote, de "a" a "z".
- **Google Trends:** abra a comparação dos termos achados (até 5 por vez) no país do público e leia o interesse relativo e as pesquisas relacionadas.
- **Biblioteca de Anúncios:** use a skill `facebook-ad-library` (busca por palavra-chave, anúncios ativos, data de início). Abra a página de destino dos mais antigos e com mais variações.
- **Páginas de venda e VSLs concorrentes:** leia o texto da página. Se a VSL estiver no YouTube, use a transcrição. Se estiver num player fechado (VTurb e similares) e não houver transcrição, registre o que a página mostra e peça ao usuário um resumo ou uma gravação, se ele quiser.
- **Amazon:** abra a busca do tema ordenada por mais vendidos; leia sinopse e avaliações dos 3 a 5 primeiros livros.
- **Reddit e fóruns:** busque o tema com "site:reddit.com" no Google e abra os tópicos com mais respostas.

## Coleta em paralelo
Quando houver várias fontes, divida a coleta entre subagentes (ferramenta Agent), um por fonte ou grupo de fontes: por exemplo, um para YouTube, um para Reddit e fóruns, um para Amazon e Google, um para os concorrentes. Cada subagente recebe o briefing, as regras de coleta (`fontes.md`) e o caminho do arquivo onde deve salvar os trechos literais com o link. Depois você junta tudo no `03-brainstorm.md` e revisa. Não deixe dois subagentes escreverem no mesmo arquivo.

## Organização automática
- Salve sempre o material bruto (trechos com link) antes de analisar. A análise vem depois, em arquivo separado.
- Ao final de cada etapa, atualize o resumo no topo do arquivo da etapa: quantos trechos, de quais fontes, o que ficou de fora.
