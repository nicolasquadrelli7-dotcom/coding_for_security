# Exercício 1 — Verificador de Idade: Crie um programa...
def verificar_idade():
    idade = int(input("Digite sua idade: "))
    
    if idade < 0 or idade > 120:
        print("idade inválida")
    elif idade <= 11:
        print("criança")
    elif idade <= 17:
        print("adolescente")
    elif idade <= 59:
        print("adulto")
    else:
        print("idoso")

verificar_idade()> **Exercício 1 — Verificador de Idade:** Crie um programa que peça a idade do usuário e exiba se ele é criança (0-11), adolescente (12-17), adulto (18-59) ou idoso (60+). Se a idade for negativa ou maior que 120, exiba "Idade inválida".
>
> ```python
> # Teste com estas idades:
> idades = [5, 15, 25, 70, -3, 150]
>
> # Saída esperada:
> # Idade 5   → Criança
> # Idade 15  → Adolescente
> # Idade 25  → Adulto
> # Idade 70  → Idoso
> # Idade -3  → Idade inválida
> # Idade 150 → Idade inválida
> ```

> **E# Exercício 2 — Calculadora de IMC

def calcular_imc():
    peso = float(input("Digite seu peso: "))
    altura = float(input("Digite sua altura: "))

    imc = peso / (altura ** 2)

    print(f"Peso: {peso} kg | Altura: {altura} m")

    if imc < 18.5:
        print(f"IMC: {imc:.1f} - Abaixo do peso")
    elif imc <= 24.9:
        print(f"IMC: {imc:.1f} - Peso normal")
    elif imc <= 29.9:
        print(f"IMC: {imc:.1f} - Sobrepeso")
    else:
        print(f"IMC: {imc:.1f} - Obesidade")

calcular_imc()xercício 2 — Calculadora de IMC:** Crie um programa que peça peso (kg) e altura (m), calcule o IMC (peso / altura²) e exiba a classificação: abaixo do peso (< 18.5), peso normal (18.5 - 24.9), sobrepeso (25.0 - 29.9), obesidade (≥ 30.0). Exiba o resultado com 1 casa decimal.
>
> ```python
> # Teste com estes valores:
> testes = [
>     (52.0, 1.75),   # IMC 17.0 → Abaixo do peso
>     (70.0, 1.75),   # IMC 22.9 → Peso normal
>     (85.0, 1.70),   # IMC 29.4 → Sobrepeso
>     (110.0, 1.65),  # IMC 40.4 → Obesidade
> ]
>
> # Saída esperada:
> # Peso: 70.0 kg | Altura: 1.75 m
> # IMC: 22.9 - Peso normal
> ```

> *# Exercício 3 — Conversor de Moedas

cotacoes = {
    "dolar": 5.15,
    "euro": 5.55,
    "libra": 6.45
}

print("[1] Real → Dólar")
print("[2] Real → Euro")
print("[3] Real → Libra")

opcao = input("Escolha uma opção: ")

if opcao == "1":
    valor = float(input("Digite o valor em reais: "))
    if valor < 0:
        print("Valor inválido")
    else:
        convertido = valor / cotacoes["dolar"]
        print(f"R$ {valor:.2f} = US$ {convertido:.2f}")

elif opcao == "2":
    valor = float(input("Digite o valor em reais: "))
    if valor < 0:
        print("Valor inválido")
    else:
        convertido = valor / cotacoes["euro"]
        print(f"R$ {valor:.2f} = € {convertido:.2f}")

elif opcao == "3":
    valor = float(input("Digite o valor em reais: "))
    if valor < 0:
        print("Valor inválido")
    else:
        convertido = valor / cotacoes["libra"]
        print(f"R$ {valor:.2f} = £ {convertido:.2f}")

else:
    print("Opção inválida")*Exercício 3 — Conversor de Moedas:** Crie um programa que exiba um menu com 3 opções de conversão: Real → Dólar, Real → Euro, Real → Libra. O usuário escolhe a opção, digita o valor em reais e o programa exibe o valor convertido com 2 casas decimais. Se o usuário escolher uma opção inválida, exiba "Opção inválida". Se digitar um valor negativo, exiba "Valor inválido".
