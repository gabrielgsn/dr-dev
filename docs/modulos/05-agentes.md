---
icon: material/robot-outline
---

# Módulo 5: Agentes de IA Trabalhando por Você

!!! info "Tempo estimado: 45 minutos"

## O que você vai aprender

- O que é um "agente de IA" e como ele é diferente de um chatbot comum
- Como funciona a coordenação entre múltiplos agentes (orquestração)
- Quais tarefas os agentes já conseguem fazer de forma autônoma hoje
- Como supervisionar agentes de forma eficiente sem perder o controle

---

## A analogia da equipe

Imagine que você contratou um assistente muito competente. Um dia, você passa uma tarefa complexa para ele: analisar documentos, pesquisar informações, calcular custos e montar um relatório final.

Esse assistente inteligente não faz tudo sozinho. Ele monta uma **mini-equipe**:

- Um **especialista em análise** para ler os documentos
- Um **pesquisador** para buscar informações online
- Um **contador** para fazer os cálculos
- Um **redator** para escrever o relatório final

Seu assistente coordena tudo. Você só deu o objetivo. No final, recebe o relatório pronto.

**Isso é orquestração de agentes.** A IA cria uma equipe virtual, divide o problema em partes, e cada "especialista" resolve a sua parte.

!!! tip "Você não é o programador aqui"
    Você é o **diretor**. Você define o objetivo e aprova o resultado. Os agentes fazem o trabalho operacional.

---

## Chatbot vs. Agente: qual a diferença?

É fácil confundir os dois. Veja a distinção prática:

| | Chatbot | Agente |
|---|---------|--------|
| **Como funciona** | Você pergunta, ele responde | Você dá um objetivo, ele age |
| **Usa ferramentas?** | Não | Sim (navega na web, lê arquivos, executa código) |
| **Autonomia** | Nenhuma | Alta — toma decisões intermediárias |
| **Interação** | Rodada a rodada | Pode trabalhar por minutos sozinho |
| **Exemplo** | "Explique X" | "Pesquise os 5 melhores fornecedores de X e monte uma comparação" |

!!! example "Exemplo concreto"
    **Chatbot:** *"Quais são os critérios para escolher um fornecedor de concreto?"*
    → A IA explica os critérios. Você ainda precisa fazer a pesquisa.

    **Agente:** *"Pesquise fornecedores de concreto na região de Campinas, compare preços e prazo de entrega, e me apresente os 3 melhores com justificativa."*
    → O agente pesquisa, compara e entrega o resultado. Você revisa e decide.

---

## Como os agentes funcionam

O padrão que domina o mercado em 2025 tem três papéis:

### :material-chess-king: O Orquestrador — o gerente

Recebe seu objetivo. Decompõe em tarefas menores. Delega para os agentes trabalhadores. Consolida os resultados no final.

### :material-account-hard-hat: Os Trabalhadores — os especialistas

Cada um executa uma tarefa específica: buscar informação, ler um documento, fazer um cálculo, gerar um texto. Podem usar ferramentas reais — navegador, arquivos, código.

### :material-clipboard-check-outline: O Avaliador — o revisor

Verifica se o resultado atende ao objetivo original. Se não atender, pede para refazer. Funciona como o controle de qualidade da equipe.

```
Você → Orquestrador ─┬─→ Trabalhador A → Resultado A ─┐
                     ├─→ Trabalhador B → Resultado B ─→ Avaliador → Resultado Final → Você
                     └─→ Trabalhador C → Resultado C ─┘
```

---

## O que agentes já fazem hoje

Aqui está o que é realidade hoje, não ficção científica:

### Análise de documentos em volume

Você envia 50 laudos técnicos. O agente lê todos, identifica os padrões e monta um resumo executivo em minutos. O que levaria dias, leva minutos.

### Pesquisa e comparação

Você pede uma comparação de fornecedores, materiais ou tecnologias. O agente navega na web, coleta informações e monta uma tabela comparativa com fontes.

### Automação de relatórios recorrentes

Com acesso aos seus arquivos, um agente pode coletar dados, fazer cálculos e gerar relatórios automaticamente — sem você precisar montar a planilha toda semana.

