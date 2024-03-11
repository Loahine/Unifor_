# Unifor 
**Nome**: Luiza
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
### Pseudocódigo
```
1 ALGORÍTMO verificar_par_ou_ímpar
2 DECLARE N, R NUMÉRICO
3 ESCREVA “Digite o número”
4 LEIA N
5 SE N>=0 ENTÃO
6 	R⇐N%2
7 	SE R==0 ENTÃO 
8 		ESCREVA “NUMERO É PAR”
9 	SENÃO
10		ESCREVA ”NUMERO É IMPAR”
11 	SENÃO
12 		ESCREVA “O NÚMERO NÃO É POSITIVO”0
13 FIM_ALGORITMO
```