>
> ```python
> # Cotações fixas para o exercício:
> cotacoes = {
>     "dolar": 5.15,
>     "euro": 5.55,
>     "libra": 6.45
> }
>
> # Menu:
> # [1] Real → Dólar
> # [2] Real → Euro
> # [3] Real → Libra
>
> # Teste: opção 1, valor R$ 100.00
> # Saída: R$ 100.00 = US$ 19.42
>
> # Teste: opção 2, valor R$ 250.00
> # Saída: R$ 250.00 = € 45.05
>
> # Teste: opção 5
> # Saída: Opção inválida
> ```

> **Exercício 4 — Classificador de Triângulos:** Crie um programa que peça 3 valores representando os lados de um triângulo. Primeiro, verifique se os valores formam um triângulo válido (a soma de dois lados deve ser maior que o terceiro — teste as 3 combinações). Se for válido, classifique como equilátero (3 lados iguais), isósceles (2 lados iguais) ou escaleno (3 lados diferentes). Se não for válido, exiba "Não forma triângulo".
>#Exercício 4 — Classificador de Triângulos

a = float(input("Digite o primeiro lado: "))
b = float(input("Digite o segundo lado: "))
c = float(input("Digite o terceiro lado: "))

print(f"Lados: {a}, {b}, {c}")

if a <= 0 or b <= 0 or c <= 0:
    print("Não forma triângulo")

elif a + b > c and a + c > b and b + c > a:
    
    if a == b and b == c:
        print("Triângulo válido: Equilátero")
    
    elif a == b or a == c or b == c:
        print("Triângulo válido: Isósceles")
    
    else:
        print("Triângulo válido: Escaleno")

else:
    print("Não forma triângulo")
> ```python
> # Teste com estes valores:
> testes = [
>     (5, 5, 5),    # Equilátero
>     (5, 5, 3),    # Isósceles
>     (3, 4, 5),    # Escaleno
>     (1, 2, 10),   # Não forma triângulo (1 + 2 < 10)
>     (0, 5, 5),    # Não forma triângulo (lado zero)
>     (7, 7, 12),   # Isósceles
> ]
>
> # Saída esperada:
> # Lados: 3, 4, 5
> # Triângulo válido: Escaleno
> #
> # Lados: 1, 2, 10
> # Não forma triângulo
> ```

> #Exercício 5 — Calculadora de Desconto Progressivo

valor = float(input("Digite o valor da compra: "))
vip = input("Cliente VIP? (sim/nao): ")

if valor <= 100:
    desconto = 0
elif valor <= 300:
    desconto = 0.10
elif valor <= 500:
    desconto = 0.15
else:
    desconto = 0.20

valor_desconto = valor * desconto

if vip == "sim":
    desconto_vip = valor * 0.05
else:
    desconto_vip = 0

valor_final = valor - valor_desconto - desconto_vip

print("=== Resumo da Compra ===")
print(f"Valor original:  R$ {valor:.2f}")
print(f"Desconto ({desconto*100:.0f}%):  R$ {valor_desconto:.2f}")

if desconto_vip > 0:
    print(f"Desconto VIP (5%): R$ {desconto_vip:.2f}")

print(f"Valor final:     R$ {valor_final:.2f}")**Exercício 5 — Calculadora de Desconto Progressivo:** Crie um programa para uma loja que aplica descontos baseados no valor da compra: até R$ 100 não tem desconto, de R$ 100.01 a R$ 300 tem 10% de desconto, de R$ 300.01 a R$ 500 tem 15%, acima de R$ 500 tem 20%. Além disso, se o cliente for VIP (pergunte sim ou não), ganha 5% extra em qualquer faixa. Exiba o valor original, o desconto aplicado, o desconto VIP (se houver) e o valor final.
>
> ```python
> # Teste com estes valores:
> testes = [
>     (80.00,  "nao"),  # Sem desconto, sem VIP
>     (200.00, "nao"),  # 10% = R$ 20.00 → R$ 180.00
>     (200.00, "sim"),  # 10% + 5% VIP = R$ 30.00 → R$ 170.00
>     (450.00, "nao"),  # 15% = R$ 67.50 → R$ 382.50
>     (1000.00, "sim"), # 20% + 5% VIP = R$ 250.00 → R$ 750.00
> ]
>
> # Saída esperada (compra R$ 200.00, VIP sim):
> # === Resumo da Compra ===
> # Valor original:  R$ 200.00
> # Desconto (10%):  R$ 20.00
> # Desconto VIP (5%): R$ 10.00
> # Valor final:     R$ 170.00
> ```

