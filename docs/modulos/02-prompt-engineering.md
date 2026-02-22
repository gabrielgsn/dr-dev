---
icon: material/chat-processing-outline
---

# Modulo 2: Prompt Engineering

!!! info "Tempo estimado: 45 minutos"

## O que voce vai aprender

- Entender por que a qualidade do prompt determina a qualidade do resultado
- Conhecer os 5 componentes de um prompt eficiente
- Aplicar tecnicas como cadeia de pensamento, exemplos e refinamento iterativo
- Identificar e evitar os erros mais comuns ao interagir com IA

---

## O modelo mental

Pense na IA como um **estagiario extremamente capaz**. Ele estudou tudo -- normas, manuais, artigos, livros. Tem um conhecimento tecnico impressionante. Mas acabou de chegar na sua empresa e nao sabe absolutamente nada sobre o **seu** projeto.

Se voce chega para esse estagiario e diz "projeta um predio", o resultado vai ser generico e provavelmente inutil. Mas se voce diz "projeta a estrutura de um edificio residencial de 5 andares, em solo argiloso, zona sismica 0, seguindo a NBR 6118, com orcamento de R$ 2M" -- agora ele tem o que precisa para entregar algo util.

!!! tip "A regra de ouro"
    A qualidade da saida e **diretamente proporcional** a qualidade da entrada. Prompt vago = resposta vaga. Prompt preciso = resposta precisa.

Essa e a essencia do prompt engineering: aprender a dar instrucoes claras, completas e bem estruturadas para que a IA entregue exatamente o que voce precisa.

Nao e sobre usar palavras magicas. E sobre **comunicacao eficiente** -- uma habilidade que todo engenheiro ja pratica no dia a dia.

---

## Anatomia de um bom prompt

Um bom prompt tem ate **5 componentes**. Nem sempre voce precisa de todos, mas quanto mais complexa a tarefa, mais componentes voce deve incluir.

Pense neles como as secoes de um memorial descritivo: cada uma cumpre uma funcao especifica.

### 1. Papel (Role)

Diga a IA **quem ela deve ser**. Isso ativa o "modo" certo de conhecimento e ajusta o tom da resposta.

!!! example "Exemplo"
    *"Voce e um engenheiro estrutural experiente, especializado em estruturas de concreto armado para edificios residenciais no Brasil."*

E como dizer ao estagiario: "para essa tarefa, quero que voce pense como um especialista em fundacoes." Ele vai ajustar a abordagem.

### 2. Tarefa (Task)

Defina **o que** voce quer que a IA faca. Seja especifico. "Me ajude" e vago. "Crie uma planilha de verificacao" e claro.

!!! example "Exemplo"
    *"Crie uma lista de verificacao (checklist) para inspecao de fundacoes em estacas cravadas."*

### 3. Contexto (Context)

Forneca as **informacoes de fundo** que a IA precisa para entender a situacao. E o briefing do projeto.

!!! example "Exemplo"
    *"O projeto e para um edificio residencial de 5 andares em Sao Paulo, zona sul. O solo e argiloso, o nivel do lencol freatico esta a 3 metros de profundidade e as estacas sao pre-moldadas de concreto com 30 cm de diametro."*

### 4. Formato (Format)

Especifique **como** voce quer a resposta. Tabela? Lista numerada? Codigo? Relatorio? Se voce nao disser, a IA decide por voce -- e nem sempre vai acertar.

!!! example "Exemplo"
    *"Apresente em formato de tabela com 4 colunas: Item de Verificacao, Criterio de Aceitacao, Metodo de Ensaio e Observacoes."*

### 5. Restricoes (Constraints)

Defina os **limites e regras** que a IA deve seguir. E o equivalente das premissas e hipoteses de calculo.

!!! example "Exemplo"
    *"Use a norma NBR 6122 como referencia principal. Limite a checklist a no maximo 15 itens. Evite jargao academico -- o documento sera usado por tecnicos em campo."*

---

### Comparacao: prompt ruim vs. prompt bom

Veja na pratica como os 5 componentes transformam o resultado:

=== "Prompt ruim :material-close:"

    ```
    Me ajude com fundacoes.
    ```

    **O que a IA vai entregar:** uma resposta generica sobre o que sao fundacoes, provavelmente copiando definicoes de livro-texto. Nada util para o seu projeto.

=== "Prompt bom :material-check:"

    ```
    Voce e um engenheiro geotecnico experiente. [PAPEL]

    Crie uma lista de verificacao para inspecao de
    fundacoes em estacas cravadas. [TAREFA]

    O projeto e um edificio residencial de 5 andares
    em Sao Paulo, solo argiloso, lencol freatico a 3m,
    estacas pre-moldadas de concreto de 30cm. [CONTEXTO]

    Apresente em tabela com colunas: Item, Criterio de
    Aceitacao, Metodo de Ensaio, Observacoes. [FORMATO]

    Use a NBR 6122 como referencia. Maximo 15 itens.
    Linguagem simples para uso em campo. [RESTRICOES]
    ```

    **O que a IA vai entregar:** uma checklist pratica, normatizada, formatada e pronta para uso. Uma resposta que realmente economiza horas de trabalho.

