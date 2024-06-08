# GS-PYTHON
Rodrigo Mori RM:555384  
Gabriel Barros RM:555410

No prototipo a nossa intenção foi recompernasr as pessoas que reciclam os lixos nas praias, recompesando elas com algum tipo de premio
codigo do Python:

residuos = {
    "garrafa": "Reciclável",
    "saco_plastico": "Reciclável",
    "canudo": "Não Reciclável",
    "embalagem": "Reciclável"
}


residuos_encontrados = []

num_residuos = int(input("Quantos tipos de resíduos você encontrou? "))

count = 0
while count < num_residuos:
    residuo = input("Insira o tipo de resíduo: ").lower()
    residuos_encontrados.append(residuo)
    count += 1

classificacao_residuos = []

for residuo in residuos_encontrados:
    if residuo in residuos:
        classificacao = residuos[residuo]
    elif residuo == "papel":
        classificacao = "Reciclável"
    else:
        classificacao = "Desconhecido"
   
    classificacao_residuos.append((residuo, classificacao))

print("\nResumo dos resíduos classificados:")
for residuo, classificacao in classificacao_residuos:
    print(f"Resíduo: {residuo.capitalize()}, Classificação: {classificacao}")
