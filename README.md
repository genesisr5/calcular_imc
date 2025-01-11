def calcular_imc(peso, altura):
  """
  Calcula el Índice de Masa Corporal (IMC) a partir del peso en kilogramos y la altura en metros.

  Args:
    peso (float): Peso en kilogramos.
    altura (float): Altura en metros.

  Returns:
    float: Índice de Masa Corporal calculado.
  """

  imc = peso / (altura ** 2)
  return imc

# Rangos de peso y altura
pesos = [50, 60, 70, 80, 90, 100, 110, 120]
alturas = [1.55, 1.60, 1.65, 1.70]

# Iterar sobre todas las combinaciones de peso y altura
for peso in pesos:
  for altura in alturas:
    imc = calcular_imc(peso, altura)
    print(f"Para un peso de {peso} kg y una altura de {altura} m, el IMC es: {imc:.2f}")

    # Clasificación básica del IMC (puedes personalizar)
    if imc < 18.5:
      print("Bajo peso")
    elif 18.5 <= imc < 25:
      print("Peso normal")
    elif 25 <= imc < 30:
      print("Sobrepeso")
    else:
      print("Obesidad")
