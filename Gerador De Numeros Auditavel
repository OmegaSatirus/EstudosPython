import random 

Confirmacaodegeracao = 0
BD = []
contador = 0
Prosseguir = "sim"

def GeracaoDeNumeros():
    global Confirmacaodegeracao
    global contador

    while True:
        Sequencia = ''.join(map(str, random.sample(range(0, 10), 9)))      
        if Sequencia not in BD:
            contador += 1
            Confirmacaodegeracao = 1  
            return Sequencia

def ArmazemAuditavel(Sequencia, Confirmacaodegeracao):
    global BD
    global contador 
    if Confirmacaodegeracao == 1:
        BD.insert(contador - 1, Sequencia)
        Confirmacaodegeracao = 0

# Loop principal
while Prosseguir.lower() == "sim":
    # Gere a sequência de números sem repetição
    sequencia_gerada = GeracaoDeNumeros()

    # Verifique se a geração ocorreu
    if Confirmacaodegeracao == 1:
        ArmazemAuditavel(sequencia_gerada, Confirmacaodegeracao)
        print(BD)

    # Solicitação de input para continuar
    Prosseguir = input("Deseja continuar?\n sim \n Não: ")
