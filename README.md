# Funções para as operações básicas

def adicao(a, b):
    return a + b

def subtracao(a, b):
    return a - b

def multiplicacao(a, b):
    return a * b

def divisao(a, b):
    if b != 0:
        return a / b
    else:
        return "Erro: divisão por zero"

# Função principal da calculadora

def calculadora():
    print("Bem-vindo à calculadora simples!")
    while True:
        print("Operações disponíveis:")
        print("1 - Adição")
        print("2 - Subtração")
        print("3 - Multiplicação")
        print("4 - Divisão")
        print("5 - Sair")
        
        op = input("Escolha a operação (1/2/3/4/5): ")
        
        if op == '5':
            print("Encerrando a calculadora.")
            break
        
        if op in ('1', '2', '3', '4'):
            try:
                num1 = float(input("Digite o primeiro número: "))
                num2 = float(input("Digite o segundo número: "))
                
                if op == '1':
                    print("Resultado:", adicao(num1, num2))
                elif op == '2':
                    print("Resultado:", subtracao(num1, num2))
                elif op == '3':
                    print("Resultado:", multiplicacao(num1, num2))
                elif op == '4':
                    print("Resultado:", divisao(num1, num2))
                    
            except ValueError:
                print("Erro: por favor, digite números válidos.")
            
        else:
            print("Opção inválida. Escolha novamente.")

# Chamada da função principal da calculadora
calculadora()
