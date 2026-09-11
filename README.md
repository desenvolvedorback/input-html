# 📋 Guia de Campos de Formulário — HTML5

Projeto desenvolvido para demonstrar e servir como referência dos principais **campos de formulário disponíveis no HTML5**, apresentando diferentes tipos de `<input>`, além de elementos como `<textarea>`, `<select>` e `<datalist>`.

O projeto reúne os campos em categorias para facilitar o estudo e a consulta durante o desenvolvimento de páginas web.

---

## 🚀 Tecnologias utilizadas

* HTML5
* CSS3

---

## 📁 Estrutura do projeto

```text
guia-formularios/
├── index.html
└── style.css
```

---

## 📝 Sobre o projeto

A página apresenta uma coleção de campos de formulário organizados em diferentes categorias:

1. Entradas de texto e dados gerais
2. Números e seleção numérica
3. Data e horário
4. Seleção e opções
5. Arquivos, cores e outros
6. Botões

O objetivo é demonstrar na prática como diferentes elementos e atributos de formulários HTML podem ser utilizados.

---

# 1. ✏️ Entradas de Texto e Dados Gerais

### `text`

Campo para entrada de texto simples.

```html
<input type="text" id="text" placeholder="Ex: João da Silva">
```

Utilizado para informações como nomes, títulos e textos curtos.

### `password`

Campo destinado à entrada de senhas.

```html
<input type="password" id="password" placeholder="Digite sua senha">
```

Normalmente oculta os caracteres digitados.

### `email`

Campo para endereços de e-mail.

```html
<input type="email" id="email" placeholder="Usuario@dominio.com">
```

O navegador pode realizar uma validação básica do formato do e-mail.

### `url`

Campo para endereços de sites.

```html
<input type="url" id="url" placeholder="https://exemplo.com.br">
```

### `tel`

Campo para números de telefone.

```html
<input type="tel" id="tel" placeholder="+55 (11) 99999-9999">
```

### `search`

Campo destinado a pesquisas.

```html
<input type="search" id="search" placeholder="O que você procura?">
```

### `textarea`

Permite inserir textos com múltiplas linhas.

```html
<textarea
    id="textarea"
    rows="4"
    placeholder="Escreva sua mensagem aqui..."
></textarea>
```

É muito utilizado para mensagens, comentários e descrições.

---

# 2. 🔢 Números e Seleção Numérica

### `number`

Permite inserir valores numéricos.

```html
<input
    type="number"
    id="number"
    min="0"
    max="100"
    step="1"
>
```

Principais atributos:

* `min` → valor mínimo
* `max` → valor máximo
* `step` → intervalo entre os valores

### `range`

Cria um controle deslizante.

```html
<input
    type="range"
    id="range"
    min="0"
    max="100"
    step="1"
    value="50"
>
```

Pode ser utilizado para representar valores dentro de um intervalo.

---

# 3. 📅 Data e Horário

### `date`

Permite selecionar uma data.

```html
<input type="date" id="date">
```

### `time`

Permite selecionar um horário.

```html
<input type="time" id="time">
```

### `datetime-local`

Permite selecionar data e horário.

```html
<input type="datetime-local" id="datetime-local">
```

### `month`

Permite selecionar um mês.

```html
<input type="month" id="month">
```

### `week`

Permite selecionar uma semana.

```html
<input type="week" id="week">
```

---

# 4. ☑️ Seleção e Opções

## Radio

O `radio` permite selecionar **uma opção dentro de um grupo**.

```html
<input type="radio" name="radio" value="opcao1">
Masculino

<input type="radio" name="radio" value="opcao2">
Feminino

<input type="radio" name="radio" value="opcao3">
Outro
```

Para que funcionem como um grupo de escolha única, os campos devem possuir o mesmo atributo `name`.

---

## Checkbox

O `checkbox` permite selecionar **uma ou várias opções**.

```html
<input type="checkbox" name="checkbox" value="html">
HTML

<input type="checkbox" name="checkbox" value="css">
CSS

<input type="checkbox" name="checkbox" value="javascript">
JavaScript
```

---

## Select

Cria uma lista suspensa de opções.

```html
<select id="select" name="select">
    <option value="">Selecione uma opção</option>
    <option value="opcao1">Opção 1</option>
    <option value="opcao2">Opção 2</option>
    <option value="opcao3">Opção 3</option>
</select>
```

---

## Select múltiplo

