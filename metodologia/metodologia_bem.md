# Guia de Referência: Metodologia BEM (Block, Element, Modifier)

A metodologia **BEM** (Bloco, Elemento, Modificador) é um padrão de nomenclatura popular e modular para HTML e CSS. Seu objetivo é ajudar a criar código reutilizável, legível, sustentável e escalável, evitando conflitos de especificidade em projetos web.

---

## 1. Os Três Pilares do BEM

### 🏢 Bloco (`Block`)
* **O que é:** Um componente funcional e independente na página. Pode ser reutilizado em qualquer lugar sem depender de outros elementos ao seu redor.
* **Sintaxe:** `nome-do-bloco` (usando hífens para separar palavras compostas).
* **Exemplos:** `card`, `menu`, `button`, `search-form`.

```html
<!-- Exemplo de Bloco -->
<div class="card">
  ...
</div>
```

---

### 🧩 Elemento (`Element`)
* **O que é:** Uma parte integrante de um **Bloco** que não possui significado semântico/funcional isoladamente. Sempre pertence a um único bloco.
* **Sintaxe:** `bloco__elemento` (separado por **dois underline** `__`).
* **Exemplos:** `card__title`, `menu__item`, `search-form__input`.

```html
<!-- Exemplo de Bloco com Elementos -->
<div class="card">
  <h2 class="card__title">Título do Card</h2>
  <p class="card__description">Descrição breve do conteúdo.</p>
</div>
```

> **Atenção:** Evite encadear elementos (ex: `card__body__title`). A estrutura do BEM deve ser sempre "plana", mantendo a referência direta ao bloco pai (`card__title`).

---

### 🎛️ Modificador (`Modifier`)
* **O que é:** Uma flag ou propriedade usada para alterar a aparência, estado ou comportamento de um Bloco ou Elemento.
* **Sintaxe:** `bloco--modificador` ou `bloco__elemento--modificador` (separado por **dois hífens** `--`).
* **Exemplos:** `button--success`, `card--featured`, `menu__item--active`.

```html
<!-- Exemplo de Bloco e Elemento com Modificadores -->
<button class="button button--large button--success">Enviar</button>

<li class="menu__item menu__item--active">Início</li>
```

---

## 2. Sintaxe e Convenções de Nomenclatura

| Conceito | Separador | Exemplo HTML | Exemplo CSS |
| :--- | :--- | :--- | :--- |
| **Bloco** | N/A | `class="card"` | `.card { ... }` |
| **Elemento** | `__` (Duplo underline) | `class="card__button"` | `.card__button { ... }` |
| **Modificador** | `--` (Duplo hífen) | `class="card--dark"` | `.card--dark { ... }` |
| **Palavras Compostas** | `-` (Hífen simples) | `class="site-header"` | `.site-header { ... }` |

---

## 3. Exemplo Prático Completo

### Estrutura HTML:

```html
<!-- Bloco de perfil/cartão com modificador de tema escuro -->
<article class="profile-card profile-card--dark">
  <img class="profile-card__avatar" src="avatar.jpg" alt="Foto de perfil">
  
  <h3 class="profile-card__name">
    Ana Silva
  </h3>
  
  <p class="profile-card__bio">
    Desenvolvedora Frontend apaixonada pela metodologia BEM.
  </p>
  
  <!-- Reutilizando um bloco genérico 'button' com um modificador específico -->
  <button class="button button--primary profile-card__button">
    Seguir
  </button>
</article>
```

### Estilização CSS:

```css
/* Bloco Principal */
.profile-card {
  border: 1px solid #ddd;
  padding: 16px;
  border-radius: 8px;
  background-color: #ffffff;
}

/* Modificador do Bloco */
.profile-card--dark {
  background-color: #1a1a1a;
  color: #ffffff;
  border-color: #333;
}

/* Elementos */
.profile-card__avatar {
  width: 80px;
  height: 80px;
  border-radius: 50%;
}

.profile-card__name {
  font-size: 1.25rem;
  margin-top: 8px;
}

.profile-card__bio {
  font-size: 0.9rem;
  color: #666;
}

/* Ajuste no elemento específico sob o tema escuro */
.profile-card--dark .profile-card__bio {
  color: #aaa;
}

/* Bloco Independente de Botão */
.button {
  padding: 8px 16px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.button--primary {
  background-color: #007bff;
  color: #ffffff;
}
```

---

## 4. Boas Práticas e Regras de Ouro

1. **Evite seletores aninhados profundos:** Em CSS, prefira estilizar diretamente a classe BEM (`.card__title`) em vez de encadear seletores (`.card .card__title` ou `.card h2`). Isso garante especificidade baixa e uniforme.
2. **Não use BEM para IDs:** O BEM foi desenhado estritamente para ser usado com classes HTML (`class=""`).
3. **Mantenha os componentes independentes:** Um bloco não deve depender de sua posição na página para funcionar corretamente. Avoid utilizar margens externas (`margin`) nas regras de um Bloco isolado; prefira definir o posicionamento no elemento pai ou em classes utilitárias.
4. **Subcomponentes vs. Elementos:** Se uma parte de um Bloco puder ser reutilizada fora dele, ela deve ser transformada em um novo **Bloco** independente em vez de um **Elemento**.

---

## 5. Referências e Leituras Recomendadas

Para mais detalhes e aprofundamento na metodologia, consulte os links abaixo:

* [Documentação Oficial do BEM](https://bem.info/en/) - Guia completo oficial da metodologia e ecossistema.
* [Metodologia BEM para CSS (Medium - Fernanda Leite)](https://medium.com/@fnandaleite/metodologia-bem-para-css-b0d3269b4853) - Artigo em português explicando os conceitos e aplicação prática.
* [Metodologia BEM no CSS (Hashtag Treinamentos)](https://www.hashtagtreinamentos.com/metodologia-bem-no-css-html-e-css) - Tutorial prático introdutório focado em HTML e CSS.