# Carteira-de-Investimentos-portugol-
 O cliente da corretora poderá definir um percentual de diversificação entre as seguintes opções de investimento:Algoritmo "mapa1"
// Disciplina   : [Algoritmo e Lógica de Programação I]
// Descrição   : o cliente da corretora poderá definir um percentual de
// diversificação de investimento:
// Autor(a)    : Ketlyn amanda Athan Gonçalves
// Data atual  : 25/06/2021
Var
   // Seção de Declarações das variáveis
   Invest: vetor[1..5] de caractere
   p: vetor[1..5] de inteiro
   d: vetor[1..5] de inteiro   //percentual Atual (deu erro por isso modifiquei)
   i, a, x, opcao: inteiro
   flag: logico
   b, c : inteiro
procedimento Investir
Inicio
   a <- 0
   b <- 20
   invest[1]<- "CDBs"
   invest[2]<- "Ações"
   invest[3]<- "Fundos de Investimento"
   invest[4]<- " Stoks "
   invest[5]<- "Reits "
   enquanto a <> 100 faca
      escreval(" O Valor Indicado é de:-> ", b , "%", "Para cada Categoria" )
      escreval("-----------------------------------------------------------")
      escreval(" Se não deseja investir em determinada categoria digite 0  ")
      escreval("-----------------------------------------------------------")
      para i de 1 ate 5 faca
         escreval(" Quanto % deseja  investir em: ", invest[i])
         leia(p[i])
         a <- a + p[i]
      fimpara
      se a <> 100 entao
         limpatela
         escreval("  Você não atingiu o limite esperado, Tente novamente! ")
         escreval("-------------------------------------------------------")
         escreval("OBS: -> Cada rodada de investimento o valor deve atingir 100 %")
         a <- 0
      senao
         se a = 100 entao
            escreval("------------------Rodada Concluida------------------")
            Escreval("---> Digite 2 para Verificar valores Investidos <---")
         fimse
      fimse
   fimenquanto
fimprocedimento
procedimento consultar
inicio
   c <- b * 100
   x <- a * 100
   escreval(" O Valor Indicado é de : --> ", b , "%", "Para cada Categoria" )
   escreval("--------------------------------------------------------------")
   escreval("Seu valor Investimento Atual é: ")
   para i de 1 ate 5 faca
      escreval("Você tem : ",p[i], "% em -->", invest[i])
      se p[i]< b entao
         escreval("Valor investido Abaixo do recomendado")
      senao
         se p[i]= b entao
            escreval("Investimento Balanceado")
         senao
            se p[i] > b entao
               escreval("Valor a cima do recomendado")
            fimse
         fimse
      fimse
   fimpara
   escreval ("Seu valor Investido em cada categoria é de  R$", c)
   escreval ("seu valor Total é --> R$ ", x)
   escreval("Seu total de investimento é : ", a, "%")
fimprocedimento
procedimento sobre
inicio
   escreval("  Uma carteira de investimentos bem diversificada  ")
   escreval(" Deve ser composta por ativos de renda fixa e renda variável")
   escreval(" muito importante o fator da > diversificação <   ")
   escreval("------------------------------------------------------------")
   escreval("---------OPÇÕES DE INVESTIMENTOS----------")
   escreval("")
   escreval("            Renda Fixa                     ")
   escreval("                 E                         ")
   escreval("                CDBs                       ")
   escreval("")
   escreval("            Renda VariaveL                ")
   escreval("              Que são:                    ")
   escreval("        Ações e Fundos ImobiliárioS       ")
   escreval("")
   escreval("     Uma boa opção para diversificação    ")
   escreval("              São STOCKS                  ")
   escreval("     Ações de empresas InternacionaiS     ")
   escreval("")
   escreval("               E os REITs                 ")
   escreval("     Fundos Imobiliários Internacionais   ")
   escreval("")
   escreval("")
fimprocedimento
procedimento menu
inicio
   opcao <- 0
   limpatela
   enquanto opcao <> 4 faca
      escreval("-----------------------------------------")
      escreval(" Bem Vindo A Sua Carteira de Investimentos")
      escreval("-----------------------------------------")
      escreval("Escolha a opção Desejada")
      escreval("1- Investir")
      escreval("2- Consultar")
      escreval("3- Sobre Investimento ")
      escreval("4- Sair ")
      escreval("Digite Opção")
      leia(opcao)
      escolha (opcao)
      caso 1
         limpatela()
         investir
      caso 2
         limpatela()
         consultar
      caso 3
         limpatela()
         sobre
      outrocaso
         limpatela()
         escreval("Sair...")
         leia(flag)
      fimescolha
   fimenquanto
fimprocedimento
inicio
   limpatela
   menu
fimalgoritmo