> #Exercício 6 — Verificador de Ano Bissexto e Dia da Semana

dia = int(input("Digite o dia: "))
mes = int(input("Digite o mês: "))
ano = int(input("Digite o ano: "))

print(f"Data: {dia:02d}/{mes:02d}/{ano}")

if (ano % 4 == 0 and ano % 100 != 0) or (ano % 400 == 0):
    bissexto = True
else:
    bissexto = False

if bissexto:
    print("Ano bissexto: Sim")
else:
    print("Ano bissexto: Não")

if mes < 1 or mes > 12:
    print("Data inválida: mês inválido")

else:
    if mes in [1, 3, 5, 7, 8, 10, 12]:
        max_dias = 31
    elif mes in [4, 6, 9, 11]:
        max_dias = 30
    else:
        if bissexto:
            max_dias = 29
        else:
            max_dias = 28

    if dia < 1:
        print("Data inválida: dia inválido")
    elif dia > max_dias:
        print(f"Data inválida: mês {mes} tem apenas {max_dias} dias")
    else:
        print("Data válida!")**Exercício 6 — Verificador de Ano Bissexto e Dia da Semana:** Crie um programa que peça uma data (dia, mês e ano, separados) e verifique: se o ano é bissexto (divisível por 4, exceto os divisíveis por 100, exceto os divisíveis por 400), se o mês é válido (1-12), se o dia é válido para aquele mês (considere meses com 28/29, 30 ou 31 dias), e exiba a data formatada. Se qualquer valor for inválido, exiba o motivo.
>
> ```python
> # Dias por mês:
> # 31 dias: janeiro(1), março(3), maio(5), julho(7), agosto(8), outubro(10), dezembro(12)
> # 30 dias: abril(4), junho(6), setembro(9), novembro(11)
> # 28/29 dias: fevereiro(2) — 29 se bissexto, 28 se não
>
> # Teste com estas datas:
> testes = [
>     (29, 2, 2024),   # Válida — 2024 é bissexto
>     (29, 2, 2023),   # Inválida — 2023 não é bissexto
>     (31, 4, 2025),   # Inválida — abril tem 30 dias
>     (15, 8, 2025),   # Válida — 15/08/2025
>     (29, 2, 2000),   # Válida — 2000 é bissexto (divisível por 400)
>     (29, 2, 1900),   # Inválida — 1900 NÃO é bissexto (divisível por 100)
>     (5, 13, 2025),   # Inválida — mês 13 não existe
>     (0, 6, 2025),    # Inválida — dia 0 não existe
> ]
>
> # Saída esperada:
> # Data: 29/02/2024
> # Ano bissexto: Sim
> # Data válida!
> #
> # Data: 29/02/2023
> # Ano bissexto: Não
> # Data inválida: fevereiro de 2023 tem apenas 28 dias
> ```

> **Exercício 7 — Simulador de Caixa Eletrônico:** Crie um programa que simule um caixa eletrônico. O usuário digita um valor de saque (inteiro, múltiplo de 10) e o programa calcula a menor quantidade de cédulas necessárias. Cédulas disponíveis: R$ 200, R$ 100, R$ 50, R$ 20 e R$ 10. Valide se o valor é positivo, inteiro e múltiplo de 10. Exiba cada cédula usada e a quantidade.
>
> ```python
> # Teste com estes valores:
> testes = [
>     380,    # 1x R$200, 1x R$100, 1x R$50, 1x R$20, 1x R$10
>     1250,   # 6x R$200, 0x R$100, 1x R$50, 0x R$20, 0x R$10
>     70,     # 0x R$200, 0x R$100, 1x R$50, 1x R$20, 0x R$10
>     15,     # Inválido — não é múltiplo de 10
>     -100,   # Inválido — valor negativo
>     0,      # Inválido — valor zero
> ]
>
> # Saída esperada (saque R$ 380):
> # === Saque: R$ 380 ===
> # R$ 200: 1 cédula(s)
> # R$ 100: 1 cédula(s)
> # R$ 50:  1 cédula(s)
> # R$ 20:  1 cédula(s)
> # R$ 10:  1 cédula(s)
> # Total de cédulas: 5
> ```
#Exercício 7 — Simulador de Caixa Eletrônica

