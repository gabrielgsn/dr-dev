---
icon: material/cloud-upload-outline
---

# Módulo 6: Publicar e Lançar

!!! info "Tempo estimado: 30 minutos"

## O que você vai aprender

- O que significa "fazer deploy" (colocar um app na internet)
- Como publicar seu app de graça em menos de 10 minutos
- O que é o GitHub e por que ele é o ponto central do processo
- Como garantir que o seu app se atualize automaticamente

---

## A analogia da loja

Construir um app é como montar uma loja. Você comprou as prateleiras, organizou os produtos, treinou os funcionários. Está tudo pronto internamente.

Mas a loja ainda está fechada. Ninguém sabe que ela existe. Nenhum cliente pode entrar.

**Fazer deploy é abrir as portas.**

É o passo que transforma o seu app de "arquivo no computador" em "endereço na internet que qualquer pessoa pode acessar do celular".

!!! tip "Boas notícias"
    Esse processo, que antigamente exigia configurar servidores, contratar hospedagem e mexer em arquivos de configuração complexos, hoje leva menos de 10 minutos — e é gratuito.

---

## As duas situações

Dependendo de como você construiu seu app no Módulo 4, o caminho é diferente:

### Situação A: Você usou o Lovable

O Lovable já publica automaticamente. Clique em **"Share"** ou **"Publish"** — você recebe um link. Pronto. Seu app já está na internet.

Se quiser um endereço personalizado (como `www.seuapp.com.br`) em vez do link automático do Lovable, siga para a seção "Domínio personalizado" mais abaixo.

### Situação B: Você quer publicar via GitHub

Se você está usando Cursor, Claude Code, ou qualquer ferramenta que gera arquivos locais, o fluxo de publicação usa GitHub + Vercel. Esse é o padrão da indústria em 2025 e funciona de forma completamente automática depois de configurado uma vez.

---

## O que é o GitHub?

Pense no GitHub como um **armário de escritório inteligente** para o seu código.

Todo arquivo tem histórico: quem alterou, quando, o que mudou. É como um registro de revisões de projeto, mas automático e completo.

O mais importante: quando você guarda uma versão nova do código no GitHub, **o app na internet atualiza automaticamente**. Você mexeu no app → salvou → o site já está atualizado. Sem precisar fazer nada mais.

!!! tip "Você já tem uma conta no GitHub"
    Se você seguiu o guia de Primeiros Passos, já criou sua conta no GitHub lá. Essa mesma conta é usada aqui.

---

## Publicando com Vercel

O Vercel é a plataforma mais popular para publicar apps em 2025. É gratuito para uso pessoal e se conecta ao seu GitHub em um clique.

### Por que o Vercel?

- Gratuito para projetos pessoais
- Integração direta com GitHub
- Cada vez que você atualiza o código, o site atualiza automaticamente
- Funciona para qualquer tipo de site ou app moderno

### Passo a passo

**Passo 1:** Acesse [vercel.com](https://vercel.com){ target=_blank } e clique em **"Sign Up"**

**Passo 2:** Escolha **"Continue with GitHub"** — isso conecta o Vercel à sua conta do GitHub

**Passo 3:** Clique em **"Add New Project"** → **"Import Git Repository"**

**Passo 4:** Escolha o repositório do seu app na lista

**Passo 5:** Clique em **"Deploy"** — o Vercel lê o código e publica em menos de 60 segundos

!!! success "Resultado"
    Você recebe um endereço como `seu-app.vercel.app`. Esse endereço funciona no computador, no celular, em qualquer lugar do mundo.

---

## Atualização automática

Depois de publicar uma vez, o processo de atualização é automático:

```
Você muda algo no app
        ↓
Salva no GitHub (git push)
        ↓
Vercel detecta a mudança
        ↓
Publica a nova versão automaticamente
        ↓
Em menos de 60 segundos, o site está atualizado
```

Não precisa fazer login no Vercel de novo. Não precisa clicar em nada. É como ter um funcionário que monitora o armário e atualiza a vitrine da loja automaticamente sempre que você muda o estoque.

---

## Domínio personalizado (opcional)

Se você quiser um endereço profissional como `minhaferramenta.com.br` em vez de `minhaferramenta.vercel.app`:

1. Compre um domínio — [registro.br](https://registro.br){ target=_blank } para `.com.br`, ou [namecheap.com](https://namecheap.com){ target=_blank } para `.com`
2. No painel do Vercel, vá em **Settings → Domains**
3. Adicione seu domínio
4. O Vercel mostra as configurações DNS para copiar no seu provedor
5. Em até 24 horas, o domínio personalizado já funciona

!!! info "Custo"
    Um domínio `.com.br` custa em torno de R$ 40/ano. O `.com` internacional custa cerca de US$ 10/ano. A hospedagem no Vercel é gratuita.

---

## Alternativa: Netlify

O Netlify é uma alternativa ao Vercel com funcionalidades muito similares. Ambos são excelentes.

| | Vercel | Netlify |
|---|--------|---------|
| **Plano gratuito** | Generoso | Generoso |
| **Facilidade** | ⭐⭐⭐ | ⭐⭐⭐ |
| **Deploy automático** | Sim | Sim |
| **Melhor para** | React/Next.js | Qualquer site estático |

**Recomendação:** Comece com o Vercel. Se tiver alguma razão específica para o Netlify, é igualmente fácil de usar.

---

## Exercício prático

!!! tip "Publique o app que você criou no Módulo 4"

**Se você usou o Lovable:**

1. Abra seu projeto no Lovable
2. Clique em **"Share"** ou **"Publish"**
3. Copie o link gerado
4. Teste no celular — funciona?

**Se você quer publicar via Vercel:**

1. Certifique-se que seu código está no GitHub
2. Acesse [vercel.com](https://vercel.com){ target=_blank } e conecte sua conta GitHub
3. Importe o repositório e clique em Deploy
4. Aguarde os 60 segundos e acesse o link gerado

**Independente do caminho:**

- Envie o link para uma pessoa
- Observe como ela usa o app
- Anote o que a confundiu ou o que achou difícil
- Use esses feedbacks para melhorar o app — mais um ciclo de refinamento!

---

## Resumo

- **Deploy** é o passo que abre o app para o mundo — transforma "arquivo no computador" em "site na internet"
- **Lovable** publica com um clique — mais simples para iniciantes
- **Vercel + GitHub** é o padrão da indústria — automático, gratuito, robusto
- Uma vez configurado, qualquer atualização no código **publica automaticamente**
- Domínio personalizado é opcional e custa ~R$ 40/ano

---

## Próximo passo

Você construiu, você publicou. Agora: como **se manter relevante** num campo que muda toda semana? No Módulo 7, você vai montar uma rotina simples e sustentável para acompanhar as novidades sem se afogar em informação.

[Módulo 7: Mantendo-se Atualizado :material-arrow-right:](07-atualizado.md){ .md-button .md-button--primary }
