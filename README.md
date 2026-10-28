# Desafio: Login e Cadastro com Tailwind CSS

Neste desafio você vai criar **duas páginas**: uma tela de **Login** e uma tela de **Cadastro**, usando só HTML e Tailwind CSS (sem escrever nenhuma linha de CSS!).

> 💡 Se é sua primeira vez com Tailwind, tudo bem. A ideia é aprender **procurando na documentação** e **testando**. Errar faz parte!

---

## 🎯 O que você precisa entregar

Dois arquivos:

- `login.html`
- `cadastro.html`

### Como a página de Login deve ficar

- Fundo da página **cinza bem clarinho**
- Um **cartão branco** bem no **centro da tela** (na horizontal e na vertical)
- O cartão tem **borda fina cinza** e **cantos arredondados**
- Dentro do cartão, de cima para baixo:
  1. Título **"Entrar"** (maior e em negrito) e, abaixo, o subtítulo **"Acesse sua conta"** (menor e cinza), os dois centralizados
  2. Campo **E-mail** (o texto do rótulo fica em cima do campo)
  3. Campo **Senha**
  4. Botão **"Entrar"**: fundo escuro, texto branco, cantos arredondados, e que **fica um pouco mais claro quando o mouse passa por cima**
  5. Texto **"Não tem conta? Cadastre-se"**, onde "Cadastre-se" é um link para a página de cadastro e ganha **sublinhado** quando o mouse passa por cima
- Todos os itens têm o **mesmo espaçamento** entre si

### Como a página de Cadastro deve ficar

**Igualzinha** à de login, só que:

- Título: **"Criar conta"** / Subtítulo: **"Preencha seus dados"**
- Tem um campo a mais no começo: **Nome**
- Botão: **"Cadastrar"**
- Rodapé: **"Já tem conta? Entrar"** (com link para o login)

### Detalhes extras (para caprichar ✨)

- Quando você clica em um campo (foco), a **borda do campo fica escura**
- O texto de exemplo dentro do campo (placeholder) fica **cinza claro**
- No **celular**, o cartão ocupa **a largura toda**. Em telas **maiores**, ele tem uma **largura fixa** (por volta de 384px)
- O cursor vira uma **mãozinha** em cima do botão

---

## 🚀 Passo a passo sugerido

### 1. Prepare o arquivo

Crie o `login.html` com a estrutura básica de HTML e coloque esta linha dentro do `<head>` para o Tailwind funcionar:

```html
<script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
```

Para testar se funcionou, coloque `class="bg-red-500"` no `<body>`. Ficou vermelho? Então está tudo certo! (Depois apague isso 😄)

