## Questão 03 — Distribuição inteligente de tarefas

***[ Nível: intermediário — desafio de lógica ]***

Uma equipe de tecnologia precisa distribuir tarefas entre profissionais que possuem habilidades e disponibilidades diferentes.

O gestor quer automatizar essa distribuição para evitar sobrecarga e garantir que cada tarefa seja atribuída somente a alguém que possua todas as habilidades necessárias.

```
profissionais = {
    "Ana": {
        "habilidades": {"python", "sql"},
        "horas": 6
    },
    "Bruno": {
        "habilidades": {"python", "excel"},
        "horas": 5
    },
    "Carla": {
        "habilidades": {"sql", "excel"},
        "horas": 4
    }
}

tarefas = [
    ("Conferir indicadores", {"sql"}, 3, 1),
    ("Automatizar planilha", {"python", "excel"}, 4, 2),
    ("Integrar dados", {"python", "sql"}, 3, 3),
    ("Criar apresentacao", {"excel"}, 3, 4),
    ("Revisar automacao", {"python"}, 2, 5),
    ("Tarefa inconsistente", {"excel"}, -1, 6)
]
```

Cada tarefa é representada por uma tupla contendo nome, habilidades exigidas, horas estimadas e prioridade. Quanto menor o número da prioridade, mais urgente é a tarefa.

---

### Seu desafio: 

Construir um algoritmo que distribua as tarefas respeitando as regras de negócio abaixo.

1. As tarefas devem ser analisadas em ordem de prioridade;
2. Um profissional só pode receber uma tarefa se possuir todas as habilidades exigidas e horas suficientes;
3. Quando houver mais de um profissional elegível, escolha aquele com mais horas disponíveis. Se houver empate, escolha pelo nome em ordem alfabética;
4. As horas atribuídas devem ser descontadas da disponibilidade do profissional;
5. Tarefas com duração inválida devem ser rejeitadas. Tarefas que não puderem ser atribuídas devem constar em uma relação de pendências;

Ao final, apresente a distribuição das tarefas, as horas restantes de cada profissional e os motivos das tarefas não atribuídas ou rejeitadas.

---

### Requisitos técnicos: 

Utilize operações com conjuntos para comparar habilidades, `sorted()` com `lambda` para ordenar as tarefas e compreensão de listas para identificar os profissionais elegíveis. Organize sua lógica em funções.

---

### Questão para reflexão: 

*Escolher sempre o profissional com maior disponibilidade produz necessariamente a melhor distribuição possível de todas as tarefas? Pense em um cenário no qual uma escolha inicial impeça uma distribuição melhor posteriormente.*
