---
icon: material/chat-processing-outline
---

# Módulo 2: Prompt Engineering

!!! info "Tempo estimado: 45 minutos"

## O que você vai aprender

- Entender por que a qualidade do prompt determina a qualidade do resultado
- Conhecer os 5 componentes de um prompt eficiente
- Aplicar técnicas como cadeia de pensamento, exemplos e refinamento iterativo
- Identificar e evitar os erros mais comuns ao interagir com IA

---

## O modelo mental

Pense na IA como um **estagiário extremamente capaz**. Ele estudou tudo -- normas, manuais, artigos, livros. Tem um conhecimento técnico impressionante. Mas acabou de chegar na sua empresa e não sabe absolutamente nada sobre o **seu** projeto.

Se você chega para esse estagiário e diz "projeta um prédio", o resultado vai ser genérico e provavelmente inútil. Mas se você diz "projeta a estrutura de um edifício residencial de 5 andares, em solo argiloso, zona sísmica 0, seguindo a NBR 6118, com orçamento de R$ 2M" -- agora ele tem o que precisa para entregar algo útil.

!!! tip "A regra de ouro"
    A qualidade da saída é **diretamente proporcional** à qualidade da entrada. Prompt vago = resposta vaga. Prompt preciso = resposta precisa.

Essa é a essência do prompt engineering: aprender a dar instruções claras, completas e bem estruturadas para que a IA entregue exatamente o que você precisa.

Não é sobre usar palavras mágicas. É sobre **comunicação eficiente** -- uma habilidade que todo engenheiro já pratica no dia a dia.

---

## Anatomia de um bom prompt

Um bom prompt tem até **5 componentes**. Nem sempre você precisa de todos, mas quanto mais complexa a tarefa, mais componentes você deve incluir.

Pense neles como as seções de um memorial descritivo: cada uma cumpre uma função específica.

### 1. Papel (Role)

Diga à IA **quem ela deve ser**. Isso ativa o "modo" certo de conhecimento e ajusta o tom da resposta.

!!! example "Exemplo"
    *"Você é um engenheiro estrutural experiente, especializado em estruturas de concreto armado para edifícios residenciais no Brasil."*

É como dizer ao estagiário: "para essa tarefa, quero que você pense como um especialista em fundações." Ele vai ajustar a abordagem.

### 2. Tarefa (Task)

Defina **o que** você quer que a IA faça. Seja específico. "Me ajude" é vago. "Crie uma planilha de verificação" é claro.

!!! example "Exemplo"
    *"Crie uma lista de verificação (checklist) para inspeção de fundações em estacas cravadas."*

### 3. Contexto (Context)

Forneça as **informações de fundo** que a IA precisa para entender a situação. É o briefing do projeto.

!!! example "Exemplo"
    *"O projeto é para um edifício residencial de 5 andares em São Paulo, zona sul. O solo é argiloso, o nível do lençol freático está a 3 metros de profundidade e as estacas são pré-moldadas de concreto com 30 cm de diâmetro."*

### 4. Formato (Format)

Especifique **como** você quer a resposta. Tabela? Lista numerada? Código? Relatório? Se você não disser, a IA decide por você -- e nem sempre vai acertar.

!!! example "Exemplo"
    *"Apresente em formato de tabela com 4 colunas: Item de Verificação, Critério de Aceitação, Método de Ensaio e Observações."*

### 5. Restrições (Constraints)

Defina os **limites e regras** que a IA deve seguir. É o equivalente das premissas e hipóteses de cálculo.

!!! example "Exemplo"
    *"Use a norma NBR 6122 como referência principal. Limite a checklist a no máximo 15 itens. Evite jargão acadêmico -- o documento será usado por técnicos em campo."*

---

### Comparação: prompt ruim vs. prompt bom

Veja na prática como os 5 componentes transformam o resultado:

=== "Prompt ruim :material-close:"

    ```
    Me ajude com fundações.
    ```

    **O que a IA vai entregar:** uma resposta genérica sobre o que são fundações, provavelmente copiando definições de livro-texto. Nada útil para o seu projeto.

=== "Prompt bom :material-check:"

    ```
    Você é um engenheiro geotécnico experiente. [PAPEL]

    Crie uma lista de verificação para inspeção de
    fundações em estacas cravadas. [TAREFA]

    O projeto é um edifício residencial de 5 andares
    em São Paulo, solo argiloso, lençol freático a 3m,
    estacas pré-moldadas de concreto de 30cm. [CONTEXTO]

    Apresente em tabela com colunas: Item, Critério de
    Aceitação, Método de Ensaio, Observações. [FORMATO]

    Use a NBR 6122 como referência. Máximo 15 itens.
    Linguagem simples para uso em campo. [RESTRIÇÕES]
    ```

    **O que a IA vai entregar:** uma checklist prática, normatizada, formatada e pronta para uso. Uma resposta que realmente economiza horas de trabalho.

