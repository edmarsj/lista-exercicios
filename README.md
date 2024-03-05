# Laço `para`
O laço `para` é usado principalmente em duas situações
- Quando sabemos exatamente quantas vezes vamos executar um bloco de instruções. 
```
//Ex. 1 imprimir todo os números de 0 à 10
para (inteiro i = 0; i <= 10; i++)  
{  
    excreva(i)
}  

//Ex. 2 imprimir "Já chegamos?" 10 mil vezes
para (inteiro i = 0; i <= 10000; i++)  
{  
    excreva("Já chegamos?")
}  
```
- Quando queremos ter controle sobre valores que estamos usando ao executar um bloco de código
```
//Ex. 3 imprimir todos os números entre 50 e 100, porém de 10 em 10
// ex. 10 20 30 40...
inteiro inicial = 50
inteiro final = 100
inteiro incremento = 10
para (inteiro i = inicial; i <= final; i = i + incremento)  
{  
    excreva(i)
}  
```

### Exercícios

#### 1. Faça um programa que imprima todos os números pares entre 1 e 10. Dica: Use o operador aritimético módulo (%).

#### 2. Faça um programa que leia duas entradas do usuário: Valor inicial e valor final. Imprima todo os números multiplos de 5 entre esses valores.

#### 3. Faça um programa que leia um numero `n` do usuário. Exiba a tabuada para aquele número. (ex. n x 1 = X, n x 2 = X, etc..) 

#### 4. Hoje em dia os processadores possúem circuitos específicos para realizar operações matemáticas, entre elas a multiplicação. Mas nem sempre foi assim, antigamente, devido a limitações de hardware, a multiplicação era feita usando laços! Vamos fazer igual aos computadores de antigamente faziam: Escreva um programa que leia um numeroA e um numeroB e exiba o resultado de numeroA x numeroB. Você não pode usar o operador aritimético *



# Laços `Enquanto` e `Faça-Enquanto`
Estes laços são usados principalmente quando você ter repetir um bloco de instruções indefinitivamente enquanto uma condição específica for verdadeira.

```
//Ex. 4 exibe a mensagem "Já chegamos? s/n" enquanto o usuário digitar n

cadeia entrada
logico aindaNaoChegamos= verdadeiro
enquanto(aindaNaoChegamos)
{
    escreva("Já chegamos? (s/n):   ")
    leia(entrada)
    se (entrada == "s")
    {
    aindaNaoChegamos = falso
    }
}
escreva("Ufa!")

```

A principal diferença entre os laços Enquanto e Faça-Enquanto é a ordem na qual a condição é conferida. No laço Enquanto, a condição é conferida primeiro para depois executar o bloco de código. Em Faça-Enquanto, primeiro o código é executado para depois se verificar a condição. 


```
//Ex. 5 Diferenças entre enquanto e faça-enquanto:

logico condicao = falso

// condicao e falso então não deve executar o bloco de instruções
enquanto(condicao)
{
    escreva("Eu não devo imprimir isso!")
}

// condicao e falso vai executar o bloco de instruções apenas uma vez
faca
{
    escreva("Eu vou imprimir isso uma vez!")
} enquanto(condicao) 

```


### Exercícios
#### 5. Escreva um programa que leia um texto do usuário. Se o usuário escrever "ping", o programa deve imprimir "pong". Se o usuário escrever "pong" o programa deverá escrever "ping". Se o usuário digitar qualquer coisa diferente o programa deve ser encerrado.  

#### 6. Escreva um programa que leia um numero do usuário, salve em uma variável acumuladora e mostre o total acumulado. O programa deve parar se o usuário digitar um número negativo. 

#### 7. Faça um programa que escolha secretamente um número aleatório entre 1 e 10 e peça para o usuário tentar adivinhar o número sorteado. Se o usuário acertar encerre o programa. Se o usuário errar repita a operação sorteando um novo número e pedindo para o usuário adivinhar. Use a biblioteca Util e a função sorteia dentro da mesma. Aqui vai um exemplo de seu uso
```
programa {
  inclua biblioteca Util

  funcao inicio() {

    escreva(Util.sorteia(10,20))    

  }
}
```

## Desafio: Pedra, papel e tesoura

Faça um programa para jogar pedra, papel e tesoura com o usuário. 
- O programa deve pedir para o usuário entrar um número de 1 à 3, sendo:
  - 1: Pedra
  - 2: Papel
  - 3: Tesoura
- O programa deve escolher um número aleatório entre 1 e 3. 
- O programa deve informar ao usuário o resultado da disputa seguindo as regras clássicas do jogo (pedra amassa tesoura, tesoura corta papel, papel enrola pedra, empate)
