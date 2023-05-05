# include  <stdio.h>
// Soma todos os valores entrados pelo usuário na faixa
// de 1 a 19, até que a soma seja maior ou igual a 100.
int main () {
    int n, soma = 0 ;
    do {
            do {
                    printf ( " Digite um numero [1..19] : \n " );
                    scanf ( " %d " , &n);
            } while (n< 1 || n> 19 );
              if (n == 0) break;
            soma += n;
    } while (soma < 100 );
    printf ( " Valor final da soma: %d  \n " , soma);
    return  0 ;
}

# include  < stdio.h >

int  main () {
    int a= 2 , b= 3 ;
    int c = a++ + b++;
    printf ( " %d  %d  %d  \n " , a, b, c);
    c = ++a + ++b;
    printf ( " %d  %d  %d  \n " , a, b, c);
    return  0 ;
}

# include  < stdio.h >

int  main () {
    int num;
    int soma = 0 ;
    fazer {
        printf ( " Digite um numero: \n " );
        scanf ( " %d " , &num);
        soma+= num;
    } while (soma < 100 );
    printf ( " Resultado: %d  \n " ,soma);
    return  0 ;
}

# include  < stdio.h >

int  main () {
    int opcao;
    printf ( " Menu do Biro Lanchonete \n " );
    printf ( " 1. Coxinha \n " );
    printf ( " 2. Esfiha \n " );
    printf ( " 3. Pastel de Carne \n " );
    printf ( " 4. Pastel de Queijo \n " );
    printf ( " Escolha sua opção:   \n " );
    scanf ( " %d " , &opcao);
    switch (opção) {
        caso  1 :
            printf ( " Coxinha, R$ 8,00 \n " );
            quebrar ;
        caso  2 :
            printf ( " Esfiha, R$ 7,00 \n " );
            quebrar ;
        caso  3 :
            printf ( " Pastel de Carne, R$ 8,00 \n " );
            quebrar ;
        caso  4 :
            printf ( " Pastel de Queijo, R$ 8,00 \n " );
            quebrar ;
        padrão :
            printf ( " Escolha errada. Verifique. \n " );
    }
    return  0 ;
}

# include  < stdio.h >

int  main () {
    char letra;
    printf ( " Digite uma unica letra: \n " );
    fflush (stdin);
    letra = getchar ();
    switch (letra) {
        caso  ' a ' :
        caso  ' A ' :
        caso  ' e ' :
        caso  ' E ' :
        caso  ' eu ' :
        caso  ' eu ' :
        caso  ' o ' :
        caso  ' O ' :
        caso  ' u ' :
        caso  ' U ' :
            printf ( " Trata-se de vogal \n " );
            break ;
        default :
            printf ( " Nao eh vogal \n " );
    }
    return  0 ;
}

# include  < stdio.h >

int  main () {
    char estadoCivil;
    printf ( " Cadastro de Pessoas \n " );
    printf ( " Viuvo(a) - [v] \n " );
    printf ( " Divorciado(a) - [d] \n " );
    printf ( " Casado(a) - [c] \n " );
    printf ( " Solteiro(a) - [s] \n " );
    fflush (stdin); // limpa o buffer do teclado
    estadoCivil = getchar ();
    switch (estadoCivil) {
        case  ' v ' :
        case  ' V ' :
            printf ( " Estado civil: viuvo(a) \n " );
            break ;
        case  ' d ' :
        case  ' D ' :
            printf ( " Estado civil: divorciado \n " );
            break ;
        case  ' c ' :
        case  ' C ' :
            printf ( " Estado civil: casado(a) \n " );
            break ;
        case  ' s ' :
        case  ' S ' :
            printf ( " Estado civil: solteiro(a) \n " );
            break ;
        default :
            printf ( " opção inválida \n " );
    }
    return  0 ;
}

# include  < stdio.h >

int  main () {
/* Ele não vai imprimir o 3 e o 7*/
    for ( int i = 1 ; i <= 10 ; i++) {
        se (i== 3 || i== 7 ) continue ;
        printf ( " %d  \n " ,i);
    }
    printf ( " Acabou \n " );
    return  0 ;
}

