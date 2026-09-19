# Aplicação Prática — Regressão Linear Simples

## 1. Sobre o projeto

Este projeto apresenta uma aplicação prática de **Regressão Linear Simples** utilizando uma base de dados real de vendas de informática.

A aplicação foi desenvolvida para atender à **Parte IV — Aplicação Prática** da atividade de Machine Learning, utilizando a situação proposta:

> Prever o valor da venda utilizando apenas o número de produtos vendidos.

A implementação foi realizada em **Python**, utilizando o **Jupyter Notebook** e a biblioteca **Scikit-learn**.

---

## 2. Situação escolhida

Foi escolhida a **Situação A**:

**Prever o valor da venda utilizando apenas a quantidade de produtos vendidos.**

O objetivo é verificar se a quantidade de produtos pode ser utilizada para gerar uma estimativa do valor total de uma venda.

---

## 3. Base de dados

Foi utilizada a base real:

`vendas_informatica_100_mil.csv`

A base contém informações de vendas de produtos de informática, incluindo colunas como:

- `ID_Pedido` — identificação do pedido;
- `Data` — data da venda;
- `Loja` — loja relacionada à venda;
- `Produto` — produto vendido;
- `Preco_Unitario` — preço unitário do produto;
- `Qtd` — quantidade de produtos vendidos;
- `Cliente` — identificação do cliente;
- `Data_Base` — data de referência da base.

Para realizar a aplicação, foi criada uma nova variável chamada `Valor_Venda`, calculada por:

`Valor_Venda = Preco_Unitario × Qtd`

Essa variável representa o valor total da venda e foi utilizada como variável-alvo.

**Observação:** o `Preco_Unitario` foi utilizado somente para calcular o valor da venda. Ele não foi utilizado como variável de entrada do modelo, pois a situação escolhida determina que a previsão seja realizada utilizando apenas a quantidade de produtos.

---

## 4. Entradas e variável-alvo

### Variável de entrada

**`Qtd` — quantidade de produtos vendidos**

É a única variável utilizada pelo modelo para realizar a previsão.

### Variável-alvo

**`Valor_Venda` — valor total da venda**

É o valor que o modelo busca prever.

---

## 5. Modelo escolhido

Foi utilizada a **Regressão Linear Simples**.

O modelo foi escolhido porque a situação possui:

- uma única variável de entrada (`Qtd`);
- uma variável-alvo numérica (`Valor_Venda`).

A Regressão Linear Simples busca representar a relação entre uma variável de entrada e uma variável numérica que se deseja prever por meio de uma equação linear.

A equação obtida com os dados utilizados foi aproximadamente:

`Valor_Venda = 19,70 + 1.985,31 × Qtd`

---

## 6. Preparação mínima dos dados

A preparação dos dados foi realizada de forma simples:

1. Importação da base CSV;
2. Criação da coluna `Valor_Venda`;
3. Definição de `Qtd` como variável de entrada;
4. Definição de `Valor_Venda` como variável-alvo.

O objetivo foi manter o tratamento dos dados apenas no necessário para realizar a demonstração solicitada.

---

## 7. Implementação

As principais bibliotecas utilizadas foram:

- **Pandas** — para carregar e manipular os dados;
- **Scikit-learn** — para aplicar a Regressão Linear;
- **Matplotlib** — para representar graficamente os dados e a reta de regressão.

---
## 8. Previsão realizada

Foi realizada uma previsão considerando uma venda com 5 produtos.

O modelo estimou:

R$ 9.946,23

Esse resultado representa o valor estimado pelo modelo a partir da quantidade de produtos informada.

---

## 9. Interpretação do resultado

A previsão mostra que, utilizando somente a quantidade de produtos vendidos, o modelo consegue gerar uma estimativa para o valor de uma venda.

A equação encontrada indica uma relação positiva entre a quantidade de produtos e o valor previsto da venda.

De acordo com o modelo, cada unidade adicional de produto está associada a um aumento estimado de aproximadamente R$ 1.985,31 no valor previsto.

---

## 10. Interpretação em linguagem de negócio

No contexto de um e-commerce, o modelo pode ser utilizado para obter uma estimativa inicial do valor de uma venda a partir da quantidade de produtos.

Por exemplo, para uma venda contendo 5 produtos, a estimativa obtida foi de aproximadamente R$ 9.946,23.

Entretanto, a previsão deve ser interpretada com cuidado, pois o modelo utiliza somente a quantidade de produtos e não considera diretamente as diferenças entre os preços dos produtos vendidos.

---

## 11. Limitação

Uma limitação da aplicação é que o valor total de uma venda também depende do preço dos produtos. Como a situação escolhida determina que somente a quantidade seja utilizada como entrada, o modelo não utiliza Preco_Unitario como variável explicativa.

Assim, o resultado deve ser entendido como uma estimativa baseada exclusivamente na quantidade de produtos, e não como uma representação de todos os fatores que determinam o valor de uma venda.
