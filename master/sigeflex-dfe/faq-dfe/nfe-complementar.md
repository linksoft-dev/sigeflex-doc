---
description: manual para emissão de NF-e complementar
---

# Nota Fiscal Complementar

**A NF-e complementar serve para “complementar” dados de um ou mais produtos que porventura vieram a serem emitidos com dados inferiores aos reais. A idéia é que a NF-e normal + NF-e complementar = operação real.**

Atualmente ela pode ser complementar de valor, **quantidade ou ICMS**. Seu uso deve observar os seguintes critérios estabelecidos no manual de integração v.4.0:

• deve-se referenciar a chave da nota original a qual nota se refere o complemento;

• Pode ser complementado tanto uma NF-e quanto uma Nota modelo 1/1ª;

• Os dados do destinatário/emissor devem ser idênticos ao da nota referenciada;

• CFOP da operação pode ser alterado;

• Transportadora: deve-se informar a modalidade de frete por conta do emitente, sem necessidade de inserir as demais informações sobre transporte;

• Campo Informações Complementares: pode ser informado os dados da nota como numero ou chave das notas referenciadas ou qualquer outra informação de interesse;

• Deve possuir o(s) mesmo(s) produto(s) das notas referenciadas. Caso exista algum produto que foi incluido e não constou na NF-e normal, deve emitir uma nova NF-e normal constando este produto;

• É utilizada sempre para complementar, ou seja, para acrescentar e nunca para debitar/subtrair. Para tais fatos deve-se utilizar carta de correção e/ou nota fiscal de devolução de acordo com cada caso.

**CFOP 5.111 - Saída de Nota complementar: o que é e quando utilizar?**

Inicialmente, é importante recordar que o CFOP(Código Fiscal de Operações e Prestações) – CFOP é composto por 4 dígitos, sendo que o primeiro deles define a natureza da operação.

O dígito 5 no início do código indica que a operação ou prestação contempla movimentações dentro do mesmo estado, ou seja, elas são intermunicipais e podem ser de movimentação, venda, saída, demonstração, transferência de mercadoria e também de remessa para conserto.

Os outros dígitos especificam a operação. No caso, o CFOP 5.111 é utilizado para indicar as vendas efetivas de produtos industrializados no estabelecimento remetidos anteriormente a título de consignação industrial. Esse código pode ser utilizado na operação fiscal quando alguma informação importante deixou de ser destacada na Nota Fiscal eletrônica (NF-e), sendo necessário **complementá-la** em algum campo.

Em resumo, o CFOP 5.111 pode ser utilizado nesses casos:

* **Somente para casos de operações intermunicipais;**
* Em NF-e de produtos produzidos pela própria indústria;
* Para complementar uma informação na NF-e, como reajuste de preço, de valor menor informado, entre outros.

**OBS: Esta informação foi obtida de uma fonte de terceiros e não possui teor fiscal ou legal, visando somente direcionar o cliente à uma solução concreta, que deve ser obtida junto ao contador da Empresa, até mesmo devido à variações legislativas de cada Unidade Federativa. Não nos responsabilizamos pelo seu conteúdo e pelas ações tomadas com base nele.**

No Sigeflex, basta realizar uma emissão de nota normal, seguindo as orientações acima, e nos campos de informações DADOS DA NOTA se atentar aos dados:

* NATUREZA DA OPERAÇÃO Informar que é uma Nota **complementar**;
* FINALIDADE informar também que é um complemento.