!!! tip "Dica prática"
    Você não precisa rotular cada componente como `[PAPEL]` ou `[CONTEXTO]`. Esses rótulos estão aí apenas para fins didáticos. Na prática, basta escrever tudo de forma natural em um único parágrafo ou em blocos separados.

---

## Técnicas essenciais

Além de estruturar bem o prompt, existem técnicas específicas que melhoram drasticamente a qualidade das respostas.

### Prompt de passo a passo (Chain of Thought)

Pedir para a IA **pensar passo a passo** faz com que ela decomponha o problema antes de dar a resposta final. Isso reduz erros, especialmente em tarefas que envolvem lógica, cálculo ou análise.

É o equivalente de pedir para o estagiário "me mostre o memorial de cálculo, não só o resultado."

!!! example "Exemplo"
    ```
    Preciso dimensionar uma viga de concreto armado
    simplesmente apoiada, com vão de 6 metros e carga
    distribuída de 15 kN/m.

    Pense passo a passo:
    1. Calcule o momento fletor máximo
    2. Estime a altura útil necessária
    3. Calcule a área de aço necessária
    4. Sugira a armadura (diâmetro e quantidade de barras)

    Mostre cada etapa com as fórmulas utilizadas.
    ```

!!! tip "Quando usar"
    Use chain of thought sempre que a tarefa envolver **cálculos, decisões com múltiplos critérios ou análises** onde você quer entender o raciocínio, não só o resultado.

---

### Exemplos no prompt (Few-shot)

Dar **1 ou 2 exemplos** do que você espera é uma das técnicas mais poderosas. A IA entende padrão muito melhor que descrições abstratas.

Imagine que você quer que a IA transforme descrições de tarefas em itens de escopo formatados. Em vez de explicar o formato, mostre:

=== "Sem exemplo"

    ```
    Transforme descrições de serviços em itens de
    escopo padronizados para um cronograma de obra.
    ```

    A IA vai inventar um formato próprio -- que pode não ser o que você quer.

=== "Com exemplo"

    ```
    Transforme descrições de serviços em itens de
    escopo padronizados. Siga exatamente este formato:

    Entrada: "Tirar o entulho do terreno e nivelar"
    Saída: "1.1 - Limpeza do terreno e remoção de
    entulho | 1.2 - Terraplanagem e nivelamento do
    terreno"

    Agora transforme:
    "Fazer as formas, armar e concretar as sapatas"
    ```

    A IA vai seguir exatamente o padrão do exemplo.

!!! tip "Regra de ouro do few-shot"
    Um bom exemplo vale mais que um parágrafo de explicação. Se você tem dificuldade em descrever o que quer, **mostre** o que quer.

---

### Prompt iterativo

Você **não precisa acertar de primeira**. Na verdade, os melhores resultados vêm de uma conversa iterativa com a IA, refinando a cada rodada.

É como o processo de revisão de um projeto: a primeira versão nunca é a final.

Veja um exemplo de refinamento em 3 passos:

!!! example "Passo 1: Exploratório"
    ```
    Quais são os principais métodos de impermeabilização
    para lajes de cobertura?
    ```
    *A IA vai listar vários métodos. Você lê e escolhe o que interessa.*

!!! example "Passo 2: Foco"
    ```
    Fale mais sobre manta asfáltica vs. membrana líquida.
    Compare custo, durabilidade e facilidade de aplicação
    para uma laje de 200m² exposta ao sol.
    ```
    *Agora você tem uma comparação direcionada.*

!!! example "Passo 3: Decisão"
    ```
    Considerando que o acesso ao telhado é difícil e a
    mão de obra local só tem experiência com manta
    asfáltica, qual opção você recomenda? Justifique e
    liste os cuidados na aplicação.
    ```
    *A IA deu uma recomendação personalizada com justificativa.*

Perceba: cada prompt **constrói sobre o anterior**. A conversa toda forma um raciocínio completo. Nenhum dos 3 prompts isoladamente daria um resultado tão bom.

---

### Prompt de restrição

Às vezes o problema não é que a IA não sabe a resposta -- é que ela responde **demais**. Restrições ajudam a manter o foco.

Pense em restrições como as condições de contorno de um problema de engenharia: elas delimitam o espaço de soluções.

!!! example "Exemplos de restrições úteis"
    - *"Limite a resposta a 5 itens, priorizando por impacto."*
    - *"NÃO use jargão técnico. O texto será lido por clientes leigos."*
    - *"Responda em formato de email profissional, máximo 3 parágrafos."*
    - *"Considere APENAS soluções que custem menos de R$ 50 mil."*
    - *"Não inclua opções que exijam mão de obra especializada importada."*

!!! tip "Dica"
    Restrições são especialmente úteis quando você já sabe o que **não** quer. Se a IA está dando respostas longas demais, genéricas demais, ou fora de escopo -- adicione restrições.

