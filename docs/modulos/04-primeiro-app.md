---
icon: material/rocket-launch-outline
---

# Módulo 4: Seu Primeiro App

!!! info "Tempo estimado: 60 minutos"

## O que você vai aprender

- Como transformar uma ideia em aplicativo funcional, do zero, sem escrever uma linha de código
- Qual ferramenta usar para começar (e por quê)
- O ciclo completo de construção: descrever → gerar → refinar → publicar
- Como lidar quando a IA erra (e ela vai errar)

---

## A analogia do marceneiro

Imagine que você quer uma mesa de madeira personalizada para o seu escritório. Você não precisa saber trabalhar com madeira. Você precisa saber **descrever** o que quer: tamanho, estilo, quantidade de gavetas, cor do acabamento.

O marceneiro faz o trabalho físico. Você faz as decisões.

**Com AI coding é exatamente assim.** Você descreve o aplicativo que quer. A ferramenta gera o código. Você vê o resultado, pede ajustes, e a ferramenta refaz. Não importa que você nunca programou na vida — o que importa é sua capacidade de descrever o que quer com clareza.

!!! tip "Ponto chave"
    O conhecimento que você traz é o mais valioso: você sabe o que o seu app precisa fazer. A ferramenta só sabe como construir. Juntos, vocês chegam lá.

---

## Qual ferramenta usar?

Existem várias ferramentas para construir apps com IA. Para quem está começando, a recomendação é clara:

### :material-star: Lovable — para iniciantes absolutos

**Por que o Lovable?**

- Interface simples: você digita o que quer em português
- Resultado visual imediato: você vê o app se formando em tempo real
- Não precisa instalar nada: funciona no navegador
- Plano gratuito para começar

**O que o Lovable consegue fazer:** sites, dashboards, calculadoras, formulários, listas de tarefas, portfólios, pequenos sistemas internos.

!!! warning "Limite honesto"
    O Lovable é ótimo para protótipos e ferramentas internas. Para sistemas complexos com muitos usuários, você vai precisar de um desenvolvedor. Mas para o seu primeiro app? É perfeito.

**Outras opções:**

| Ferramenta | Melhor para | Dificuldade |
|------------|-------------|-------------|
| Lovable | Iniciantes absolutos | ⭐ Fácil |
| Bolt.new | Apps mais técnicos | ⭐⭐ Médio |
| v0 (Vercel) | Componentes de interface | ⭐⭐ Médio |
| Cursor + Claude | Desenvolvedores | ⭐⭐⭐ Avançado |

---

## O ciclo de construção

Independente da ferramenta, o processo segue sempre o mesmo padrão de 4 etapas. Pense nisso como o ciclo de revisão de um projeto:

```
Descrever → Gerar → Revisar → Refinar
    ↑                              ↓
    └──────────── (repetir) ───────┘
```

**1. Descrever** — Você escreve o que quer construir. Com o máximo de detalhes possível.

**2. Gerar** — A ferramenta constrói a primeira versão do app.

**3. Revisar** — Você olha o resultado. Funciona como esperado? A interface está clara? Algo está faltando?

**4. Refinar** — Você pede ajustes: "Mude a cor", "Adicione esse campo", "Coloque o botão aqui". A ferramenta atualiza.

Repita quantas vezes precisar. Em média, 3 a 5 ciclos resolvem um app simples.

---

## Construindo na prática

Vamos construir um app real: uma **calculadora de orçamento rápido** para uso profissional.

O objetivo é simples — um app onde você insere os dados de um serviço e ele calcula o valor sugerido. Sem planilha, sem papel: uma ferramenta limpa que funciona no celular.

### Passo 1: Acesse o Lovable

