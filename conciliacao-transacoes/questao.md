## Questão 02 — Conciliação de transações financeiras

***[ Nível: intermediário ]***

Uma plataforma de pagamentos exporta suas transações em um formato textual simplificado. Cada registro contém o identificador da transação, sua situação e seu valor, separados por ponto e vírgula.

O setor financeiro precisa saber quanto realmente foi vendido, mas os registros podem conter cancelamentos, estornos, valores inválidos e transações duplicadas.

```
registros = [
    "P001;aprovada;120",
    "P002;cancelada;80",
    "P003;aprovada;50",
    "P004;aprovada;75",
    "P005;aprovada;abc",
    "P006;estornada;25",
    "P007;aprovada;100",
    "P003;aprovada;60",
    "P008;aprovada;120"
]
```

---

### Seu desafio: 

Produzir um relatório de conciliação capaz de identificar registros válidos e inválidos, eliminar duplicidades e calcular o valor efetivamente aprovado.

Considere que cada identificador deve ser único e que, em caso de duplicidade, somente a primeira ocorrência válida deve ser considerada. Transações canceladas ou estornadas não entram no total de vendas aprovadas.

O relatório deverá apresentar o total arrecadado, a quantidade de transações aprovadas, o valor médio dessas transações e as três maiores vendas. Também deverá informar quantos registros foram descartados por inconsistência ou duplicidade.

---

### Requisitos técnicos:

- Utilize `map()` em alguma etapa de transformação dos dados;
- Utilize `filter()` para selecionar as transações aprovadas;
- Utilize `reduce()` para calcular o total arrecadado;
- Utilize `sorted()` com lambda para identificar as maiores vendas;
- Utilize um conjunto (`set`) para auxiliar na identificação de duplicidades;

Você pode criar funções auxiliares e usar laços convencionais quando necessário. Não é obrigatório resolver tudo com funções avançadas.

---

### Questão para reflexão: 

*O que aconteceria se você calculasse o total das vendas antes de eliminar as duplicidades? E por que converter o valor textual para número exige atenção?*
