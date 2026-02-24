---
icon: material/rocket-launch-outline
---

# Primeiros Passos

!!! info "Tempo estimado: 30-45 minutos"
    Este guia vai te levar do zero absoluto até ter todas as ferramentas instaladas e prontas para uso. Você só precisa fazer isso **uma vez**.

## Precisa de ajuda? Use o Claude como assistente

Se voce esta perdido ou prefere ter alguem te guiando em tempo real, pode usar o **Claude** (a IA da Anthropic) para te ajudar com todo o processo. Basta acessar [claude.ai](https://claude.ai){ target=_blank }, criar uma conta gratuita, e colar a mensagem abaixo.

!!! example "Copie e cole essa mensagem no Claude"

    ```
    Oi Claude! Preciso da sua ajuda para configurar meu computador para
    programar usando IA. Eu nunca programei na vida, nao tenho nenhuma
    ferramenta instalada (nem Git, nem VS Code, nem Node.js, nem Python),
    e nao tenho conta no GitHub.

    Estou seguindo o guia do site dr.dev
    (https://gabrielgsn.github.io/dr-dev/primeiros-passos/) e preciso
    instalar tudo que esta listado la:

    1. Criar conta no GitHub
    2. Instalar o VS Code
    3. Instalar o Git
    4. Instalar o Node.js
    5. Instalar o Claude Code (a ferramenta de IA no terminal)

    Por favor, me guie passo a passo. Vou te dizendo o que aparece na
    minha tela e voce me diz o que fazer. Fale comigo como se eu fosse
    inteligente mas nunca tivesse mexido com programacao. Meu computador
    e [WINDOWS/MAC - escreva qual e o seu].
    ```

!!! tip "Dica"
    Troque `[WINDOWS/MAC - escreva qual e o seu]` pelo seu sistema operacional (ex: "Windows 11" ou "MacBook"). O Claude vai adaptar as instrucoes para voce.

---

## Visão geral

Antes de começar a criar aplicações com IA, você precisa configurar algumas ferramentas no seu computador. Não se preocupe — é mais simples do que parece.

Aqui está o que vamos instalar e por quê:

| Ferramenta | O que é | Por que você precisa |
|---|---|---|
| **GitHub** | Uma "nuvem" para guardar seus projetos | Salvar e compartilhar o que você criar |
| **VS Code** | Um editor de texto inteligente | Seu "escritório" de trabalho nos projetos |
| **Git** | Sistema de controle de versões | Salvar o histórico do seu trabalho (como um Ctrl+Z poderoso) |
| **Node.js** | Plataforma para rodar programas | Necessário para instalar o Claude Code |
| **Claude Code** | Assistente de IA no terminal | Seu parceiro de trabalho — ele faz o trabalho pesado |

!!! tip "A boa notícia"
    Depois que o **Claude Code** estiver instalado, ele pode te ajudar com praticamente tudo. Você vai conversar com ele em português, e ele vai escrever código, criar arquivos, resolver problemas e explicar o que está acontecendo — passo a passo.

---

## Passo 1: Criar uma conta no GitHub

O GitHub é como um Google Drive para projetos de programação. Você vai usar para guardar e organizar tudo que criar.

1. Acesse [github.com](https://github.com){ target=_blank }
2. Clique em **Sign up** (Cadastrar-se)
3. Preencha com seu e-mail, crie uma senha e escolha um nome de usuário
4. Complete a verificação (vai pedir para resolver um puzzle simples)
5. Confirme seu e-mail (o GitHub vai enviar um código de verificação)

!!! tip "Dica"
    Escolha um nome de usuário simples e profissional — ele vai aparecer nos seus projetos públicos.

Pronto! Deixe a aba aberta, vamos usar depois.

---

## Passo 2: Instalar o VS Code

O VS Code é um editor de texto feito para programação. Pense nele como o "escritório" onde você vai ver e organizar seus arquivos. E mais importante: é onde o Claude Code vai rodar.

1. Acesse [code.visualstudio.com](https://code.visualstudio.com){ target=_blank }
2. Clique no botão grande de **Download** (ele detecta seu sistema automaticamente)
3. Abra o arquivo baixado e siga a instalação padrão (pode manter todas as opções como estão)
4. Abra o VS Code depois de instalar

!!! info "Interface em português"
    Na primeira vez que abrir, o VS Code pode sugerir instalar o pacote de idioma em português. Aceite se preferir — mas o conteúdo técnico na internet é quase todo em inglês, então pode ser útil se acostumar com os termos em inglês também.

---

## Passo 3: Instalar o Git

O Git é um sistema que guarda o histórico de tudo que você faz nos seus projetos. Pense como um "Ctrl+Z" muito poderoso que funciona para o projeto inteiro e permite voltar a qualquer ponto no tempo.

=== "Windows"

    1. Acesse [git-scm.com](https://git-scm.com){ target=_blank }
    2. Clique em **Download for Windows**
    3. Abra o instalador e **mantenha todas as opções padrão** (só clique "Next" até o final)
    4. Clique em **Install** e depois **Finish**

=== "Mac"

    1. Abra o **Terminal** (busque "Terminal" no Spotlight com ++cmd+espaço++)
    2. Digite: `xcode-select --install`
    3. Clique em **Instalar** na janela que aparecer
    4. Aguarde a instalação (pode levar alguns minutos)

!!! warning "Verificação"
    Para confirmar que o Git foi instalado corretamente:

    1. Abra o VS Code
    2. Vá em **Terminal** > **Novo Terminal** (no menu superior)
    3. Digite `git --version` e pressione ++enter++
    4. Deve aparecer algo como `git version 2.xx.x`

### Configurar o Git com seus dados

Ainda no terminal do VS Code, digite esses dois comandos (um de cada vez, trocando pelos seus dados reais):

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
```

!!! tip "Use o mesmo e-mail do GitHub"
    O e-mail aqui deve ser o mesmo que você usou para criar a conta no GitHub no Passo 1.

---

## Passo 4: Instalar o Node.js

O Node.js é uma plataforma que permite rodar programas no seu computador. Você precisa dele para instalar o Claude Code.

1. Acesse [nodejs.org](https://nodejs.org){ target=_blank }
2. Clique no botão de download da versão **LTS** (a versão estável recomendada)
3. Abra o instalador e siga com as opções padrão
4. **Reinicie o VS Code** depois da instalação

!!! warning "Verificação"
    No terminal do VS Code, digite:

    ```bash
    node --version
    ```

    Deve aparecer algo como `v22.x.x` ou superior. Se não aparecer, feche e abra o VS Code novamente.

---

## Passo 5: Instalar o Claude Code

Agora vem a parte mais importante. O Claude Code é um assistente de IA que roda direto no terminal do VS Code. Ele vai ser seu parceiro em todos os projetos — você descreve o que quer em português, e ele executa.

### Instalação

No terminal do VS Code, digite:

```bash
npm install -g @anthropic-ai/claude-code
```

Aguarde a instalação terminar (pode levar 1-2 minutos).

### Primeira execução

Depois de instalar, digite:

```bash
claude
```

Na primeira vez, ele vai abrir o navegador para você fazer login com sua conta da Anthropic.

!!! info "Conta e plano necessários"
    Para usar o Claude Code, você precisa de **uma** destas opções:

    - **Plano Claude Pro ou Max** — assinatura mensal em [claude.ai/settings](https://claude.ai/settings){ target=_blank }. É a opção mais simples.
    - **Créditos de API** — comprados em [console.anthropic.com](https://console.anthropic.com){ target=_blank }. Você paga pelo uso.

    Se você já tem uma conta no claude.ai, o caminho mais fácil é assinar o plano Pro (US$ 20/mês) e usar o login direto.

!!! warning "Verificação"
    Depois de fazer login, o Claude Code vai mostrar uma mensagem de boas-vindas no terminal. Se você vir um cursor esperando sua pergunta, está tudo funcionando!

---

## Passo 6: Sua primeira conversa com Claude Code

Com tudo instalado, é hora de testar! O Claude Code funciona como uma conversa: você descreve o que quer e ele executa.

### Crie uma pasta de projeto

1. No VS Code, vá em **Arquivo** > **Abrir Pasta**
2. Crie uma pasta nova chamada `meu-primeiro-projeto` (em qualquer lugar do seu computador, como a Área de Trabalho)
3. Selecione essa pasta e clique em **Abrir**
4. Abra o terminal (**Terminal** > **Novo Terminal**)
5. Digite `claude` para iniciar o Claude Code

### Faça seu primeiro pedido

Agora você pode conversar em português! Experimente digitar:

!!! example "Primeiro teste"
    ```
    Crie uma página web simples que mostra uma calculadora
    de conversão de metros para pés. Com um campo de entrada
    e o resultado aparecendo automaticamente quando eu digitar.
    ```

O Claude Code vai:

1. **Criar os arquivos** necessários na sua pasta
2. **Escrever todo o código** automaticamente
3. **Explicar o que ele fez** em português

Você pode abrir o arquivo HTML que ele criou (clicando nele no painel lateral do VS Code) e arrastar para o navegador para ver o resultado.

!!! tip "Dica de ouro"
    Você não precisa entender o código. Se algo não ficou como você queria, é só pedir para ele ajustar — igualzinho uma conversa normal. Por exemplo: *"O layout ficou feio, pode melhorar o visual?"* ou *"Quero que converta de pés para metros também."*

### O que mais pedir ao Claude Code

O Claude Code pode fazer muito mais do que criar páginas web. Aqui estão exemplos práticos do que você pode pedir:

**Para aprender:**
```
Explique o que são esses arquivos que você criou.
Para que serve cada um?
```

**Para usar o Git e GitHub:**
```
Me ajude a transformar essa pasta em um repositório Git
e conectar ao meu GitHub. Meu usuário é [seu-usuario].
```

**Para criar ferramentas úteis:**
```
Crie uma planilha interativa que calcula o custo de
uma reforma. Quero campos para área em m², tipo de
acabamento (básico, médio, alto) e região (SP, RJ, MG).
```

**Para resolver dúvidas:**
```
O que é um repositório Git? Me explique de forma simples,
como se eu nunca tivesse programado.
```

---

## Dicas importantes para usar o Claude Code

!!! tip "Seja específico"
    Quanto mais detalhes você der, melhor o resultado. Em vez de *"crie um site"*, diga *"crie um site com uma calculadora que converte metros para pés, com fundo azul escuro e letras brancas"*.

!!! tip "Peça explicações"
    Se o Claude Code fez algo que você não entendeu, pergunte: *"Explique o que você acabou de fazer, em termos simples."* Ele vai te explicar tudo.

!!! tip "Itere sem medo"
    Se o resultado não ficou bom, não desista. Diga o que não gostou e peça ajustes. É normal precisar de 3-5 rodadas de conversa para chegar no resultado ideal.

!!! tip "Use para aprender"
    O Claude Code é um professor paciente. Pergunte *"por que você fez assim?"* ou *"existe uma forma melhor?"* — ele vai te ensinar enquanto trabalha.

---

## Resumo

Agora você tem tudo instalado e configurado:

- [x] **GitHub** — sua conta para guardar projetos na nuvem
- [x] **VS Code** — seu editor de texto para trabalhar nos projetos
- [x] **Git** — controle de versões (histórico do seu trabalho)
- [x] **Node.js** — plataforma necessária para o Claude Code
- [x] **Claude Code** — seu assistente de IA no terminal

!!! success "Parabéns!"
    Você está pronto para começar a trilha de módulos. A partir de agora, o Claude Code vai ser seu companheiro em todos os exercícios e projetos. Quando tiver dúvida sobre qualquer coisa — desde como usar o Git até como criar um aplicativo — é só perguntar a ele.

---

## Próximo passo

Agora que seu ambiente está configurado, comece pela trilha de aprendizado. O Módulo 1 vai te apresentar ao mundo do AI Coding e mostrar o que é possível construir.

[Começar a trilha :material-arrow-right:](modulos/index.md){ .md-button .md-button--primary }
