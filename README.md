# lista-T01-udwmj
Aluno: Matheus Honorato Leite Teixeira
RA: 1261929133

## Exercício 1 — O Fim do Reino do JavaScript?

**a)** Blazor é um framework da Microsoft que permite criar aplicações web usando **C# e .NET**, aproveitando conhecimentos já adquiridos pelos desenvolvedores.

**b)** A principal vantagem é poder utilizar **C# no desenvolvimento da interface e da lógica**, reduzindo a necessidade de utilizar JavaScript.

---

## Exercício 2 — Blazor Server vs. Blazor WebAssembly

### Cenário A

**Blazor Server**, pois os computadores são antigos e a rede local possui alta velocidade e baixa latência.

### Cenário B

**Blazor WebAssembly**, pois a aplicação é executada no navegador e pode utilizar recursos locais após o carregamento.

---

## Exercício 3 — Anatomia de um Componente Razor

**a)** `@code` é utilizado para colocar o **código C#** dentro de um componente Razor.

**b)** `@quantidade` permite mostrar o valor da variável no HTML. Esse conceito está relacionado à **vinculação de dados (data binding)**.

**c)** Ao clicar no botão, o método `Incrementar()` é executado, altera o valor da variável e a interface é atualizada incrementando +1 no valor da variável.

---

## Exercício 4 — Comunicação entre Componentes

**a)** Utilizamos **`[Parameter]`** na propriedade do componente filho.

**b)** O componente pai `PaginaVendas.razor` passa um título para o componente filho `CartaoProduto.razor` através de um parâmetro.

**PaginaVendas.razor:**

```razor
<h1>Página de Vendas</h1>

<CartaoProduto Titulo="Notebook Dell" />
```

**CartaoProduto.razor:**

```razor
<div>
    <h2>@Titulo</h2>
</div>

@code {
    [Parameter]
    public string Titulo { get; set; }
}
```

Nesse exemplo, o componente `PaginaVendas` envia **"Notebook Dell"** para o componente `CartaoProduto`, que recebe o valor pelo `[Parameter]` e o exibe na tela.


## Exercício 5 — Desafio de Pensamento Arquitetural

**a)** `Console.ReadLine()` é uma lógica bloqueante porque o programa fica parado esperando o usuário digitar alguma coisa. Em uma aplicação web, a página precisa continuar funcionando enquanto aguarda as ações do usuário, então esse modelo de espera não é adequado.

**b)** No Blazor, essa espera é substituída pelo modelo orientado a eventos. A aplicação continua funcionando e, quando o usuário realiza alguma ação, como clicar em um botão, um evento é acionado e executa o método correspondente.

Por exemplo, `@onclick` detecta o clique e chama uma função, sem precisar deixar o programa parado esperando pela ação do usuário.