valor = int(input("Digite o valor do saque: "))

if valor <= 0:
    print("Valor inválido")

elif valor % 10 != 0:
    print("Valor inválido")

else:
    print(f"=== Saque: R$ {valor} ===")

    ced200 = valor // 200
    valor = valor % 200

    ced100 = valor // 100
    valor = valor % 100

    ced50 = valor // 50
    valor = valor % 50

    ced20 = valor // 20
    valor = valor % 20

    ced10 = valor // 10
    valor = valor % 10

    print(f"R$ 200: {ced200} cédula(s)")
    print(f"R$ 100: {ced100} cédula(s)")
    print(f"R$ 50:  {ced50} cédula(s)")
    print(f"R$ 20:  {ced20} cédula(s)")
    print(f"R$ 10:  {ced10} cédula(s)")

    total = ced200 + ced100 + ced50 + ced20 + ced10
    print(f"Total de cédulas: {total}")
> **Exercício 8 — Calculadora de Estacionamento:** Crie um programa para calcular o valor do estacionamento. A tarifa funciona assim: primeira hora custa R$ 10.00, horas adicionais custam R$ 5.00 cada (não tem meia hora — qualquer fração conta como hora cheia), entre 22h e 6h cobra adicional noturno de 50% sobre o total, e carros com placa terminando em número par ganham 10% de desconto às segundas-feiras. O programa deve pedir: hora de entrada, hora de saída (formato 24h, apenas horas inteiras), último número da placa e dia da semana. Exiba o detalhamento completo.
>
> ```python
> # Teste com estes cenários:
> testes = [
>     {"entrada": 14, "saida": 16, "placa_final": 3, "dia": "quarta"},
>     # 2 horas: R$10 + R$5 = R$15.00
>
>     {"entrada": 9,  "saida": 9,  "placa_final": 7, "dia": "sexta"},
>     # Menos de 1 hora: R$10.00 (mínimo)
>
>     {"entrada": 23, "saida": 2,  "placa_final": 5, "dia": "sabado"},
>     # 3 horas noturnas: (R$10 + R$5 + R$5) * 1.50 = R$30.00
>
>     {"entrada": 8,  "saida": 12, "placa_final": 4, "dia": "segunda"},
>     # 4 horas: R$10 + R$5 + R$5 + R$5 = R$25.00, desconto 10% = R$22.50
>
>     {"entrada": 20, "saida": 3,  "placa_final": 2, "dia": "segunda"},
>     # 7 horas, noturno + desconto segunda placa par
> ]
>
> # Saída esperada (cenário 3):
> # === Estacionamento ===
> # Entrada: 23h | Saída: 02h
> # Permanência: 3 horas
> # Tarifa base:     R$ 20.00
> # Adicional noturno (50%): R$ 10.00
> # Total:           R$ 30.00
> ```
#Exercício 8 — Calculadora de Estacionamento

entrada = int(input("Hora de entrada: "))
saida = int(input("Hora de saída: "))
placa = int(input("Último número da placa: "))
dia = input("Dia da semana: ")

# Calcular horas
if saida < entrada:
    horas = (24 - entrada) + saida
else:
    horas = saida - entrada

if horas == 0:
    horas = 1

# Tarifa base
if horas == 1:
    base = 10
else:
    base = 10 + (horas - 1) * 5

# Adicional noturno
if entrada >= 22 or entrada < 6:
    adicional_noturno = base * 0.5
else:
    adicional_noturno = 0

# Desconto
if dia == "segunda" and placa % 2 == 0:
    desconto = (base + adicional_noturno) * 0.10
else:
    desconto = 0

# Total
total = base + adicional_noturno - desconto

