# Unifor 
**Nome**: Nome de estudante
**Nome de disciplina**: Raciocínio lógico algorítmico

## Exercício 3
### Fluxograma
```mermaid
flowchart TD
A([Início])-->B{{Digite um número}}
B-->C[\N\]
C-->D{N>=0}
D--NÃO-->E[O número não é positivo]
E-->Z([Fim])
D--SIM-->F[R=N%2]
F-->G{R==0}
G--NÃO-->H[O número é ímpar]
G--SIM-->I[O número é par]
H-->Z([Fim])
I-->Z([Fim])
```
