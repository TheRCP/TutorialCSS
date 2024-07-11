## CSS em Acção: Conteúdo Invisível apenas para Utilizadores de Leitor de Ecrã.

### Introdução

A grande maioria das técnicas que tornam o conteúdo da web acessível a leitores de ecrã são **invisíveis** aos utilizadores que fazem uso da visão. O texto alternativo nas imagens (uso do atributo `alt`), a identificação dos cabeçalhos de uma tabela (uso do elemento `<th>`), o sumariar uma tabela (atributo `summary`), assim como a etiquetagem dos campos de um formulário (uso do elemento `<label>`) são alguns dos exemplos de técnicas extremamente úteis para quem usa leitores de ecrã, como é o caso das pessoas cegas. Para os conteúdos web o impacto da utilização destas técnicas, do ponto de vista gráfico, é mínimo ou mesmo nulo.

### Esconder Texto dos Utilizadores Que Usam o Sentido da Visão

Felizmente há formas de resolver os conflitos existentes entre as necessidades e os desejos dos utilizadores que fazem uso do sentido da visão e os desejos e necessidades dos utilizadores de leitor de ecrã. O presente artigo examina algumas das circunstâncias em que, esconder texto dos utilizadores que usam a visão, pode ser benéfico, propondo uma solução que faz com que o `HTML` fique escondido sem comprometer a acessibilidade ou a integridade semântica do documento, permitindo ainda um funcionamento transversal aos navegadores e às plataformas.

### Amostra de Código 1

O seguinte código deverá aparecer na folha de estilo:
```html
<!-- HTML code -->
<div class="hidden">
  This text is hidden from sighted users but visible to screen readers.
</div>
```

```css
/* CSS code */
.hidden {
  position: absolute;
  left: 0px;
  top: -500px;
  width: 1px;
  height: 1px;
  overflow: hidden;
}
```

And so on...