# Saída
print("=== Estacionamento ===")
print(f"Entrada: {entrada}h | Saída: {saida:02d}h")
print(f"Permanência: {horas} horas")
print(f"Tarifa base:     R$ {base:.2f}")

if adicional_noturno > 0:
    print(f"Adicional noturno (50%): R$ {adicional_noturno:.2f}")

if desconto > 0:
    print(f"Desconto (10%): R$ {desconto:.2f}")

print(f"Total:           R$ {total:.2f}")
> **Exercício 9 — Jogo de Pedra, Papel, Tesoura, Lagarto, Spock:** Crie o jogo expandido (da série The Big Bang Theory). O usuário escolhe por número (1-5) e o computador escolhe aleatoriamente. As regras são: Tesoura corta Papel, Papel cobre Pedra, Pedra esmaga Lagarto, Lagarto envenena Spock, Spock derrete Tesoura, Tesoura decapita Lagarto, Lagarto come Papel, Papel refuta Spock, Spock vaporiza Pedra, Pedra quebra Tesoura. Exiba as escolhas, quem ganhou e o motivo (ex: "Spock vaporiza Pedra"). Use o módulo `random` para a escolha do computador — importe com `import random` e use `random.randint(1, 5)` para gerar um número aleatório entre 1 e 5.
>
> ```python
> import random
>
> # Opções:
> # 1 = Pedra
> # 2 = Papel
> # 3 = Tesoura
> # 4 = Lagarto
> # 5 = Spock
>
> # Tabela de vitórias — quem a chave vence e com qual ação:
> # Pedra    vence Tesoura ("quebra") e Lagarto ("esmaga")
> # Papel    vence Pedra ("cobre") e Spock ("refuta")
> # Tesoura  vence Papel ("corta") e Lagarto ("decapita")
> # Lagarto  vence Papel ("come") e Spock ("envenena")
> # Spock    vence Pedra ("vaporiza") e Tesoura ("derrete")
>
> # Teste: Jogador escolhe 5 (Spock), computador escolhe 1 (Pedra)
> # Saída:
> # Você: Spock
> # Computador: Pedra
> # Spock vaporiza Pedra — Você venceu!
>
> # Teste: Jogador escolhe 3 (Tesoura), computador escolhe 5 (Spock)
> # Saída:
> # Você: Tesoura
> # Computador: Spock
> # Spock derrete Tesoura — Computador venceu!
>
> # Teste: Jogador escolhe 2 (Papel), computador escolhe 2 (Papel)
> # Saída:
> # Você: Papel
> # Computador: Papel
> # Empate!
> ```
#Exercício 9 — Jogo de Pedra, Papel, Tesoura, Lagarto, Spock

import random

print("1 = Pedra")
print("2 = Papel")
print("3 = Tesoura")
print("4 = Lagarto")
print("5 = Spock")

jogador = int(input("Escolha uma opção: "))
computador = random.randint(1, 5)

nomes = {
    1: "Pedra",
    2: "Papel",
    3: "Tesoura",
    4: "Lagarto",
    5: "Spock"
}

regras = {
    1: {3: "quebra", 4: "esmaga"},
    2: {1: "cobre", 5: "refuta"},
    3: {2: "corta", 4: "decapita"},
    4: {2: "come", 5: "envenena"},
    5: {1: "vaporiza", 3: "derrete"}
}

print(f"Você: {nomes[jogador]}")
print(f"Computador: {nomes[computador]}")

if jogador == computador:
    print("Empate!")

elif computador in regras[jogador]:
    acao = regras[jogador][computador]
    print(f"{nomes[jogador]} {acao} {nomes[computador]} — Você venceu!")

else:
    acao = regras[computador][jogador]
    print(f"{nomes[computador]} {acao} {nomes[jogador]} — Computador venceu!")
