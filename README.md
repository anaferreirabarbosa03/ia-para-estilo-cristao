# Moda Modesta com Estilo — Caderno Temático com NotebookLM

## Sobre o Projeto

Este projeto foi desenvolvido como parte do desafio de projeto da **DIO**, utilizando o **NotebookLM** como ferramenta de aprendizagem ativa e curadoria de conhecimento.

O objetivo foi construir um **caderno temático especializado em Moda Modesta Feminina**, reunindo diferentes fontes sobre consultoria de imagem, estilo, tecidos, modelagem, combinações e princípios da moda modesta.

Mais do que resumir conteúdos, a proposta foi **treinar a IA para responder dentro de um contexto específico**, oferecendo sugestões coerentes com um estilo elegante, feminino e discreto — e documentar todo o raciocínio, os testes e os ajustes feitos ao longo do caminho.

---

## Objetivos

- Criar uma base de conhecimento estruturada sobre moda modesta.
- Ensinar a IA a gerar recomendações alinhadas ao conceito de modéstia.
- Aprender e praticar técnicas de engenharia de prompts (prompt base, especialização e refinamento).
- Criar um guia reutilizável para futuras consultas de estilo.
- Organizar um acervo de referências confiáveis sobre o tema.

---

## Curadoria de Fontes

| Tipo | Fonte | Descrição |
|------|-------|-----------|
| PDF | *Vestuário, Certo Qual É?* | Livro base sobre princípios de vestimenta e modéstia |
| PDF | Materiais de palestra sobre moda | Conteúdo de apoio sobre estilo e apresentação pessoal |
| DOCX | Transcrição de vídeo (YouTube) | Conteúdo sobre moda modesta reunido e organizado manualmente |
| DOCX | Palestra sobre moda modesta | Material de referência adicional |
| Link | [Pinterest — Painel de referências visuais](https://pin.it/6ZI1hYW7G) | Curadoria visual de looks alinhados aos princípios de modéstia |

> **Observação sobre a curadoria:** encontrar boas referências prontas sobre moda modesta — para mulheres que não utilizam decotes, roupas muito justas, joias, calças, roupas sem manga ou com transparência — é um desafio, pois a maior parte do conteúdo disponível na internet segue tendências opostas a esses princípios. Por isso, foi necessária uma curadoria detalhada: documentos foram criados e agrupados especificamente sobre o assunto, para evitar que o NotebookLM trouxesse à tona referências de moda contrárias aos princípios da modéstia.

---

## Engenharia de Prompts e "Cicatrizes"

### Prompt Base (persona)

```
Você é uma consultora especializada em moda modesta feminina.
Considere sempre os seguintes critérios:
- não sugerir decotes profundos;
- não sugerir transparências;
- não sugerir roupas muito justas;
- evitar peças excessivamente curtas;
- priorizar mangas;
- priorizar saias e vestidos midi ou longos;
- priorizar elegância atemporal;
- utilizar princípios de consultoria de imagem;
- considerar combinação de cores;
- considerar tecidos;
- considerar proporção corporal;
- considerar ocasiões de uso.

Quando houver mais de uma opção, explique o motivo da escolha.
```

**Por que esse formato?** Definir a persona e as regras logo no início ancora todas as respostas seguintes da IA dentro do mesmo contexto, evitando que ela "esqueça" os critérios de modéstia em perguntas subsequentes na mesma conversa.

### Prompts Especializados (testados a partir do prompt base)

1. `Monte um look para trabalhar em um escritório.`
2. `Monte uma mala cápsula com 20 peças.`
3. `Explique por que determinada calça não é considerada adequada para uma proposta de moda modesta.`
4. `Explique quais acessórios valorizam um look discreto sem perder elegância.`

### Cicatrizes (dificuldades encontradas e como foram resolvidas)

**Cicatriz 1 — Exceções da fonte original conflitando com a regra do projeto**

- **O que aconteceu:** o autor do livro utilizado como fonte fazia exceções ao uso de calças em contextos específicos (frio intenso, atividades práticas), e essas exceções apareciam misturadas com o argumento principal, deixando a resposta menos clara sobre qual era a regra geral e qual era a exceção pontual.
- **Diagnóstico:** a IA estava reproduzindo a estrutura argumentativa bruta da fonte, sem reorganizar o raciocínio em blocos temáticos claros (motivo → base conceitual → modéstia → exceções).
- **Solução aplicada:** revisei o material de origem e refinei o prompt pedindo explicitamente uma estrutura em tópicos nomeados, separando o argumento central das exceções de uso prático.
- **Resultado (antes → depois):**

  | Antes da correção | Depois da correção |
  |---|---|
  | Resposta citava a calça como "não pecaminosa por si mesma", mas misturava argumentos de identidade, saúde e modéstia sem separação clara entre regra geral e exceção | Resposta passou a ter estrutura em 3 pilares nomeados (Distinção de Gêneros, Preservação da Modéstia, Simbolismo/Mensagem Visual) + uma seção final dedicada só a "Contextos de Exceção" |
  | Exceções (frio, esporte, tarefas domésticas) apareciam soltas no meio do texto | Exceções centralizadas em um único bloco, com critério explícito ("modelos femininos, folgados, que respeitem o pudor") |

  Isso mostra como pequenos ajustes no prompt (pedir estrutura explícita) e na curadoria da fonte melhoram significativamente a utilidade da resposta para revisão futura.

> 📄 O registro completo das perguntas e respostas testadas está documentado em [`interacoes-notebooklm.md`](./interacoes-notebooklm.md).

**Cicatriz 2 — Ambiguidade em pedidos abertos (ex.: mala cápsula)**

- **O que aconteceu:** ao pedir "monte uma mala cápsula com 20 peças" sem contexto adicional, a IA retornava combinações genéricas, sem considerar estação do ano ou ocasião de uso.
- **Solução aplicada:** passei a adicionar contexto ao prompt (estação, clima, ocasiões previstas) e pedir que a IA explicasse a lógica de combinação entre as peças, não apenas listasse itens.
- **Resultado:** respostas mais úteis e reutilizáveis, com justificativa de combinação de cores e tecidos.

---

## Miniguia de Estudo (Entrega Final)

### 1. Resumos Estruturados

**Silhueta e caimento**
Priorizar peças com caimento solto a semi-ajustado, evitando tecidos colados ao corpo. O objetivo é sugerir a forma do corpo sem expor contornos.

**Comprimento**
Saias e vestidos midi (na altura da canela) ou longos são preferidos a peças curtas. Em calças, prioriza-se comprimento total, evitando modelos muito justos.

**Decote e mangas**
Decotes discretos (canoa, careca, gola alta) substituem decotes profundos. Mangas — de três quartos a longas — são priorizadas no lugar de looks sem manga, especialmente em contextos formais.

**Transparência e tecidos**
Tecidos opacos e de boa estrutura (algodão, linho, tricoline, malhas mais densas) são preferidos. Quando há transparência natural do tecido, recomenda-se forro ou sobreposição.

**Cor e combinação**
A consultoria de imagem é usada para indicar paletas harmônicas (cores neutras como base + uma cor de destaque), favorecendo elegância atemporal em vez de estampas ou combinações muito chamativas.

**Proporção corporal**
Peças são escolhidas considerando o formato do corpo (ampulheta, triângulo, retângulo, etc.), buscando equilíbrio visual sem depender de roupas justas para isso.

**Ocasião de uso**
Cada contexto (trabalho, igreja, casual, eventos) tem um conjunto de critérios próprios dentro dos princípios gerais de modéstia — por exemplo, o escritório pede mais estrutura e sobriedade, enquanto o casual permite mais leveza nos tecidos.

### 2. Glossário

| Termo | Definição |
|---|---|
| **Modéstia (moda)** | Filosofia de vestir que prioriza discrição, cobertura adequada e elegância, evitando exposição do corpo |
| **Midi** | Comprimento de saia/vestido que vai até a altura da canela |
| **Consultoria de imagem** | Área que estuda cor, forma, proporção e estilo para orientar escolhas de vestuário |
| **Mala cápsula** | Conjunto reduzido de peças versáteis, combináveis entre si, pensado para otimizar o guarda-roupa |
| **Proporção corporal** | Análise da relação entre as medidas do corpo, usada para equilibrar visualmente um look |
| **Paleta de cores** | Conjunto de cores que combinam entre si e favorecem a pessoa, usado como base de composição de looks |
| **Tecido estruturado** | Tecido com corpo e caimento firme, que não marca o corpo e mantém a forma da peça |
| **Elegância atemporal** | Estilo que não segue tendências passageiras, priorizando peças e combinações duradouras |

### 3. Prompts Reutilizáveis (para futuras consultas)

```
[PERSONA]
Você é uma consultora especializada em moda modesta feminina. Considere sempre:
não sugerir decotes profundos; não sugerir transparências; não sugerir roupas
muito justas; evitar peças curtas; priorizar mangas; priorizar saias e vestidos
midi/longos; priorizar elegância atemporal; usar princípios de consultoria de
imagem (cor, tecido, proporção corporal, ocasião de uso). Quando houver mais de
uma opção, explique o motivo da escolha.

[LOOK PONTUAL]
Monte um look para [ocasião: trabalho / igreja / casual / evento], considerando
estação [verão/inverno], e explique cada escolha.

[MALA CÁPSULA]
Monte uma mala cápsula com [N] peças para [estação/ocasião], explicando como as
peças se combinam entre si e por que cada uma foi incluída.

[JUSTIFICATIVA / TROUBLESHOOTING]
Explique por que [peça específica] não é considerada adequada dentro dos
princípios de moda modesta definidos acima, e sugira uma alternativa equivalente.

[ACESSÓRIOS]
Quais acessórios valorizam um look discreto sem perder elegância, considerando
[ocasião]? Explique o motivo de cada sugestão.
```

---

## Como este projeto foi construído (reprodutibilidade)

1. Fontes selecionadas e revisadas manualmente para alinhamento com os princípios de modéstia.
2. Upload das fontes no NotebookLM.
3. Criação do prompt base (persona + regras).
4. Testes com prompts especializados, registrando respostas e dificuldades.
5. Refinamento iterativo dos prompts a partir das "cicatrizes" encontradas.
6. Consolidação dos aprendizados no Miniguia final (resumos + glossário + prompts reutilizáveis).

---

## Referências Visuais

- [Painel de inspiração no Pinterest](https://pin.it/6ZI1hYW7G)

---

*Projeto desenvolvido para o desafio de projeto da [DIO](https://www.dio.me/) utilizando NotebookLM.*

