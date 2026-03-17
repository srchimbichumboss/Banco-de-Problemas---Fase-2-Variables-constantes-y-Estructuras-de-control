# Banco-de-Problemas---Fase-2-Variables-constantes-y-Estructuras-de-control
Problemas del 1 al 5
# aplicamos los consumos.
consumos = [100, 200, 300, 400, 150]
Costo_KWH = 320.5

#Se clasifican los consumos por categoria y porcentaje.
for consumo in consumos: 
     if consumo < 150:
          categoria = "Consumo bajo"
          porcentaje = 0.05
          ajuste = "Descuento"

     elif consumo <= 350:
          categoria = "Consumo medio"
          porcentaje = 0.0
          ajuste = "sin ajuste"

     else:
          categoria = "Consumo alto"
          porcentaje = 0.12
          ajuste= "recargo"
          
     #valor de la base:
     valor_base = consumo * Costo_KWH

     #Uso del ajuste:
     monto_ajuste = valor_base * porcentaje

     if ajuste == "Descuento":
         valor_final = valor_base - monto_ajuste
     else:
      valor_final = valor_base + monto_ajuste
     #Salida:
     print("consumo:", consumo,"KWH")
     print("categoria:", categoria)
     print("valor base: $", round(valor_base, 2))
     print(f"{ajuste} aplicando", porcentaje * 100, "%")
     print("valor final a pagar:$" , round(valor_final, 2))
     print("-"* 40)
     
