# -

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

**c)** Ao clicar no botão, o método `Incrementar()` é executado, altera o valor da variável e a interface é atualizada.

---

## Exercício 4 — Comunicação entre Componentes

**a)** Utilizamos **`[Parameter]`** na propriedade do componente filho.

**b)** O componente pai pode passar um título para o componente filho:

```razor
<CartaoProduto Titulo="Notebook" />
```

E o filho recebe o valor através de:

```csharp
[Parameter]
public string Titulo { get; set; }
```

---

## Exercício 5 — Desafio de Pensamento Arquitetural

**a)** `Console.ReadLine()` bloqueia a execução esperando uma entrada do usuário, algo que não funciona dessa maneira em aplicações web.

**b)** O Blazor utiliza um modelo **orientado a eventos**, como `@onclick`, para executar ações quando o usuário interage com a página.
