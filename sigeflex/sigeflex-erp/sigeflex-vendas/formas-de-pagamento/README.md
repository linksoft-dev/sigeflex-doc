---
description: Cadastrando uma forma de pagamento
---

# Formas de pagamento

No cadastro de formas de pagamentos é possivel criar os registros para gerir melhor os recebimentos, seja ele Cartão, Boleto ou Dinheiro. Tambem onde é possivel realizar as configurações para os recebimentos online.

![](<../../../../.gitbook/assets/image (56).png>)

Para recebimentos online é necessario ter integracão com os gateway de pagamentos, no momento o sistema tem disponível integração com  PagHiper, e Cielo.

![](<../../../../.gitbook/assets/image (57).png>)

O cadastro dispodem dos campos:\
\- Nome (nome da forma de pagamento).\
\- Tipo de pagamento.\
\- Codigo.\
Ao selecionar as opções a(s) marcada(s) irá ser disponibilizado as formas de pagamentos:\
\
\- Disponível Checkout para exibir na tela de recebimento online.\
\- Disponível Venda para exibir na tela de pedido ou PDV.

Na Aba Condições de pagamento, será necessario configurar a quantidade de parcelas caso seja uma opção disponivel o parcelamento.



Logo após, a aba Intermediadores de Pagamentos, terá disponivel os campos para inserir os dados de configuração da integração do sistema, seja para recebimentos em boletos ou cartao. O preenchimento correto dessas informações é importante para o recebimento de forma online. Todos os dados solicitados será encontrado com seu Intermediador, seja ele Cielo ou PagHiper.

Para utilizar a função e receber os pagamentos via boleto ou cartão, é necessario ter cadastro com os gateways de pagamento/intermediador de pagamento suportado pelo sistema,  atualmente temos suporte para os seguintes gateways:

* **Boleto**
  * Cielo
  * [Paghiper](pagamento-online-com-boleto-via-paghiper.md)
* **Cartão Crédito**
  * [Cielo](pagamento-online-com-cartao-via-cielo.md)