# include  < stdio.h >
# include  < stdlib.h >
# inclui  < hora.h >

int  main () {
    srand ( time ( NULL ));      /* pega um numero aleatório*/
    int magico = rand ()% 100 ;  /* limita a quantidade*/
    int palpite;
    int cont = 0 ;
    while ( 1 ){
        cont++;
        printf ( " Digite seu palpite de [0..99] - Tentativa [ %d /7] \n " , cont);
        scanf ( " %d " , &palpite);
        if (palpite == magico){
            printf ( " Parabens. Voce venceu \n " );
            retorna  0 ;
        } else if {
            printf ( " Você errou \n " );
            palpite > mágico ? printf ( " Foi alto \n " ): printf ( " Foi baixo \n " );
        }
        if (cont== 7 ) {
            printf ( " Suas chances terminaram \n " );
            printf ( " O numero era: %d " , magico);
            return  0 ;
        }
    }
}


/*
* Durante uma corrida de automóveis com N voltas (onde
* 0 < N < 15) de duração foram anotados, para um piloto,
* na ordem, os tempos registrados em cada volta. fazer
* um programa em C para ler os tempos das N voltas.
* Calcular e imprimir:
* a) melhor tempo;
* b) a volta em que ocorreu o melhor tempo;
* c) tempo médio das N voltas
 */
# include  < stdio.h >
int  principal () {
    int nvoltas= 0 , melhorVolta= 0 ;
    tempo duplo , tempomedio= 0.0 , somaTempo= 0.0 , menorTempo= 0.0 ;
    fazer {
        printf ( " Digite o numero de voltas: " );
        scanf ( " %d " , &nvoltas);
    } while (nvoltas<= 0 || nvoltas>= 15 );
    for ( int i = 1 ; i <= nvoltas; ++i) {
        printf ( " Digite o tempo da %d a) volta \n " ,i);
        scanf ( " %lf " , &tempo);
        se (i== 1 ){
            menorTempo = tempo;
            melhorVolta = 1 ;
        }
        if (tempo < menorTempo){
            menorTempo = tempo;
            melhorVolta = i;
        }
        somaTempo+= tempo;
    }
    tempomedio = somaTempo / nvoltas;
    printf ( " Melhor volta em tempo: %lf  \n " , menorTempo);
    printf ( " Melhor volta numerica: %d  \n " ,melhorVolta);
    printf ( " Tempo medio das voltas: %lf  \n " ,tempomedio);
    retorna  0 ;
}


# include  < stdio.h >
/*
* Fazer um programa em C para calcular a somatória dos
* N primeiros divisores de um inteiro X, onde N e X
* são lidos e são números inteiros e positivos.
* [Validar entradas].
 */
int  principal () {
    int x, n;
    printf ( " Entre com o valor inteiro e positivo de x: \n " );
    scanf ( " %d " , &x);
    fazer {
        printf ( " Digite o valor inteiro e positivo de n: \n " );
        scanf ( " %d " , &n);
    } while (n<= 0 || n>x);
    int soma = 0 ;
    int contdivisores = 0 ;
    for ( int i = 1 ; i <= x; ++i) {
       if (x % i == 0 ) {
           soma+=i;
           contdivisores++;
       }
       if (contdivisores == n) break ;
    }
    printf ( " Somatoria eh: %d  \n " ,soma);
    printf ( " Quantidade de divisores considerados: %d  \n " , contdivisores);
    retorna  0 ;
}


# include  < stdio.h >
/*
* Faça o programa que apresenta a seguinte saída,
* acompanhando o usuário o número máximo (no exemplo, 9).
* Este número deve ser sempre ímpar.
 */
int  principal () {
    int n;
    fazer {
        printf ( " Digite um valor impar \n " );
        scanf ( " %d " , &n);
    } while (n% 2 == 0 );
    for ( int i = 1 ; i <= n; i++) {
        for ( int j = i; j <= n; j++) {
            printf ( " %d  " , j);
        }
        printf ( " \n " );
    }
    retorna  0 ;
}