📖 [Play CDN do Tailwind](https://tailwindcss.com/docs/installation/play-cdn)

### 2. Monte o HTML primeiro, sem nenhuma classe

Antes de estilizar, escreva só o HTML. Pense:

- Qual tag faz sentido para agrupar campos e um botão de envio? (dica: começa com **f**)
- Como ligar um texto ao seu campo? (dica: a tag `<label>` pode **envolver** o `<input>`)
- Qual `type` de input usar para e-mail? E para senha?
- Como fazer o botão enviar o formulário?

Abra no navegador. Vai estar feio, e é assim mesmo!

### 3. Estilize o fundo e centralize o cartão

- Dê uma cor de fundo para o `<body>`
- Para centralizar algo no meio da tela, você vai precisar de **Flexbox** no `<body>`
- ⚠️ Pegadinha: o `<body>` só tem a altura do conteúdo. Para centralizar **na vertical**, ele precisa ter **pelo menos a altura da tela**. Procure por "min-height" na documentação.

📖 [Display flex](https://tailwindcss.com/docs/display) · [Justify content](https://tailwindcss.com/docs/justify-content) · [Align items](https://tailwindcss.com/docs/align-items) · [Min height](https://tailwindcss.com/docs/min-height)

### 4. Transforme o formulário em um cartão

- Fundo branco, borda, cantos arredondados e um respiro interno (padding)
- Para empilhar os itens um embaixo do outro **com o mesmo espaço entre eles**, existe um jeito muito mais fácil do que colocar margem em cada um. Pesquise sobre **`gap`** junto com **`flex-direction`**.

📖 [Background color](https://tailwindcss.com/docs/background-color) · [Border width](https://tailwindcss.com/docs/border-width) · [Border color](https://tailwindcss.com/docs/border-color) · [Border radius](https://tailwindcss.com/docs/border-radius) · [Padding](https://tailwindcss.com/docs/padding) · [Flex direction](https://tailwindcss.com/docs/flex-direction) · [Gap](https://tailwindcss.com/docs/gap)

### 5. Estilize os textos

- Título: tamanho maior e mais "pesado"
- Subtítulo e rodapé: tamanho menor e cor cinza
- Alinhamento centralizado

💡 Dica de cores: o Tailwind tem uma paleta de cinzas chamada **neutral**, que vai de `50` (quase branco) até `950` (quase preto). Use ela em tudo!

📖 [Font size](https://tailwindcss.com/docs/font-size) · [Font weight](https://tailwindcss.com/docs/font-weight) · [Text color](https://tailwindcss.com/docs/color) · [Text align](https://tailwindcss.com/docs/text-align) · [Paleta de cores](https://tailwindcss.com/docs/colors)

### 6. Estilize os campos

- O `<label>` também pode ser um flex em coluna, assim o texto fica em cima do campo
- Dê ao input uma **altura**, um **padding nas laterais**, uma **borda** e **cantos arredondados**
- O navegador coloca um contorno azul quando o campo está em foco. Descubra como **remover esse contorno** e, no lugar, **mudar a cor da borda** quando o campo estiver em foco
- Descubra como mudar a cor do **placeholder**

📖 [Height](https://tailwindcss.com/docs/height) · [Outline style](https://tailwindcss.com/docs/outline-style) · [Estados: hover, focus e outros](https://tailwindcss.com/docs/hover-focus-and-other-states) · [Placeholder](https://tailwindcss.com/docs/hover-focus-and-other-states#placeholder-text)

### 7. Estilize o botão e o link

- Botão: fundo escuro, texto branco, mesma altura dos inputs, cantos arredondados
- Mude a cor do fundo quando o mouse passar por cima (**hover**)
- Troque o cursor para a "mãozinha"
- Link: sublinhado só no hover

📖 [Cursor](https://tailwindcss.com/docs/cursor) · [Text decoration](https://tailwindcss.com/docs/text-decoration-line) · [Hover](https://tailwindcss.com/docs/hover-focus-and-other-states#hover-focus-and-active)

### 8. Deixe responsivo

- O Tailwind é **mobile first**: as classes sem prefixo valem para **todas as telas**, e as classes com prefixo (ex.: `sm:`) valem **a partir de** um certo tamanho
- Então: primeiro faça o cartão ocupar a largura toda, depois use um prefixo para dar uma largura fixa em telas maiores
- Teste diminuindo a janela do navegador ou usando o modo celular do DevTools (`F12` → ícone de celular)

📖 [Design responsivo](https://tailwindcss.com/docs/responsive-design) · [Width](https://tailwindcss.com/docs/width)

### 9. Crie a página de cadastro

Se o login ficou pronto, essa parte é rápida 😉 Pense no que dá para **reaproveitar** e no que muda.

Não esqueça de **ligar uma página na outra** pelos links!

---

## ✅ Checklist final

- [ ] O cartão está centralizado na horizontal **e** na vertical
- [ ] Os itens do cartão têm espaçamento igual entre eles
- [ ] Os rótulos ficam em cima dos campos
- [ ] A borda do campo muda de cor ao clicar nele
- [ ] O botão muda de cor no hover e mostra a mãozinha
- [ ] O link fica sublinhado no hover
- [ ] No celular, o cartão ocupa a largura toda; no computador, tem largura fixa
- [ ] O link do login leva ao cadastro e vice-versa
- [ ] Não escrevi nenhuma linha de CSS, só classes do Tailwind 💪

---

## 🤖 Usando a I.A. como professor particular

A I.A. pode ser uma ótima professora, **desde que você peça para ela te ensinar e não para fazer por você**. Se ela entregar o código pronto, você não aprende, e na hora de fazer sozinho vai travar.

### Regra de ouro

Sempre comece a conversa deixando claro que você quer **aprender**. Copie e cole este prompt inicial:

```text
Estou aprendendo Tailwind CSS pela primeira vez e estou fazendo um exercício
de tela de login. Quero que você seja meu professor particular.

Regras:
- NÃO me dê o código pronto, nem as classes prontas.
- Me explique o conceito e me dê dicas ou perguntas que me façam chegar
  na resposta sozinho.
- Se eu pedir, me indique a página da documentação oficial do Tailwind.
- Use exemplos que NÃO sejam do meu exercício.
- Fale de um jeito simples, pois sou iniciante.
```

### Prompts para quando você travar

**Para entender um conceito:**

```text
Me explica o que é Flexbox como se eu tivesse 12 anos. Não use código
do meu exercício, use um exemplo do dia a dia.
```

```text
Qual a diferença entre margin, padding e gap? Me dê um exemplo visual
(pode ser com desenho em texto) e me pergunte qual eu usaria para
espaçar itens dentro de uma caixa.
```

```text
O que significa "mobile first" no Tailwind? Me explique e depois me faça
uma pergunta para ver se eu entendi.
```

**Para receber uma dica (sem resposta):**

```text
Quero centralizar uma caixa no meio da tela, na horizontal e na vertical,
usando Tailwind. Não me dê as classes. Me diga só quais conceitos eu
preciso pesquisar na documentação.
```

```text
Meu cartão centraliza na horizontal, mas não na vertical. Não me dê a
resposta, me faça perguntas que me ajudem a descobrir o motivo.
```

**Para revisar o seu código:**

```text
Esse é o meu código. Não reescreva ele. Me diga, em forma de lista,
o que pode ser melhorado e por quê, e deixe que eu faço as alterações:

[cole seu código aqui]
```

```text
Explique o que cada classe deste elemento faz, uma por uma:

[cole o elemento aqui]
```

**Para testar o que você aprendeu:**

```text
Me faça 5 perguntas rápidas sobre Tailwind CSS (flex, gap, padding,
cores, hover e responsividade) para eu testar o que aprendi.
Espere eu responder antes de corrigir.
```

> ⚠️ Se a I.A. mesmo assim te mandar o código pronto, **não copie**. Responda: _"Eu pedi para não me dar a resposta. Me dê só uma dica."_

---

## 📚 Links úteis

- [Documentação oficial do Tailwind CSS](https://tailwindcss.com/docs) (use a busca com `Ctrl + K`!)
- [Tailwind Play](https://play.tailwindcss.com/): editor online para testar classes rapidinho
- [Flexbox Froggy](https://flexboxfroggy.com/#pt-br): joguinho para aprender Flexbox (os nomes das propriedades são do CSS, mas o conceito é o mesmo do Tailwind)
- [MDN: formulários em HTML](https://developer.mozilla.org/pt-BR/docs/Learn/Forms)

Bons estudos e mão na massa! 🚀
