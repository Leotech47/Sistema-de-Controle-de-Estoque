---

## Explicação do Código

Este código Python é um **sistema básico de verificação de estoque** que determina se um produto específico está disponível em uma lista pré-definida de itens. Ele simula como uma loja poderia rapidamente checar a existência de um produto.

Veja como ele funciona:

1.  **Lista de Estoque (`estoque`):** O código começa definindo uma `lista` chamada `estoque`. Essa lista atua como o inventário da loja, contendo os nomes dos produtos que estão atualmente disponíveis para venda, como "Camiseta", "Calça", "Tênis", etc.

2.  **Entrada do Usuário (`produto = input().strip()`):**
    * A linha `input()` pede ao usuário (neste caso, o funcionário da loja) para digitar o **nome do produto** que ele deseja verificar.
    * O método `.strip()` é importante aqui: ele remove quaisquer espaços em branco que o usuário possa ter digitado acidentalmente no início ou no fim do nome do produto (por exemplo, " Camiseta " se torna "Camiseta"). Isso garante que a comparação seja precisa.

3.  **Verificação no Estoque (`if produto in estoque:`):**
    * Esta é a parte central da lógica. Ela usa o operador `in` para verificar se o `produto` digitado pelo usuário **existe como um item** dentro da lista `estoque`.
    * Se o produto for encontrado na lista, a condição é **verdadeira**, e o código dentro do bloco `if` é executado.
    * Se o produto *não* for encontrado na lista, a condição é **falsa**, e o código dentro do bloco `else` é executado.

4.  **Saída (`print`):**
    * Se o produto estiver no estoque (`if`), o programa imprime a mensagem "**Produto disponível**".
    * Se o produto não estiver no estoque (`else`), o programa imprime a mensagem "**Produto esgotado**".

---

## Exemplos de Aplicação Prática

Esse tipo de lógica simples, que verifica a existência de um item em uma coleção, é fundamental e aparece em várias situações do dia a dia, mesmo que de forma mais complexa.

1.  **Verificação de Disponibilidade em uma Loja Online:**
    * **Cenário:** Um cliente está comprando em um e-commerce e clica em um produto.
    * **Aplicação:** O sistema de fundo verifica se aquele produto (`produto`) está na lista de itens em estoque (`estoque`). Se estiver, mostra "Adicionar ao Carrinho"; se não, mostra "Produto Indisponível" ou "Fora de Estoque". É a mesma lógica, mas com uma interface mais bonita.

2.  **Gerenciamento de Lista de Presença em Eventos:**
    * **Cenário:** Em uma conferência, um funcionário na entrada precisa verificar se a pessoa que chegou está na lista de convidados.
    * **Aplicação:** O funcionário digita o nome do participante (ou escaneia um código que corresponde ao nome), e o sistema compara esse nome com uma lista de nomes cadastrados (`estoque` seria a lista de convidados). Se o nome estiver na lista, permite a entrada; caso contrário, nega.

3.  **Controle de Acesso em Bibliotecas ou Videolocadoras (Antigas):**
    * **Cenário:** Um bibliotecário precisa saber se um livro específico está disponível para empréstimo ou se já foi retirado.
    * **Aplicação:** O bibliotecário digita o título do livro. O sistema verifica se o livro está na lista de "livros disponíveis no acervo" (`estoque`). Se sim, o livro pode ser emprestado; se não, ele está "emprestado" ou "esgotado" (no sentido de não disponível).

---

Conseguiu visualizar como essa verificação básica pode ser útil em diferentes contextos?
