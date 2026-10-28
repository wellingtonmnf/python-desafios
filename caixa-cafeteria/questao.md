## Questão 01 — O caixa de uma cafeteria

***[ Nível: básico a intermediário ]***

Uma cafeteria está desenvolvendo um sistema simples para processar pedidos. Os funcionários registram os produtos e suas quantidades, mas o sistema ainda não verifica se os produtos existem, se estão disponíveis ou se as quantidades fazem sentido.

Você recebeu os seguintes dados:

```
cardapio = {
    "cafe": (5, True),
    "sanduiche": (12, True),
    "suco": (7, False),
    "bolo": (8, True)
}

pedidos = [
    ("cafe", 2),
    ("bolo", 1),
    ("suco", 2),
    ("cafe", 1),
    ("agua", 1),
    ("sanduiche", 1),
    ("bolo", -2),
    ("cafe", "dois")
]
```

No dicionário `cardapio`, cada produto possui uma tupla contendo seu preço e sua disponibilidade (`True` ou `False`).

---

### Seu desafio: 

Desenvolver um processamento que produza um recibo com os produtos válidos, suas quantidades acumuladas, os subtotais e o valor total da compra. O sistema também deverá produzir um relatório separado com os pedidos rejeitados e os motivos de cada rejeição.

Você precisará decidir como tratar produtos inexistentes, indisponibilidade, quantidades negativas e quantidades que não sejam números válidos. Um pedido incorreto não deverá impedir o processamento dos demais.

---

### Requisitos técnicos:

Utilize pelo menos uma função própria, tratamento de exceções com `try/except`, um dicionário para consolidar os produtos e compreensão de listas em alguma etapa significativa do processamento.

---

### Questão para reflexão: 

*Por que o sistema não deve simplesmente ignorar os pedidos inválidos sem registrar os motivos?*