> **Exercício 10 (Desafio) — Calculadora de Imposto de Renda 2025:** Crie um programa completo que calcule o Imposto de Renda mensal de um funcionário. O programa deve pedir: salário bruto mensal, número de dependentes, se paga pensão alimentícia (e qual valor) e se tem 65 anos ou mais. O cálculo segue estas etapas nesta ordem:
>
> **Etapa 1 — Base de cálculo:**
> Comece com o salário bruto. Desconte INSS usando a tabela progressiva (calcule faixa por faixa, não aplique a alíquota sobre o total). Depois desconte R$ 189.59 por dependente e o valor da pensão alimentícia (se houver). Se o funcionário tem 65+ anos, desconte mais R$ 1.903.98 de isenção extra. O resultado é a base de cálculo do IR.
>
> **Etapa 2 — INSS progressivo:**
>
> ```python
> # Tabela INSS 2025 (calcule faixa por faixa):
> # Até R$ 1.518.00         → 7.5%
> # De R$ 1.518.01 a R$ 2.793.88  → 9%
> # De R$ 2.793.89 a R$ 4.190.83  → 12%
> # De R$ 4.190.84 a R$ 8.157.41  → 14%
> # Acima de R$ 8.157.41   → teto (não desconta mais)
> #
> # Exemplo para salário R$ 5.000.00:
> # Faixa 1: 1.518.00 * 7.5% = 113.85
> # Faixa 2: (2.793.88 - 1.518.00) * 9% = 114.83
> # Faixa 3: (4.190.83 - 2.793.88) * 12% = 167.63
> # Faixa 4: (5.000.00 - 4.190.83) * 14% = 113.28
> # Total INSS: R$ 509.59
> ```
>
> **Etapa 3 — IR progressivo (sobre a base de cálculo):**
>
> ```python
> # Tabela IR 2025 (também progressiva, faixa por faixa):
> # Até R$ 2.259.20         → isento
> # De R$ 2.259.21 a R$ 2.826.65  → 7.5%
> # De R$ 2.826.66 a R$ 3.751.05  → 15%
> # De R$ 3.751.06 a R$ 4.664.68  → 22.5%
> # Acima de R$ 4.664.68   → 27.5%
> ```
>
> ```python
> # Teste com estes cenários:
> testes = [
>     {"salario": 2000.00, "dependentes": 0, "pensao": 0, "idoso": False},
>     # INSS: R$ 157.17 | Base: R$ 1.842.83 | IR: isento
>
>     {"salario": 5000.00, "dependentes": 2, "pensao": 0, "idoso": False},
>     # INSS: R$ 509.59 | Dedução dep: R$ 379.18 | Base: R$ 4.111.23 | IR: R$ 263.02
>
>     {"salario": 8000.00, "dependentes": 1, "pensao": 500, "idoso": False},
>     # INSS: R$ 872.77 | Dedução dep: R$ 189.59 | Pensão: R$ 500 | Base: R$ 6.437.64
>
>     {"salario": 3500.00, "dependentes": 0, "pensao": 0, "idoso": True},
>     # INSS: R$ 401.36 | Isenção idoso: R$ 1.903.98 | Base: R$ 1.194.66 | IR: isento
> ]
>
> # Saída esperada (cenário 2):
> # ====================================
> # CONTRACHEQUE — Cálculo de IR Mensal
> # ====================================
> # Salário bruto:       R$ 5.000,00
> #
> # (-) INSS:            R$ 509,59
> #     Faixa 7.5%:      R$ 113,85
> #     Faixa 9%:        R$ 114,83
> #     Faixa 12%:       R$ 167,63
> #     Faixa 14%:       R$ 113,28
> #
> # (-) Dependentes (2): R$ 379,18
> # (-) Pensão:          R$ 0,00
> # (-) Isenção 65+:     R$ 0,00
> #
> # Base de cálculo IR:  R$ 4.111,23
> #
> # (-) IR:              R$ 263,02
> #     Faixa isenta:    R$ 0,00
> #     Faixa 7.5%:      R$ 42,56
> #     Faixa 15%:       R$ 138,66
> #     Faixa 22.5%:     R$ 81,04
> #     Faixa 27.5%:     R$ 0,00
> #
> # ====================================
> # Salário líquido:     R$ 4.227,39
> # ====================================
> ```
> #Exercício 10 (Desafio) — Calculadora de Imposto de Renda 2025

