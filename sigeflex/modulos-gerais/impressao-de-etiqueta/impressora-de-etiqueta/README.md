---
description: Passo a Passo para imprimir código de barra usando a impressora de Etiqueta
---

# 🖨 Imprimir em Impressora de Etiqueta

### Configuração da Etiqueta no AcbrMonitor

Siga os passos abaixo para configurar a impressora para que seja possível imprimir através do sistema

* Download e instalação do drive da impressoa, [clique aqui](https://www.bztech.com.br/arquivos/driver-elgin-l42.zip)
* Após a instalação, a mesma deve aparecer na lista de impressoras, clique sobre ela com o botão direito, propriedades e compartilhe a impressora na rede, como mostra a imagem abaixo

![Imagem compartilhando a impressora após instalação](<../../../../.gitbook/assets/image (158).png>)

* Abra o AcbrMonitor, clique na aba Etiqueta, e deixe os seguintes valores nos campos:
  * Modelo: **etqPpla**
  * Porta: **\\\localhost\ELGIN L42Pro**
* Clique em salvar, pronto, o AcbrMonitor já está configurado para imprimir na impressora

![](<../../../../.gitbook/assets/image (164).png>)

### **Configuração da Etiqueta no Sistema**

* Clique no menu **Cadastros, Etiqueta,** para que possa configurar a etiqueta que deseja e seu formado no sistema, como mostra a imagem abaixo, já com alguns modelos padrão.



![Tela que mostra os modelos disponíveis](<../../../../.gitbook/assets/image (172).png>)

#### - Cadastrar uma nova Etiqueta

A tela abaixo, digite os dados da etiqueta como mostra o modelo abaixo, alterando apenas para o seu caso, depois clique em **template** para definir as configurações de impressão de Etiqueta

![Tela para cadastrar uma nova etiqueta](<../../../../.gitbook/assets/image (165).png>)

Ao abrir a tela para definir as configurações de etiqueta, o sistema já traz um modelo padrão de impressão de acordo com o número de colunas que defindiu no passo anterior

![Tela para definir as configurações de impressão da Etiqueta](<../../../../.gitbook/assets/image (174).png>)

O modelo de etiqueta é configurado seguindo o seguinte modelo abaixo, **É PRECISO CONFIGURAR CADA CAMPO COMO DESEJA,** a config abaixo já é funcional**,** mas para ajustar de acordo com preferência, é preciso alterar o modelo e ir testando, todas as medidas usam a unidade **MILÍMETRO (mm),** então essas coordenadas nas configurações é em **milímetro**, dessa forma, pode-se configurar **milimetricamente** onde cada campo será impresso na etiqueta.

#### Explicações dos campos

* **vertical** (Altura): onde vai começar a imprimir a etiqueta no posição vertical, de baixo para cima
* **horizontal** (Largura): onde vai começar a imprimir a etiqueta na posição horizontal, da esquerda para a direita
* **Orientação**: normal, 270,180 e 90 graus

Modelo abaixo de uma configuração, SE FOR COPIAR E COLAR O MODELO ABAIXO, RETIRA OS COMENTÁRIOS, POIS COM COMENTÁRIO O TEMPLATE NÃO É VÁLIDO

```javascript
   "margemEsquerda":0,
   "limparMemoria":false,
   "colunas":1,
   "configEtiqueta":{
      "campoTexto":{  //coloca quantos campos textos vao ser impressos       
         "Nome":{
            "orientacao":"normal", // normal, 270,180 e 90 graus 
            "numeroFonte":1, // tamanho da letra
            "multiplicadorHorizontal":2, //influencia no tamanho da letra
            "multiplicadorVertical":2, //influencia no tamanho da letra na horizontal   
            "vertical":2, //posicao em mm na vertical(altura) que começa a imprimir
            "horizontal":10,//posicao em mm na horizontal(largura) que começa a imprimir
            "laguraFonte":1,
            "alturaFonte":1,
            "maxLength":30, //quantidade maxima de caracteres pro campo
            "quebraLinha":true//se tem quebra de linha no caso de passar a quantidade maxima
         },
         "PrecoAvista":{
            "orientacao":"normal",
            "numeroFonte":3,
            "multiplicadorHorizontal":2,
            "multiplicadorVertical":2,
            "vertical":10,
            "horizontal":26,
            "larguraFonte":1,
            "alturaFonte":1,
            "maxLength":0,
            "quebraLinha":false,
            "prefixo": "VAREJO "
         },
         "PrecoAtacado":{
            "orientacao":"normal",
            "numeroFonte":3,
            "multiplicadorHorizontal":2,
            "multiplicadorVertical":2,
            "vertical":15,
            "horizontal":26,
            "larguraFonte":1,
            "alturaFonte":1,
            "maxLength":0,
            "quebraLinha":false,
            "prefixo": "ATACADO "
         }

      },
      "campoBarra":{
         "CodigoBarra":{
            "tipoBarraCodigo":"EAN13", //tipo de codigo de barra
            "orientacao":"normal", 
            "larguraBarraLarga":3,
            "larguraBarraFina":3,
            "vertical":20, //posicao vertical que começa a imprimir
            "horizontal":20,//posicao horizontal que começa a imprimir
            "alturaCodBarras":7,
            "exibirCodigo":true
         }
      },
      "campoImagens":null
   },
   "dados":[ //dados de teste para impressão
      {
         "codigo":"123",
         "CodigoBarra":"7892948050680",
         "Nome":"COMPUTADOR DELL",
         "PrecoAvista":"R$ 36,87",         
         "PrecoAtacado":"R$ 75,98"      
      }   
   ]
}
```



Após ir alterando o modelo, clique em salvar e em seguida imprimir teste, na mesma hora vai analisando como ta saindo a etiqueta até chegar ao padrão que deseja, depois disso, basta salvar as informações da etiqueta que estará pronto para imprimir no sistema com esse novo modelo.

### Imprimindo Etiqueta no Sistema

Para imprimir as etiquetas, vá no cadastro de produto e clique no botão i**mprimir etiquetas**, será exibida as etiquetas disponíveis para impressão, basta escolher o modelo da sua etiqueta e clicar em imprimir



![tela de impressão de etiqueta para os preços de produtos](<../../../../.gitbook/assets/image (168) (1).png>)

É preciso ir imprimindo a etiqueta e ver se está de acordo com o que deseja, caso queira mudar, volta pra[ configuração de etiqueta](./#configuracao-da-etiqueta-no-sistema), altera os parâmetros e tenta novamente.

### Instalação do [`Linker`](https://github.com/linksoft-dev/downloads/releases/download/latest/LinkerInstalacao.exe) para impressão em impressora de etiquetas

Caso clique em imprimir e ainda não tenha o Linker instalado no seu computador, a mensagem abaixo aparecerá, clique no link para baixar o **Linker** e em seguida, instale-o, após esse procedimento, o Linker estará instalado no seu computador e poderá imprimir as etiquetas depois que fizer a [configuração da impressora no AcbrMonitor](./#configuracao-da-etiqueta-no-acbrmonitor)

![Necessário o Linker para impressão de etiquetas em impressora de etiquetas](<../../../../.gitbook/assets/image (171).png>)

