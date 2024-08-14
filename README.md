# Sobre algumas propriedades do CSS

## Propriedades Utilizadas no Seletor Universal

### `box-sizing: border-box;`

- **Descrição:** Inclui o conteúdo, a borda e o preenchimento. Isso significa que a largura e altura da caixa representam o tamanho total, diferente do `content-box`.

### `outline: none;`

- **Descrição:** Remove as bordas de foco padrão que aparecem em elementos focados, como botões ou campos de entrada.

### `border: none;`

- **Descrição:** Remove bordas indesejadas, como bordas padrão aplicadas por navegadores ou estilos herdados.

### `text-transform: capitalize;`

- **Descrição:** Torna a primeira letra de cada palavra maiúscula.

### `transition: 0.2s linear;`

- **Descrição:** Cria uma animação suave para a mudança de elementos, como a mudança de tamanho.
- **Nota:** Embora útil, não é recomendado aplicar a transição em todos os estilos, pois pode reduzir a performance do site.

---

## Propriedades Aplicadas em Elementos

### `text-shadow: <deslocamento-horizontal> <deslocamento-vertical> <desfoque> <cor>;`

#### Exemplo:

```css
text-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
```

#### Descrição dos Valores:

- **Deslocamento Horizontal:** O primeiro valor define o deslocamento da sombra na direção horizontal. Um valor positivo desloca a sombra para a direita, e um valor negativo para a esquerda. No exemplo, `0` significa que não há deslocamento horizontal.
- **Deslocamento Vertical:** O segundo valor define o deslocamento da sombra na direção vertical. Um valor positivo desloca a sombra para baixo, e um valor negativo para cima. No exemplo, `5px` desloca a sombra 5 pixels para baixo.
- **Desfoque:** O terceiro valor define o raio de desfoque da sombra. Um valor maior cria uma sombra mais difusa e suave, enquanto um valor de `0` cria uma sombra nítida e sem desfoque. No exemplo, `10px` cria um desfoque de 10 pixels.
- **Cor:** O quarto valor define a cor da sombra. Pode ser especificada usando cores hexadecimais, valores RGB ou RGBA. No exemplo, `rgba(0, 0, 0, 0.2)` define uma sombra preta com 20% de opacidade.

#### Notas:

- **Mínimo Requerido:** O mínimo que precisa ser declarado é pelo menos o deslocamento horizontal e vertical, para que a sombra seja visível. O desfoque e a cor são opcionais, mas a ausência de um valor de desfoque resulta em uma sombra nítida.

---

### `grid-template-columns: repeat(auto-fit, minmax(270px, 1fr));`

- **Aplicação:** Utilizada na tag que define o display grid.

#### Descrição dos Valores:

- **auto-fit:** Ajusta o número de colunas para preencher o contêiner. Se houver espaço disponível, ajusta o número de colunas para se adequar ao espaço.
- **minmax(270px, 1fr):**
  - **270px:** O tamanho mínimo de cada coluna. Se não houver espaço suficiente, a coluna não ficará menor que 270 pixels.
  - **1fr:** O tamanho máximo de cada coluna. `1fr` faz com que cada coluna ocupe uma fração do espaço disponível, distribuído igualmente entre as colunas.

#### Como Utilizar:

- **Criação de Layout Responsivo:** Esse código é útil para criar layouts responsivos onde as colunas se ajustam automaticamente com base no tamanho do contêiner. Se o contêiner for redimensionado, o número de colunas mudará para se ajustar ao novo tamanho, sem deixar colunas muito pequenas ou muito grandes.
- **Design Flexível:** Ao definir um mínimo de 270px e um máximo de 1fr, você garante que as colunas não fiquem menores que 270px, mas podem crescer para preencher o espaço disponível. Isso resulta em um design que se adapta ao tamanho da tela ou ao contêiner pai.
- **Espaçamento Automático:** Se o espaço disponível for grande, `auto-fit` adicionará mais colunas conforme necessário, preenchendo o espaço extra de maneira eficiente.
