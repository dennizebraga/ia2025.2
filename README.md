## Algoritmo Genético para o 8-Puzzle (com Fine Tuning)

Este projeto implementa um Algoritmo Genético (GA) para resolver o jogo 8-Puzzle.
Além das operações tradicionais do GA (seleção, crossover e mutação), foi adicionada uma etapa de fine tuning, feita com Busca Local (Hill-Climbing) aplicada ao melhor indivíduo de cada geração.
O objetivo desse ajuste é melhorar o desempenho do GA, acelerando a redução do fitness e ajudando o algoritmo a escapar de soluções ruins.

## Contexto

O código original fornecido pelo professor continha apenas o Algoritmo Genético básico.
Neste trabalho, foi adicionada uma etapa extra de otimização, onde o melhor indivíduo da população passa por uma busca local para tentar diminuir o fitness.
Essa modificação permite que o algoritmo avance para estados melhores mais rapidamente, principalmente em gerações onde o GA sozinho teria dificuldade.

## Como Executar
```python
python com_fine_tuning.py
```
## Em execução, o algoritmo exibirá, a cada geração:

O número da geração, o fitness do melhor indivíduo, o estado atual do puzzle

Quando o fine tuning encontrar um estado melhor, aparecerá uma mensagem indicando a melhora.

## Output Sem Fine Tuning
```python
O GA melhora o fitness aos poucos, mas geralmente não chega a 0:
Generation 0 | Best fitness: 6 | State: [...]
Generation 1 | Best fitness: 6 | State: [...]
...
Generation 15 | Best fitness: 1 | State: [...]
```

## Output Com Fine Tuning
A Busca Local reduz o fitness rapidamente e permite que o GA atinja o objetivo:
```python
Busca Local melhorou o fitness de 8 para 4!
Generation 0 | Best fitness: 4 | State: [...]

Busca Local melhorou o fitness de 3 para 0!
Generation 1 | Best fitness: 0 | State: [...]
Goal reached!
```