!!! tip "Dica pratica"
    Voce nao precisa rotular cada componente como `[PAPEL]` ou `[CONTEXTO]`. Esses rotulos estao ai apenas para fins didaticos. Na pratica, basta escrever tudo de forma natural em um unico paragrafo ou em blocos separados.

---

## Tecnicas essenciais

Alem de estruturar bem o prompt, existem tecnicas especificas que melhoram drasticamente a qualidade das respostas.

### Prompt de passo a passo (Chain of Thought)

Pedir para a IA **pensar passo a passo** faz com que ela decomponha o problema antes de dar a resposta final. Isso reduz erros, especialmente em tarefas que envolvem logica, calculo ou analise.

E o equivalente de pedir para o estagiario "me mostre o memorial de calculo, nao so o resultado."

!!! example "Exemplo"
    ```
    Preciso dimensionar uma viga de concreto armado
    simplesmente apoiada, com vao de 6 metros e carga
    distribuida de 15 kN/m.

    Pense passo a passo:
    1. Calcule o momento fletor maximo
    2. Estime a altura util necessaria
    3. Calcule a area de aco necessaria
    4. Sugira a armadura (diametro e quantidade de barras)

    Mostre cada etapa com as formulas utilizadas.
    ```

!!! tip "Quando usar"
    Use chain of thought sempre que a tarefa envolver **calculos, decisoes com multiplos criterios ou analises** onde voce quer entender o raciocinio, nao so o resultado.

---

### Exemplos no prompt (Few-shot)

Dar **1 ou 2 exemplos** do que voce espera e uma das tecnicas mais poderosas. A IA entende padrao muito melhor que descricoes abstratas.

Imagine que voce quer que a IA transforme descricoes de tarefas em itens de escopo formatados. Em vez de explicar o formato, mostre:

=== "Sem exemplo"

    ```
    Transforme descricoes de servicos em itens de
    escopo padronizados para um cronograma de obra.
    ```

    A IA vai inventar um formato proprio -- que pode nao ser o que voce quer.

=== "Com exemplo"

    ```
    Transforme descricoes de servicos em itens de
    escopo padronizados. Siga exatamente este formato:

    Entrada: "Tirar o entulho do terreno e nivelar"
    Saida: "1.1 - Limpeza do terreno e remocao de
    entulho | 1.2 - Terraplanagem e nivelamento do
    terreno"

    Agora transforme:
    "Fazer as formas, armar e concretar as sapatas"
    ```

    A IA vai seguir exatamente o padrao do exemplo.

!!! tip "Regra de ouro do few-shot"
    Um bom exemplo vale mais que um paragrafo de explicacao. Se voce tem dificuldade em descrever o que quer, **mostre** o que quer.

---

### Prompt iterativo

Voce **nao precisa acertar de primeira**. Na verdade, os melhores resultados vem de uma conversa iterativa com a IA, refinando a cada rodada.

E como o processo de revisao de um projeto: a primeira versao nunca e a final.

Veja um exemplo de refinamento em 3 passos:

!!! example "Passo 1: Exploratorio"
    ```
    Quais sao os principais metodos de impermeabilizacao
    para lajes de cobertura?
    ```
    *A IA vai listar varios metodos. Voce le e escolhe o que interessa.*

!!! example "Passo 2: Foco"
    ```
    Fale mais sobre manta asfaltica vs. membrana liquida.
    Compare custo, durabilidade e facilidade de aplicacao
    para uma laje de 200m2 exposta ao sol.
    ```
    *Agora voce tem uma comparacao direcionada.*

!!! example "Passo 3: Decisao"
    ```
    Considerando que o acesso ao telhado e dificil e a
    mao de obra local so tem experiencia com manta
    asfaltica, qual opcao voce recomenda? Justifique e
    liste os cuidados na aplicacao.
    ```
    *A IA deu uma recomendacao personalizada com justificativa.*

Perceba: cada prompt **constroi sobre o anterior**. A conversa toda forma um raciocinio completo. Nenhum dos 3 prompts isoladamente daria um resultado tao bom.

---

### Prompt de restricao

As vezes o problema nao e que a IA nao sabe a resposta -- e que ela responde **demais**. Restricoes ajudam a manter o foco.

Pense em restricoes como as condicoes de contorno de um problema de engenharia: elas delimitam o espaco de solucoes.

!!! example "Exemplos de restricoes uteis"
    - *"Limite a resposta a 5 itens, priorizando por impacto."*
    - *"NAO use jargao tecnico. O texto sera lido por clientes leigos."*
    - *"Responda em formato de email profissional, maximo 3 paragrafos."*
    - *"Considere APENAS solucoes que custem menos de R$ 50 mil."*
    - *"Nao inclua opcoes que exijam mao de obra especializada importada."*

