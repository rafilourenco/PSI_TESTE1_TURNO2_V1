# Teste de PSI 1 - Turno 2 - Versão 1

## Informação do aluno

    Nome: Rafael Lourenço

Teste termina às 13:25.

Escreve as respostas dentro dos blocos correspondentes.
Substitui as reticências pelo que é pedido em cada pergunta.
Não desformates o documento.

### P1. Indica o que é impresso pelo seguinte código. Justifica a tua resposta

    bool x = true && false;
    x |= 2 < 5;
    
    Console.WriteLine(x);

P1 - Resposta

    Vai imprimir True.
    Portanto, o bool x é false porque true && false porque no operador bit-a-bit AND verdadeiro com falso equivale a falso, mas de seguida é feito x |=, ou seja operador OR e apresenta 2 < 5 o que é True /verdadeiro, o que resta falso OU verdadeiro o que equivale a TRUE. 

### P2. Considera o seguinte código com um *bug*

    short s = long.MaxValue;

    Console.WriteLine(s);

### Indica uma possível correção para que o código não apresente erros. Explica porque foi necessário fazer essa correção 

P2 - Resposta
    
    Ocorre um erro pois as variaveis são de tipo diferente short e long, é necessario que sejam ambas do mesmo tipo.
    Existem duas resoluções possiveis, a primeira sendo substituir a variavel "s" por long, logo long s = long.MaxValue; Que da 9223372036854775807. Ou a segundo sendo substituir o long.MaxValue para short.MaxValue, ou seja short s = short.MaxValue; que ira apresentar 32767.

### P3. Escreve um programa que solicite ao utilizador dois números reais e apresente o resultado do primeiro (base) elevado ao segundo (expoente). Não podes usar um método da classe Math para obter o resultado

P3 - Resposta

            // Declaração das variaveis
            double base1;
            double expoente;
            double resultado = 1;
            
            // Solicitação dos valores
            Console.WriteLine("Introduza o primeiro número: ");
            base1 = Convert.ToDouble(Console.ReadLine());
            Console.WriteLine("Introduza o segundo número: ");
            expoente = Convert.ToDouble(Console.ReadLine());

            // Ciclo for que ira multiplicar a base, durante um determinado tempo de ciclos que é o expoente
            for(int i = 1; i<= expoente;i++){
                resultado *= base1;
            }

            Console.WriteLine(resultado); // Imprimir o resultado

### P4. Estás na pasta raiz do teu repositório local, onde atualizaste um ficheiro de nome 'Classes.cs'. Queres enviar **apenas** esta atualização para o teu repositório remoto. Indica os comandos necessários. A mensagem de commit deve ser apropriada

P4 - Resposta

    git add Classes.cs
    git commit -m "Atualização de Classes"
    git push
