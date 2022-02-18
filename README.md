# introduccion_algoritmica

## Ejercicio 8.1
**Algoritmo porcentajes, iva**
   * Calcular el precio con los impuestos incluidos

**entrada**
   * precio sin impuestos: REAL # precio en bruto
   
**Resultado: REAL variable****
   * precio con impuestos: REAL # precio neto
   
**Constante**
   * porcentaje de IVA: REAL #porcentaje de IVA escrito de forma decimal, vale 0,21
 
**realizacion**
```
precio con impuestos = precio sin impuestos * porcentaje de IVA
precio con impuestos = precio con impuestos + precio sin impuestos
```

## Ejercicio 8.2
**Algoritmo inversiones**
   * Calcular el importe de los intereses
   
**entrada**
   * capital invertido: REAL #dinero que se invierte 
   * tiempo: ENTERO #tiempo en meses

**variable**
   * capital con intereses: REAL #capital al que se le han añadido los intereses
   * tasa de interes: REAL #cantidad que se abona segun el tiempo por capital invertido. Esta tasa viene dada, pero luego operaremos con ella

**realizacion**
```
 tasa de interes = tasa de interes dado + 1
 tasa de interes = tasa de interes ^ tiempo
 capital con intereses = tasa de interes
```

## Ejercicio 9.1
**Algoritmo media aritmetica ponderada**