def calcular_inss(salario):
    inss = 0

    # Faixa 1
    faixa1 = min(salario, 1518.00)
    inss_f1 = faixa1 * 0.075
    inss += inss_f1

    # Faixa 2
    if salario > 1518.00:
        faixa2 = min(salario, 2793.88) - 1518.00
        inss_f2 = faixa2 * 0.09
        inss += inss_f2
    else:
        inss_f2 = 0

    # Faixa 3
    if salario > 2793.88:
        faixa3 = min(salario, 4190.83) - 2793.88
        inss_f3 = faixa3 * 0.12
        inss += inss_f3
    else:
        inss_f3 = 0

    # Faixa 4
    if salario > 4190.83:
        faixa4 = min(salario, 8157.41) - 4190.83
        inss_f4 = faixa4 * 0.14
        inss += inss_f4
    else:
        inss_f4 = 0

    return inss, inss_f1, inss_f2, inss_f3, inss_f4


def calcular_ir(base_ir):
    ir = 0

    # Faixa isenta
    ir_f1 = 0

    # Faixa 7.5%
    if base_ir > 2259.20:
        faixa2 = min(base_ir, 2826.65) - 2259.20
        ir_f2 = faixa2 * 0.075
        ir += ir_f2
    else:
        ir_f2 = 0

    # Faixa 15%
    if base_ir > 2826.65:
        faixa3 = min(base_ir, 3751.05) - 2826.65
        ir_f3 = faixa3 * 0.15
        ir += ir_f3
    else:
        ir_f3 = 0

    # Faixa 22.5%
    if base_ir > 3751.05:
        faixa4 = min(base_ir, 4664.68) - 3751.05
        ir_f4 = faixa4 * 0.225
        ir += ir_f4
    else:
        ir_f4 = 0

    # Faixa 27.5%
    if base_ir > 4664.68:
        faixa5 = base_ir - 4664.68
        ir_f5 = faixa5 * 0.275
        ir += ir_f5
    else:
        ir_f5 = 0

    return ir, ir_f1, ir_f2, ir_f3, ir_f4, ir_f5


def calcular_ir_mensal():
    salario = float(input("Salário bruto: "))
    dependentes = int(input("Número de dependentes: "))
    pensao = float(input("Pensão alimentícia: "))
    idoso = input("Tem 65 anos ou mais? (sim/nao): ").lower()

    # INSS
    inss, f1, f2, f3, f4 = calcular_inss(salario)

    # Deduções
    ded_dep = dependentes * 189.59
    ded_idoso = 1903.98 if idoso == "sim" else 0

    # Base IR
    base_ir = salario - inss - ded_dep - pensao - ded_idoso

    # IR
    ir, ir_f1, ir_f2, ir_f3, ir_f4, ir_f5 = calcular_ir(base_ir)

    # Salário líquido
    liquido = salario - inss - ir

    # Saída
    print("\n====================================")
    print("CONTRACHEQUE — Cálculo de IR Mensal")
    print("====================================")

    print(f"Salário bruto:       R$ {salario:,.2f}")

    print(f"\n(-) INSS:            R$ {inss:,.2f}")
    print(f"    Faixa 7.5%:      R$ {f1:,.2f}")
    print(f"    Faixa 9%:        R$ {f2:,.2f}")
    print(f"    Faixa 12%:       R$ {f3:,.2f}")
    print(f"    Faixa 14%:       R$ {f4:,.2f}")

    print(f"\n(-) Dependentes ({dependentes}): R$ {ded_dep:,.2f}")
    print(f"(-) Pensão:          R$ {pensao:,.2f}")
    print(f"(-) Isenção 65+:     R$ {ded_idoso:,.2f}")

    print(f"\nBase de cálculo IR:  R$ {base_ir:,.2f}")

    print(f"\n(-) IR:              R$ {ir:,.2f}")
    print(f"    Faixa isenta:    R$ {ir_f1:,.2f}")
    print(f"    Faixa 7.5%:      R$ {ir_f2:,.2f}")
    print(f"    Faixa 15%:       R$ {ir_f3:,.2f}")
    print(f"    Faixa 22.5%:     R$ {ir_f4:,.2f}")
    print(f"    Faixa 27.5%:     R$ {ir_f5:,.2f}")

    print("====================================")
    print(f"Salário líquido:     R$ {liquido:,.2f}")
    print("====================================")


# Executar
calcular_ir_mensal()