Vá para [lovable.dev](https://lovable.dev){ target=_blank } e crie uma conta gratuita.

### Passo 2: Descreva o app

Na tela inicial, há uma caixa de texto. Digite uma descrição clara do que você quer. Aqui está um exemplo que você pode adaptar:

!!! example "Exemplo de prompt inicial"
    ```
    Crie uma calculadora de orçamento profissional simples.

    O usuário deve conseguir:
    - Inserir o nome do serviço
    - Informar as horas estimadas de trabalho
    - Informar o valor por hora (em reais)
    - Adicionar uma margem de lucro (em %)
    - Ver o valor total calculado automaticamente

    Interface limpa, profissional, com botão para "Gerar Orçamento".
    Use cores neutras (branco e azul escuro).
    ```

### Passo 3: Veja a magia acontecer

O Lovable vai gerar o app em alguns segundos. Uma prévia aparece ao lado do seu prompt.

Não se preocupe se não ficou perfeito — essa é a versão 1. Exatamente como um projeto executivo na primeira revisão.

### Passo 4: Refine com pedidos simples

Veja o resultado e peça ajustes em linguagem natural:

!!! example "Exemplos de refinamento"
    - *"Adicione um campo para o nome do cliente"*
    - *"Mude o título para 'Calculadora de Proposta'"*
    - *"Coloque os resultados em destaque, com fonte maior"*
    - *"Adicione um botão para limpar os campos"*

Cada pedido é um novo prompt. A ferramenta atualiza o app e você vê a mudança na hora.

### Passo 5: Publique

Quando estiver satisfeito, clique em **"Publish"** ou **"Share"**. O Lovable gera um link que qualquer pessoa pode abrir no celular ou computador.

Parabéns — você publicou seu primeiro app.

!!! tip "Compartilhe"
    Mande o link para um colega. Ver alguém usar algo que você criou é uma das experiências mais motivadoras nesse processo.

---

## Quando a IA errar

A IA vai errar. Isso é normal e faz parte do processo — não é uma falha sua.

Quando o resultado não for o esperado:

**:material-numeric-1-circle: Seja mais específico.** Em vez de "mude o layout", diga "mova o campo de horas para baixo do campo de serviço". Quanto mais preciso, melhor o resultado.

**:material-numeric-2-circle: Use o histórico da conversa.** Você pode continuar refinando na mesma sessão. A ferramenta lembra do contexto anterior.

**:material-numeric-3-circle: Comece do começo.** Se o app foi numa direção errada, não tem problema recomeçar com um prompt mais refinado. O segundo app sempre fica melhor que o primeiro.

**:material-numeric-4-circle: Descreva o problema com precisão.** *"O cálculo não está correto. Quando coloco 10 horas a R$ 100, o resultado deveria ser R$ 1.000, mas está aparecendo R$ 100."*

!!! warning "Nunca aceite resultados errados sem questionar"
    Especialmente em cálculos. A IA pode gerar código que parece correto visualmente, mas tem uma lógica equivocada. Sempre teste com valores que você conhece o resultado correto.

---

## Exercício prático

!!! tip "Construa algo para você"
    O melhor primeiro app é um que resolve um problema real do seu dia a dia.

**Sugestões para o seu primeiro app:**

- Uma calculadora para uma fórmula que você usa frequentemente no trabalho
- Um formulário de coleta de dados para visitas a campo
- Um checklist digital de inspeção
- Uma página de apresentação profissional
- Um conversor de unidades específico para sua área

**O exercício:**

1. Escolha uma dessas ideias (ou a sua própria)
2. Escreva um prompt descrevendo o app em detalhes
3. Acesse o [Lovable](https://lovable.dev){ target=_blank } e construa
4. Faça pelo menos 3 rodadas de refinamento
5. Publique e compartilhe o link com alguém

---

## Resumo

- **A analogia do marceneiro**: você descreve, a IA constrói. Seu conhecimento de domínio é o diferencial
- **Lovable** é a ferramenta mais acessível para quem está começando
- O ciclo **Descrever → Gerar → Revisar → Refinar** é o coração do processo
- **Erros fazem parte**: refine, seja mais específico, ou recomece
- Em 60 minutos, você pode ter um app funcional e publicado

---

## Próximo passo

Você já sabe construir um app. No **Módulo 5**, você vai aprender a dar um passo além: colocar **múltiplos agentes de IA para trabalhar juntos**, como uma equipe que executa tarefas complexas de forma autônoma enquanto você supervisiona.

[Módulo 5: Agentes de IA :material-arrow-right:](05-agentes.md){ .md-button .md-button--primary }