Permite selecionar várias opções.

```html
<select id="select-multiple" multiple size="3">
    <option value="opcao1">Módulo 1</option>
    <option value="opcao2">Módulo 2</option>
    <option value="opcao3">Módulo 3</option>
</select>
```

O atributo `multiple` permite múltiplas seleções.

---

## Datalist

Cria sugestões para um campo de entrada.

```html
<input list="sugestoes" id="datalist-input">

<datalist id="sugestoes">
    <option value="Python">
    <option value="Java">
    <option value="C#">
    <option value="PHP">
    <option value="TypeScript">
</datalist>
```

É útil para criar campos com **autocompletar/sugestões**.

---

# 5. 🎨 Arquivos, Cores e Outros

### Color

Permite selecionar uma cor.

```html
<input type="color" id="color" value="#ff0000">
```

### File

Permite selecionar um arquivo do dispositivo.

```html
<input type="file" id="file">
```

É utilizado em formulários que precisam receber arquivos do usuário.

### Hidden

Cria um campo que não é exibido visualmente.

```html
<input
    type="hidden"
    id="hidden"
    name="hidden"
    value="valor_oculto"
>
```

Pode ser utilizado para enviar valores adicionais junto ao formulário.

### Readonly

Cria um campo que pode ser visualizado, mas não editado pelo usuário.

```html
<input
    type="text"
    value="Valor somente para leitura"
    readonly
>
```

### Submit

Cria um botão para enviar o formulário.

```html
<input
    type="submit"
    value="Enviar"
>
```

---

# 6. 🔘 Botões

### Button

Cria um botão genérico.

```html
<input
    type="button"
    value="Clique Aqui"
>
```

Por si só, não envia o formulário. Normalmente é utilizado junto com JavaScript para executar alguma ação.

### Reset

Limpa/restaura os valores dos campos do formulário.

```html
<input
    type="reset"
    value="Limpar Formulário"
>
```

### Image

Cria um botão de envio utilizando uma imagem.

```html
<input
    type="image"
    src="imagem.png"
    alt="Botão de Imagem"
>
```

Quando utilizado dentro de um formulário, funciona como um botão de envio.

---

# 🧩 Principais tipos de `<input>`

| Tipo             | Utilização                |
| ---------------- | ------------------------- |
| `text`           | Texto simples             |
| `password`       | Senhas                    |
| `email`          | E-mail                    |
| `url`            | Endereços de sites        |
| `tel`            | Telefone                  |
| `search`         | Pesquisa                  |
| `number`         | Números                   |
| `range`          | Intervalo numérico        |
| `date`           | Data                      |
| `time`           | Horário                   |
| `datetime-local` | Data e horário            |
| `month`          | Mês                       |
| `week`           | Semana                    |
| `radio`          | Escolha única             |
| `checkbox`       | Múltiplas escolhas        |
| `color`          | Seleção de cor            |
| `file`           | Upload de arquivo         |
| `hidden`         | Campo oculto              |
| `submit`         | Envio do formulário       |
| `button`         | Botão genérico            |
| `reset`          | Limpar formulário         |
| `image`          | Botão de envio com imagem |

---

# 🏗️ Elementos HTML utilizados

Além dos diferentes tipos de `input`, o projeto utiliza:

* `<form>` → define o formulário
* `<fieldset>` → agrupa campos relacionados
* `<legend>` → define o título de um grupo
* `<label>` → identifica um campo
* `<textarea>` → entrada de texto com várias linhas
* `<select>` → lista de opções
* `<option>` → opção de um `<select>`
* `<datalist>` → lista de sugestões
* `<input>` → principal elemento para entradas de dados

---

# ⚙️ Formulário

O projeto utiliza:

```html
<form action="#" method="post">
```

### `action`

Define para onde os dados do formulário serão enviados.

### `method`

Define o método HTTP utilizado no envio.

Neste projeto:

```html
method="post"
```

---

# 🎯 Objetivo

Este projeto foi desenvolvido como uma **atividade prática de HTML5**, com o objetivo de estudar e consultar os principais campos utilizados em formulários.

A página também pode funcionar como uma pequena **referência rápida para desenvolvedores**, permitindo visualizar diferentes tipos de entrada e seus respectivos comportamentos.

---

## 👨‍💻 Autor

**Davi Leonardo**

Projeto desenvolvido para estudos e prática de desenvolvimento web.