# include  < stdio.h >
/*
* Escreva um programa em C para ler 04 pares de valores
* inteiros e positivos, valide essa entrada. Para cada
* por lido deve ser impresso o valor do maior
* elemento do par ou a frase "Valores Iguais" quando o forem.
 */
int  principal () {
    int num1, num2;
    for ( int i = 1 ; i <= 4 ; i++) {
        // Estrutura para receber quatro pares de valores
        fazer {
            printf ( " Entre com dois valores inteiros e positivos: \n " );
            scanf ( " %d%d " , &num1, &num2);
        } while (num1 <= 0 || num2<= 0 );
        if (num1 == num2){
            printf ( " Par de valores entrados eh igual \n " );
        } senão {
            if (num1 > num2){
                printf ( " Primeiro numero eh maior: %d  \n " , num1);
            } senão {
                printf ( " Segundo numero eh maior: %d  \n " , num2);
            }
        }
    }
    retorna  0 ;
}


# include  < stdio.h >
/*
* Escreva um programa que leia 05 números inteiros positivos. Para cada número
* informei escrever a soma de seus divisores (exceto ele mesmo).
 */
int  principal () {
    int num;
    for ( int i = 1 ; i <= 5 ; i++) {
        // cinco entradas de dados
        fazer {
            printf ( " Digite um valor maior que 0: (inteiro) \n " );
            scanf ( " %d " , &num);
        } while (num <= 0 );
        int soma = 0 ; // declarar ou zerar a variável neste ponto
        for ( int j= 1 ; j<=(num/ 2 ); j++){ // verifica a metade do numero
            if (num % j == 0 ) soma+=j;
        }
        printf ( " Somatória dos divisores exatos: %d  \n " ,soma);
    }
    retorna  0 ;
}


# include  < stdio.h >
/*
* Escreva um programa que leia 3 notas de 5 alunos e a média
* das notas dos exercícios realizados por eles. Calcular um
* média de aproveitamento, usando a fórmula:
* MA = (N1 + N2*2 + N3*3 + EM)/7.
 */
int  principal () {
    duplo ma, n1, n2, n3, eu;
    // para cinco alunos, faremos a entrada
    for ( int i = 1 ; i <= 5 ; i++) {
        printf ( " Digitar 3 notas separadas por um espaço: \n " );
        scanf ( " %lf%lf%lf " , &n1, &n2, &n3);
        printf ( " Digite a Media de Aproveitamento: \n " );
        scanf ( " %lf " , &me);
        ma = (n1 + n2* 2 + n3* 3 + mim) / 7 ;
        printf ( " A media deste aluno eh: %2.2lf \n " , ma);
    }
    retorna  0 ;
}


# include  < stdio.h >
/*
* Faça um programa que com uso da estrutura for.
* Determine se um número dado pelo usuário é primo, ou não
 */
int  principal () {
    int num;
    int primo = 1 ;
    printf ( " Digite um numero: \n " );
    scanf ( " %d " , &num);
    for ( int i = 2 ; i <= num/ 2 ; i++) {
        if (num % i == 0 ) {
            prima = 0 ;
            quebrar ;
        }
    }
    if (primeiro){
        printf ( " O numero %d eh primo \n " , num);
    } senão {
        printf ( " O numero %d nao eh primo \n " , num);
    }
    retorna  0 ;
}


# include  < stdio.h >
/*
* Faça um programa que receba 10 dados do usuário e mostre a
* média dos valores entrados por ele, use uma estrutura while,
* para receber dez valores ou sair quando o usuário entrar com o valor 0.
 */
int  principal () {
    mídia dupla = 0,0 ;
    int cont= 0 , num;
    enquanto (cont< 10 ){
        printf ( " Digite um valor, ou 0 para finalizar: \n " );
        scanf ( " %d " , &num);
        média += num;
        cont++;
        if (num== 0 ) break ;
    }
    mídia /= cont;
    printf ( " Valor da mídia: %.2lf  \n " , mídia);
    retorna  0 ;
}