# Unifor 
**Nome**: Luiza
**Nome de disciplina**: Raciocínio lógico algorítmico

## Q1
### Fluxograma
```mermaid
flowchart TD
A([Início])-->B{{"Escreva quatro número"}}
B-->C[\A,B,C,D\]
C-->D[M=A+B+C+D]
D-->E[M=M/4]
E-->F([Fim])
```

### Pseudocódigo 
```
	ALGORITMO media_inteiros
	DECLARE A,B,C,D,M: Numéricos
	INICIO
	ESCREVA "Digite quatro números:"
	LEIA A,B,C,D
	M<--A+B+C+D
	M<--M/4
	FIM
```

### Teste
|numero|soma |media|
|--|--|--|
|2,4,6,8|20|5|
|1,1,1,1|4|1|
|10,20,30,40|100|25|
|5,5,5,5|20|5|

## Q2
### Fluxograma
```mermaid
flowchart TD
A([Início])-->B{{Digite a temperatura}}
B-->C[\C\]
C-->D["F=(9/5)C+32"]
D-->E{{F}}
E-->F([Fim])
```

### Pseudocódigo
```
	ALGORÍTMO temperatura
	DECLARE C,F: NUMÉRICO
	ESCREVA “Digite a temperatura”
	LEIA C
	F=(9/5)C+32
	ESCREVA F
	FIM_ALGORITMO
```
### Teste
°C | °F
-|-
38|100.4
25|77
28|82.4

## Q3
### Fluxograma
```mermaid
flowchart TD
A([Início])-->B{{"Digite dois números:"}}
B-->C[\a,b\]
C-->D{{"Digite a operação (+, -, *, /):"}}
D-->E[\o\]
E-->F{o==+}
F--não-->G{0==-}
G--não-->H{o==*}
H--não-->I{o==/}
I-->J{b!=0}
J--não-->K{{"divisão por zero"}}
J--sim-->L[c <-- a / b]
F--sim-->M[c <-- a + b]
G--sim-->N[c <-- a - b]
H--sim-->O[c <-- a * b]
L-->P{{c}}
M-->P{{c}}
N-->P{{c}}
O-->P{{c}}
P-->Q([Fim])
K-->Q([Fim])
```
### Pseudocodigo
```
ALGORITMO operação
DECLARE a, b, c: NUMÉRICO 
DECLARE o STRING 
INICIO 
ESCREVA "Digite dois números:" 
LEIA a, b 
ESCREVA "Digite a operação (+, -, *, /):" 
LEIA o 
	ESCOLHA 
		CASO (o==+)
			c <-- a + b 
		CASO (0==-)
			c <-- a - b 
		CASO (o==*)
			c <-- a * b 
		CASO (o==/)
			SE (b != 0) ENTÃO 
				c <-- a / b 
			SENÃO 
				ESCREVA "divisão por zero" 
			FIM_SE 
		SENÃO 
			ESCREVA "Operação inválida" 
	FIM ESCOLHA 
	ESCREVA c 
FIM
```
### Teste
| N1 | N2 | op | op == + | op == - | op == * | op == / | N2 != 0 | Saída                           |
|----|----|----|---------|---------|---------|---------|:-------:|---------------------------------|
| 10 | 1  | +  | True    | False   | False   | False   |    -    | 11                              |
| 11 | 2  | -  | False   | True    | False   | False   |    -    | 9                               |
| 12 | 3  | *  | False   | False   | True    | False   |    -    | 36                              |
| 13 | 4  | /  | False   | False   | False   | True    |   True  | 3,25                            |
| 14 | 0  | /  | False   | False   | False   | True    |  False  | Digite um número maior que zero |

## Q4
### Fluxograma
```mermaid
flowchart TD
A([Início])-->B{{"Digite a idade: "}}
B-->C[\i\]
C-->D{i>=5}
D--sim-->E{5<=i e i<=7}
E--não-->F{8<=i e i<=10}
F--não-->G{11<=i e i<=13}
G--não-->H{14<=i e i<=17}
H--não-->I{{Adulto}}
H--sim-->V{{"Juvenil B"}}
G-->W{{"Juvenil A"}}
W-->Z
F--sim-->X{{"Infantil B"}}
X-->Z
E--sim-->Y{{"Infantil A"}}
Y-->Z([Fim])
D--não-->Z([Fim])
I-->Z([Fim])
V-->Z([Fim])
```

### Pseudocódigo 
```
ALGORITMO categoria 
	DECLARE i: NUMERICO
	INICIO
	ESCREVA "Digite a idade: "
	LEIA i
		SE (i>=5)
			ESCOLHA 
				CASO (5<=i e i<=7)
					ESCREVA "Infantil A"
				CASO (8<=i e i<=10)
					ESCREVA "Infantil B"
				CASO (11<=i e i<=13)
					ESCREVA "Juvenil A"
				CASO (14<=i e i<=17)
					ESCREVA "Juvenil B"
				SENÃO
					ESCREVA "Adulto"
			FIM_ESCOLHA
		SENÃO
		FIM_SE
FIM
```
idade|i>=5|5<=i e i<=7|8<=i e i<=10|11<=i e i<=13|14<=i e i<=17|saida
-|-|-|-|-|-|-
16|sim|não|não|não|sim|Juvenil B
19|sim|não|não|não|não|Adulto
4|não|-|-|-|-|-