---

## Erros comuns

!!! warning "Erro 1: Ser vago demais"
    **Prompt:** *"Me ajude com meu projeto."*

    A IA não sabe se você quer ajuda com cálculo, cronograma, orçamento ou apresentação. O resultado será genérico e provavelmente inútil. Sempre especifique **o que** você quer e **sobre o que**.

!!! warning "Erro 2: Pedir muitas coisas de uma vez"
    **Prompt:** *"Faça o dimensionamento estrutural, o orçamento, o cronograma e o memorial descritivo do projeto."*

    A IA perde foco quando recebe tarefas demais em um único prompt. O resultado de cada parte será superficial. **Divida em prompts separados**, um para cada tarefa.

!!! warning "Erro 3: Não fornecer contexto"
    **Prompt:** *"Qual o melhor tipo de fundação?"*

    Depende do solo, da carga, do local, do orçamento... sem contexto, a IA só pode dar uma resposta genérica. É como perguntar "qual o melhor remédio?" sem dizer o sintoma.

!!! warning "Erro 4: Esperar perfeição na primeira tentativa"
    Prompt engineering é **iterativo por natureza**. Se a primeira resposta não ficou boa, não desista. Refine o prompt, adicione contexto, peça ajustes. Isso não é falha -- é o processo normal.

!!! warning "Erro 5: Não especificar o formato desejado"
    Se você quer uma tabela e recebe um texto corrido, a culpa não é da IA -- é do prompt. Sempre diga **como** você quer a resposta: tabela, lista, tópicos, código, email, relatório, etc.

---

## Exercício prático

!!! tip "Mão na massa: De ruim a ótimo em 3 passos"
    Este exercício leva cerca de **15 minutos** e vai mudar a forma como você interage com IA.

O objetivo é simples: escrever **3 versões** de um prompt sobre o mesmo tema, cada uma melhor que a anterior, e comparar os resultados.

### Versão 1 -- Ruim

```
Me ajude a calcular algo de engenharia.
```

Abra o [claude.ai](https://claude.ai){ target="_blank" } e envie esse prompt. Note como a resposta é vaga, genérica e nada útil.

### Versão 2 -- Melhor

```
Preciso calcular a carga máxima que uma viga de concreto
armado pode suportar. A viga tem 6 metros de vão livre
e seção retangular de 20x50 cm.
```

Envie esse prompt na mesma conversa (ou em uma nova). Compare: a resposta já é muito mais específica e direcionada.

### Versão 3 -- Ótimo

```
Você é um engenheiro estrutural especializado em
concreto armado.

Calcule a carga máxima distribuída que uma viga
simplesmente apoiada pode suportar.

Dados da viga:
- Vão livre: 6 metros
- Seção: 20 x 50 cm (bw x h)
- Concreto: fck = 25 MPa
- Aço: CA-50
- Cobrimento: 3 cm
- Armadura longitudinal: 4 barras de 16mm

Apresente o cálculo passo a passo, mostrando:
1. Altura útil (d)
2. Momento resistente da seção
3. Carga distribuída máxima correspondente

Use as prescrições da NBR 6118. Mostre as fórmulas
utilizadas em cada etapa.
```

Envie e compare. A diferença na qualidade da resposta é dramática.

### Agora é a sua vez

1. Pense em um **problema real** do seu dia a dia de trabalho
2. Escreva **3 versões** de prompt (ruim, melhor, ótimo) sobre esse problema
3. Teste cada versão no [claude.ai](https://claude.ai){ target="_blank" }
4. Compare os resultados

!!! tip "Dica valiosa"
    Salve seus melhores prompts em um documento. Com o tempo, você vai montar uma **biblioteca de prompts** úteis para o seu trabalho. É como ter uma coleção de templates de cálculo: você não refaz do zero toda vez.

---

## Resumo

- A IA é como um estagiário brilhante: sabe muito, mas precisa de **instruções claras** sobre o seu contexto específico
- Um bom prompt tem até 5 componentes: **Papel, Tarefa, Contexto, Formato e Restrições**
- Técnicas como **cadeia de pensamento** e **exemplos no prompt** melhoram drasticamente a qualidade das respostas
- Prompt engineering é **iterativo** -- refinar é parte do processo, não sinal de falha
- **Restrições** são suas melhores amigas para evitar respostas genéricas ou prolixas

---

## Próximo passo

No **[Módulo 3: Ferramentas do Ecossistema](03-ferramentas.md)**, você vai conhecer as principais plataformas de AI coding -- Claude, Cursor, Bolt, Lovable e outras. Vai entender qual ferramenta usar para cada tipo de tarefa e como escolher a certa para o seu caso.

[:material-arrow-right: Ir para o Módulo 3](03-ferramentas.md){ .md-button .md-button--primary }
