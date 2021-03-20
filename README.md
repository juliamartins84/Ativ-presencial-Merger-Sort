Algoritmo "Mergesort"
// Disciplina  : Linguagem e Lógica de Programação
// Professor   : Fernando Maransatto
// Autor(a)    : Júlia Martins
// Data atual  : 20/03/2021

var
   vetor_inicial: vetor [1..7] de inteiro
   x,inicial,final:inteiro

inicio

   vetor_inicial[1]:=28
   escreval(vetor_inicial[1])
   vetor_inicial[2]:=14
   escreval(vetor_inicial[2])
   vetor_inicial[3]:=7
   escreval(vetor_inicial[3])
   vetor_inicial[4]:=44
   escreval(vetor_inicial[4])
   vetor_inicial[5]:=63
   escreval(vetor_inicial[5])
   vetor_inicial[6]:=25
   escreval( vetor_inicial[6])
   vetor_inicial[7]:=19
   escreval(vetor_inicial[7])
   escreval()
   escreval("")

   inicial:=1
   final:=7


Procedimento Merge_Sort(inicial, final: inteiro )
var
   meio:inteiro
   
   
inicio
   se (inicial <  final) entao
      meio:=(inicial + final) div 2
      Merge_Sort (inicial, meio)
      Merge_Sort (meio+1, final)
      Merge (inicial, meio, final)
   fimse
fimprocedimento


procedimento Merge (inicial, meio, final: inteiro )

var
   primeiro,segundo,terceiro,quarto:inteiro
   vetor_final: vetor [1..7] de inteiro

inicio

   primeiro:=inicial;
   segundo:=inicial;
   terceiro:=meio + 1;
   enquanto (primeiro<=meio) e (terceiro<=final) faca

      se vetor_inicial[primeiro] <=    vetor_inicial[terceiro] entao
         vetor_final[segundo]:=   vetor_inicial[primeiro];
         primeiro:= primeiro + 1;
      senao
         vetor_final[segundo]:=   vetor_inicial[terceiro];
         terceiro:= terceiro + 1;
      fimse
     segundo:= segundo + 1;
   fimenquanto
   se primeiro > meio entao
      Para quarto de terceiro ate final faca
         vetor_final[segundo]:=    vetor_inicial[quarto];
         segundo:= segundo + 1;
      fimpara
   senao
      Para quarto de primeiro ate meio faca
         vetor_final[segundo]:=   vetor_inicial[quarto];
         segundo:= segundo + 1;
      fimpara
   fimse
   para quarto de inicial ate final faca
      vetor_inicial[quarto]:=vetor_final[quarto];
   fimpara
fimprocedimento

Merge_sort(inicial, final )

para x de 1 ate 7 faca
   escreva (   vetor_inicial[x])
fimpara
fimalgoritmo
