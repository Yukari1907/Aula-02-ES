# Aula02-ES

Parte 1:

Requisitos Funcionais (RF)

- RF01: O sistema deve converter temperatura de Celsius para Fahrenheit.

- RF02: O sistema deve converter temperatura de Fahrenheit para Celsius.

- RF03: O sistema deve permitir que o usuário escolha o tipo de conversão e informe o valor da temperatura.

- RF04: O sistema deve exibir o resultado da conversão formatado com uma casa decimal.

Requisitos Não-Funcionais (RNF)

- RNF01 (Usabilidade): O sistema deve possuir interface simples e intuitiva no terminal.

- RNF02 (Desempenho): A conversão deve ser realizada imediatamente após a entrada do usuário.

- RNF03 (Confiabilidade): O sistema deve tratar entradas inválidas (ex: letras no lugar de números).

Parte 2

# ====================================
# CONVERSOR DE TEMPERATURA
# Exercício - Engenharia de Software
# ====================================

def celsius_para_fahrenheit(celsius):
    """
    RF01: Converter Celsius para Fahrenheit
    Fórmula: F = (C × 9/5) + 32
    """
    return (celsius * 9/5) + 32


def fahrenheit_para_celsius(fahrenheit):
    """
    RF02: Converter Fahrenheit para Celsius
    Fórmula: C = (F - 32) × 5/9
    """
    return (fahrenheit - 32) * 5/9


# ====================================
# PROGRAMA PRINCIPAL
# ====================================

print("="*40)
print("  CONVERSOR DE TEMPERATURA")
print("="*40)

print("Escolha a conversão:")
print("1 - Celsius → Fahrenheit")
print("2 - Fahrenheit → Celsius")

opcao = input("Opção: ")

try:
    if opcao == "1":
        temperatura = float(input("Digite a temperatura em Celsius: "))
        resultado = celsius_para_fahrenheit(temperatura)
        print("="*40)
        print(f"{temperatura:.1f}°C = {resultado:.1f}°F")

    elif opcao == "2":
        temperatura = float(input("Digite a temperatura em Fahrenheit: "))
        resultado = fahrenheit_para_celsius(temperatura)
        print("="*40)
        print(f"{temperatura:.1f}°F = {resultado:.1f}°C")

    else:
        print("Opção inválida!")

except ValueError:
    print("Erro: Digite apenas números válidos para a temperatura.")

print("="*40)
