---
description: Qual o critério para realizar vinculo de produto?(importação de XML)
---

# Vinculo de produto?(importação de XML)?

Os critérios para vínculo de produto devem ser analisados:

* verifica pelo código de barra, se achar, já vincula o produto.
* caso nao ache, procure pelo codigo do produto, se achar, ja vincula o prodto
* caso nao ache, procura nas notas antigas ja aceitas, pra o mesmo fornencedor, se o codigo do item bate se achar algum produto antigo, para o mesmo fornecedor com o mesmo codigo do item, entao ele vincula.
* caso nao ache o item e a opção de cadastrar produto esteja habiltiada, então ele cadastra o produto e ja faz o vinculo automaticamente nesse novo produto cadastrado.

Caso seja realizada entrada de uma nota e um produto seja vinculado a outro divergente, realizar analise dos critérios e relaizar o procedimento de correção:

Menu Estoque > produto

consultar código EAN, código do produto.

Menu Movimento> entrada de NF-e

consultar o produto pela descrição/nome que ja estava cadastrado. Na tela de entrada de mercadoria, encontrar a nota e verificar se o codigo dele era o mesmo deste produto novo. desvincular o item da nota nova, salvar.

voltar em Menu Estoque > produto

criar o produto manual para depois voltar na nota e vincula-lo corretamente.