### Construção de software em múltiplas partes

Para projetos mais avançados: um agente escreve o banco de dados, outro escreve a interface, um terceiro escreve os testes. O orquestrador integra tudo.

!!! warning "Honestidade sobre os limites"
    Agentes são poderosos, mas não são infalíveis. Eles podem cometer erros — especialmente em tarefas que exigem julgamento humano, nuances culturais, ou dados muito específicos do seu contexto. **Sempre revise o resultado antes de usar.**

---

## Como manter o controle

O modelo mais prático para quem está começando é o de **autonomia supervisionada**:

1. **Você define o objetivo** — claro e específico
2. **O agente trabalha** — executa as tarefas de forma autônoma
3. **Você aprova nos pontos de decisão** — antes de ações irreversíveis (enviar um email, deletar algo, publicar um documento)
4. **Você revisa o resultado final**

Pense em si mesmo como o **gerente de obras** que não está presente a todo momento, mas que precisa assinar antes de cada etapa crítica.

!!! tip "Regra prática"
    Quanto mais irreversível a ação, mais você deve supervisionar de perto. Deixe o agente ser autônomo em tarefas de pesquisa e análise. Supervisione em ações que envolvam publicar, enviar, deletar ou gastar dinheiro.

---

## Como usar na prática hoje

Você não precisa ser programador para usar agentes. As ferramentas abaixo permitem isso de forma acessível:

### Claude.ai — Projetos

O Claude permite criar **Projetos** com contexto persistente. É um agente que lembra das suas instruções anteriores e do seu contexto de trabalho. Muito bom para trabalho intelectual recorrente — análises, resumos, rascunhos de documentos.

### Claude Code

Para quem já configurou o ambiente no Primeiros Passos: o Claude Code é um agente que trabalha diretamente nos seus arquivos, executa código, navega na web e coordena subtarefas. É o estado da arte em 2025 para AI coding.

### Ferramentas de automação no-code

**Make** (antigo Integromat) e **Zapier** permitem criar fluxos automáticos sem código: quando tal evento acontece, tal ação é executada. Para tarefas simples e repetitivas, funcionam muito bem.

---

## Exercício prático

!!! tip "Você já tem um agente disponível"
    O Claude.ai no modo Projeto é um agente com contexto persistente. Vamos usar.

**O exercício:**

1. Acesse [claude.ai](https://claude.ai){ target=_blank } e clique em **"Novo Projeto"**
2. Na descrição do projeto, adicione contexto sobre o seu trabalho (sua área, tipos de tarefas, preferências de comunicação)
3. Agora peça ao Claude uma tarefa de múltiplas etapas:

!!! example "Exemplo de tarefa para o agente"
    ```
    Preciso de ajuda com uma tarefa de pesquisa e síntese.

    Objetivo: Montar um resumo executivo sobre as tendências
    de [sua área de atuação] para 2025-2026.

    O resumo deve incluir:
    1. As 3 principais tendências do setor
    2. Para cada tendência: impacto prático e exemplo concreto
    3. Uma recomendação de ação para um profissional
       que quer se preparar

    Formato: documento de 1 página, linguagem executiva.
    ```

4. Observe como o Claude decompõe a tarefa e entrega um resultado mais estruturado dentro do contexto do Projeto.

---

## Resumo

- **Agentes** são IAs que agem de forma autônoma usando ferramentas — chatbots apenas respondem
- O padrão dominante: **Orquestrador → Trabalhadores → Avaliador**
- Você é o **diretor**: define objetivos, aprova nas decisões críticas, revisa o resultado
- **Autonomia supervisionada** é o modelo prático: liberdade para análise, supervisão em ações irreversíveis
- Disponível hoje: Claude Projetos, Claude Code, Make, Zapier

---

## Próximo passo

Você construiu um app, entende como os agentes funcionam. Agora vem a parte mais satisfatória: **colocar o seu trabalho no mundo**. No Módulo 6, você vai publicar seu app para que qualquer pessoa possa acessar — de graça, sem servidor, sem contrato de hospedagem.

[Módulo 6: Deploy e Lançamento :material-arrow-right:](06-deploy.md){ .md-button .md-button--primary }
