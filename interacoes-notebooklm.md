# Registro de Interações — NotebookLM

Este arquivo documenta as perguntas feitas ao NotebookLM e as respostas obtidas ao longo do processo de teste e refinamento de prompts, como evidência do trabalho de engenharia de prompts descrito no [README](./README.md).

> Todas as respostas abaixo foram geradas pelo NotebookLM a partir das fontes carregadas no notebook (ver seção "Curadoria de Fontes" no README), sempre a partir do prompt base de persona (consultora de moda modesta).

---

## 1. Look para escritório

**Prompt:** `Monte um look para trabalhar em um escritório.`

**Resposta:**

Para um ambiente de escritório, o objetivo principal é comunicar credibilidade e profissionalismo, com peças estruturadas que confiram autoridade.

**Opção 1 — O Clássico Corporativo (foco em autoridade):** blazer preto ou azul-marinho estruturado, camisa branca de botão (algodão ou seda) e saia midi de alfaiataria em tom neutro, com mule ou sapatilha de bico fino. O caimento estruturado e os cortes retos transmitem seriedade; o blazer cria linhas verticais que alongam a silhueta sem marcar o corpo.

**Opção 2 — Elegância Suave (foco em acessibilidade):** blazer bege/fendi, blusa em cor suave (azul-claro ou lavanda) e saia midi evasê ou plissada em tom marinho/terroso, com sapatilha neutra. Cores análogas e tons claros transmitem harmonia e tornam o visual mais acessível, sem perder profissionalismo.

**Princípios aplicados:** regra de proporção 1/3–2/3 (cintura marcada para alongar a silhueta), tecidos de alfaiataria/linho/sarja que não marcam o corpo, 75% de cores neutras no guarda-roupa, e acessórios discretos (relógio, lenço de seda) como alternativa ao uso de joias.

**Perguntas de continuidade sugeridas pela IA:** quais acessórios usar sem joias; como identificar o tipo de corpo; quais são as 15 peças-chave de um guarda-roupa inteligente.

---

## 2. Mala cápsula com 20 peças

**Prompt:** `Monte uma mala cápsula com 20 peças.`

**Resposta (resumo):**

A mala foi organizada em categorias, seguindo a regra de 75% cores neutras / 25% cor ou estampa:

- **Partes de cima (6):** camisa branca de botão, blusa branca básica, blusa preta básica, camisa listrada azul/branco, blusa de cor (terracota ou azul sereno), blusa bege em tecido fluido.
- **Partes de baixo (5):** saia midi preta de alfaiataria, saia midi jeans, saia midi bege/off-white, saia midi plissada, saia longa fluida.
- **Peças únicas (2):** vestido midi preto, vestido midi estampado (estampa discreta).
- **Sobreposições (3):** blazer neutro estruturado, cardigã neutro, trench coat ou jaqueta jeans.
- **Calçados e acessório (4):** tênis branco, sapatilha nude de bico fino, sapato preto formal, bolsa estruturada básica.

**Lógica de combinação:** proporção visual 1/3–2/3 ao combinar saias midi com blusas por dentro; contraste entre tecidos estruturados (segurança/formalidade) e tecidos fluidos (leveza/movimento); base neutra permitindo combinações monocromáticas ou análogas; cobertura de múltiplas ocasiões (do escritório ao lazer) com as mesmas peças.

---

## 3. Por que calças não são consideradas adequadas (moda modesta)

Esta pergunta foi testada **duas vezes**: antes e depois da correção do material-fonte (livro), o que evidencia o processo de refinamento do projeto.

### Versão 1 — Antes da correção do livro

**Prompt:** `Explique por que calça não é considerada adequada para uma proposta de moda modesta.`

A resposta apresentava três pilares — distinção de gêneros, modéstia/caimento e mensagem/adequação — mas misturava o argumento central com as exceções de uso (frio intenso, esportes, tarefas domésticas), sem separação clara de blocos. As exceções apareciam soltas dentro dos parágrafos argumentativos, dificultando a leitura como material de estudo.

### Versão 2 — Depois da correção do livro

**Prompt:** `Explique por que calças não são consideradas adequadas para uma proposta de moda modesta.`

A resposta manteve os mesmos três pilares, mas agora estruturados como blocos nomeados e sequenciais:

1. **Distinção de Gêneros e Ordem da Criação** — diferenciação entre vestes masculinas e femininas como parte da identidade visual; risco de "confusão de papéis" quando essa distinção é apagada.
2. **Preservação da Modéstia e das Curvas** — peças que não marcam a anatomia do corpo são priorizadas para evitar exposição não intencional.
3. **Simbolismo e Mensagem Visual** — a aparência como comunicação não-verbal; saias e vestidos reforçam sobriedade e reverência.

Com uma seção final dedicada exclusivamente a **"Contextos de Exceção"**, deixando explícito que o uso de calça não é tratado como incorreto em si, mas sim contextual — sendo aceitável em atividades práticas, frio intenso ou esportes, desde que em modelos femininos e folgados.

**O que essa comparação demonstra:** pedir explicitamente uma estrutura em tópicos no prompt, combinado com a correção do material de origem, transformou uma resposta argumentativamente correta, porém confusa, em uma resposta clara, hierarquizada e fácil de reutilizar como material de estudo.

---

## 4. Acessórios para um look discreto e elegante

**Prompt:** `Explique quais acessórios valorizam um look discreto sem perder elegância.`

**Resposta:**

Os acessórios funcionam como o "toque final" que transforma uma produção básica em um visual com personalidade, mesmo sem o uso de joias. A resposta organizou as opções em cinco categorias:

1. **Cabeça e cabelo** — laços, tiaras e presilhas em veludo/seda (sem brilho excessivo) para um efeito romântico e delicado; chapéus e boinas para um ar mais sofisticado.
2. **Pescoço e ombros** — lenços de seda, bandanas, pashminas e echarpes substituem colares, trazendo cor e textura perto do rosto e, no caso das echarpes/pashminas, também estrutura e camadas que reforçam a modéstia.
3. **Cintos e marcação de cintura** — usados como recurso técnico para aplicar a proporção 1/3–2/3: cintos finos em tons neutros definem a silhueta sem marcar o corpo; cintos na mesma cor da peça funcionam bem para biotipos oval/retangular.
4. **Itens funcionais e estruturados** — bolsa estruturada, relógio analógico (citado como uma das poucas opções aceitas quando não se usam joias) e óculos com armação minimalista, todos reforçando autoridade e cuidado.
5. **Detalhes de acabamento** — broches (resina, madeira, tecido) e troca de botões simples por versões de melhor qualidade, como recurso de consultoria para elevar peças mais básicas.

**Princípios aplicados:** regra de quantidade (2 a 3 acessórios por look, para manter sobriedade), regra de cor 60-30-10 (acessório como "ponto de cor" em looks monocromáticos neutros), e consistência/asseio (acessórios limpos e em bom estado como parte da mensagem de excelência).

**Observação sobre o prompt:** essa foi uma das interações em que a resposta veio bem organizada de primeira, sem necessidade de refinamento — provavelmente porque o pedido já era objetivo (uma lista categorizada) e as fontes tinham conteúdo direto sobre o tema, ao contrário da pergunta sobre calças, que exigiu reformulação.