!!! tip "Dica"
    Restricoes sao especialmente uteis quando voce ja sabe o que **nao** quer. Se a IA esta dando respostas longas demais, genericas demais, ou fora de escopo -- adicione restricoes.

---

## Erros comuns

!!! warning "Erro 1: Ser vago demais"
    **Prompt:** *"Me ajude com meu projeto."*

    A IA nao sabe se voce quer ajuda com calculo, cronograma, orcamento ou apresentacao. O resultado sera generico e provavelmente inutil. Sempre especifique **o que** voce quer e **sobre o que**.

!!! warning "Erro 2: Pedir muitas coisas de uma vez"
    **Prompt:** *"Faca o dimensionamento estrutural, o orcamento, o cronograma e o memorial descritivo do projeto."*

    A IA perde foco quando recebe tarefas demais em um unico prompt. O resultado de cada parte sera superficial. **Divida em prompts separados**, um para cada tarefa.

!!! warning "Erro 3: Nao fornecer contexto"
    **Prompt:** *"Qual o melhor tipo de fundacao?"*

    Depende do solo, da carga, do local, do orcamento... sem contexto, a IA so pode dar uma resposta generica. E como perguntar "qual o melhor remedio?" sem dizer o sintoma.

!!! warning "Erro 4: Esperar perfeicao na primeira tentativa"
    Prompt engineering e **iterativo por natureza**. Se a primeira resposta nao ficou boa, nao desista. Refine o prompt, adicione contexto, peca ajustes. Isso nao e falha -- e o processo normal.

!!! warning "Erro 5: Nao especificar o formato desejado"
    Se voce quer uma tabela e recebe um texto corrido, a culpa nao e da IA -- e do prompt. Sempre diga **como** voce quer a resposta: tabela, lista, topicos, codigo, email, relatorio, etc.

---

## Exercicio pratico

!!! tip "Mao na massa: De ruim a otimo em 3 passos"
    Este exercicio leva cerca de **15 minutos** e vai mudar a forma como voce interage com IA.

O objetivo e simples: escrever **3 versoes** de um prompt sobre o mesmo tema, cada uma melhor que a anterior, e comparar os resultados.

### Versao 1 -- Ruim

```
Me ajude a calcular algo de engenharia.
```

Abra o [claude.ai](https://claude.ai){ target="_blank" } e envie esse prompt. Note como a resposta e vaga, generica e nada util.

### Versao 2 -- Melhor

```
Preciso calcular a carga maxima que uma viga de concreto
armado pode suportar. A viga tem 6 metros de vao livre
e secao retangular de 20x50 cm.
```

Envie esse prompt na mesma conversa (ou em uma nova). Compare: a resposta ja e muito mais especifica e direcionada.

### Versao 3 -- Otimo

```
Voce e um engenheiro estrutural especializado em
concreto armado.

Calcule a carga maxima distribuida que uma viga
simplesmente apoiada pode suportar.

Dados da viga:
- Vao livre: 6 metros
- Secao: 20 x 50 cm (bw x h)
- Concreto: fck = 25 MPa
- Aco: CA-50
- Cobrimento: 3 cm
- Armadura longitudinal: 4 barras de 16mm

Apresente o calculo passo a passo, mostrando:
1. Altura util (d)
2. Momento resistente da secao
3. Carga distribuida maxima correspondente

Use as prescricoes da NBR 6118. Mostre as formulas
utilizadas em cada etapa.
```

Envie e compare. A diferenca na qualidade da resposta e dramatica.

### Agora e a sua vez

1. Pense em um **problema real** do seu dia a dia de trabalho
2. Escreva **3 versoes** de prompt (ruim, melhor, otimo) sobre esse problema
3. Teste cada versao no [claude.ai](https://claude.ai){ target="_blank" }
4. Compare os resultados

!!! tip "Dica valiosa"
    Salve seus melhores prompts em um documento. Com o tempo, voce vai montar uma **biblioteca de prompts** uteis para o seu trabalho. E como ter uma colecao de templates de calculo: voce nao refaz do zero toda vez.

---

## Resumo

- A IA e como um estagiario brilhante: sabe muito, mas precisa de **instrucoes claras** sobre o seu contexto especifico
- Um bom prompt tem ate 5 componentes: **Papel, Tarefa, Contexto, Formato e Restricoes**
- Tecnicas como **cadeia de pensamento** e **exemplos no prompt** melhoram drasticamente a qualidade das respostas
- Prompt engineering e **iterativo** -- refinar e parte do processo, nao sinal de falha
- **Restricoes** sao suas melhores amigas para evitar respostas genericas ou prolixas

---

## Proximo passo

No **[Modulo 3: Ferramentas do Ecossistema](03-ferramentas.md)**, voce vai conhecer as principais plataformas de AI coding -- Claude, Cursor, Bolt, Lovable e outras. Vai entender qual ferramenta usar para cada tipo de tarefa e como escolher a certa para o seu caso.

[:material-arrow-right: Ir para o Modulo 3](03-ferramentas.md){ .md-button .md-button--primary }
