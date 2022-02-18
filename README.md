# introduccion_algoritmica

La dirección de este repositorio es: [ github](https://github.com/GonzaloGmv/introduccion_algoritmica/edit/main/README.md)

## Ejercicio 8.1
**Algoritmo porcentajes_iva**
   * Calcular el precio con los impuestos incluidos

**entrada**
   * precio sin impuestos: REAL  # precio en bruto
   
**Resultado: REAL variable****
   * precio con impuestos: REAL  # precio neto
   
**Constante**
   * porcentaje de IVA: REAL  # porcentaje de IVA escrito de forma decimal, vale 0,21
 
**realizacion**
```
precio con impuestos = precio sin impuestos * porcentaje de IVA
precio con impuestos = precio con impuestos + precio sin impuestos
```
poscondicion

...

fin porcentajes_iva

## Ejercicio 8.2
**Algoritmo inversiones**
   * Calcular el importe de los intereses
   
**entrada**
   * capital invertido: REAL  # dinero que se invierte 
   * tiempo: ENTERO  # tiempo en meses

**variable**
   * capital con intereses: REAL  # capital al que se le han añadido los intereses
   * tasa de interes: REAL  # cantidad que se abona segun el tiempo por capital invertido. Esta tasa viene dada, pero luego operaremos con ella

**realizacion**
```
 tasa de interes = tasa de interes dado + 1
 tasa de interes = tasa de interes ^ tiempo
 capital con intereses = tasa de interes
```
poscondicion

...

fin inversiones

## Ejercicio 9.1
**Algoritmo media_aritmetica_ponderada**
   * Calcular la media aritmetica de tres numeros dados

**entrada**
   * numero1: REAL  # uno de los tres numeros dados
   * numero2: REAL  # uno de los tres numeros dados
   * numero3: REAL  # uno de los tres numeros dados
   
**variable**
   * suma: REAL  # una varible para almacenar la suma
   * media: REAL  # una variable para almacenar el resultado
   
**realizacion**
```
suma = numero1 + numero2
suma = suma + numero3
media = suma/3
```

poscondicion

...

fin media_aritmetica_ponderada

## Ejercicio 9.2
**Algoritmo media_aritmetica_ponderada**
   * Dados los números y sus coeficientes de ponderación

**entrada**
   * numero_m: REAL  # uno de los numeros
   * coeficiente_m: REAL  # coeficiente de ponderacion del numero
   * numero_n: REAL  # uno de los numeros
   * coeficiente_n: REAL  # coeficiente de ponderacion del numero
   * numero_l: REAL  # uno de los numeros
   * coeficiente_l: REAL  # coeficiente de ponderacion del numero
  
**variable**
   * numero_m ponderado: REAL  # numero m, habiendo actuado su coeficiente
   * numero_n ponderado: REAL  # numero n, habiendo actuado su coeficiente
   * numero_l ponderado: REAL  # numero l, habiendo actuado su coeficiente
   * numero_m+n ponderado: REAL  # suma de los numeros ponderados
   * n: ENTERO  # cantidad de numeros que hay
   * media total: REAL  # media ponderada global

**realizacion**
```
si n = 0 
  entonces media total = 0
si n = 1
  entonces media total = 1
si n = 2
  entonces
    numero_m ponderado = numero_m * coeficiente_m
    numero_n ponderado = numero_n * coeficiente_n
    media total = numero_m ponderado + numero_n ponderado
si n > 2
  entonces
    numero_m ponderado = numero_m * coeficiente_m
    numero_n ponderado = numero_n * coeficiente_n
    numero_m+n ponderado = numero_m ponderado + numero_n ponderado
    numero_l ponderado = numero_l * coeficiente_l
    media total = numero_m+n ponderado + numero_l ponderado
```

poscondicion

...

fin media_aritmetica_ponderada

## Ejercicio 10.1

**Algoritmo area_triangulo**
   * Calcular el area de un triangulo dado un lado y la altura asociada a el

**entrada**
   * lado: REAL  # medida de un lado
   * altura: REAL  # altura asociada al lado
  
**variable**
   * operacion: REAL  # variable en la que se guardara el resultadoo de una operacion
   * area: REAL  # area del triangulo

**realizacion**
```
operacion = lado * altura
area = operacion / 2
```
poscondicion

...

fin area_triangulo

## Ejercicio 10.2

**Algoritmo area_triangulo**
   * Calcular el area de un triangulo rectangulo dados los lados perpendiculares

**entrada**
   * lado1: REAL  # medida de un lado
   * lado2: REAL  # medida del otro lado
  
**variable**
   * operacion: REAL  # variable en la que se guardara el resultadoo de una operacion
   * area: REAL  # area del triangulo

**realizacion**
```
operacion = lado1 * lado2
area = operacion / 2
```
poscondicion

...

fin area_triangulo

## Ejercicio 11

**Algoritmo horas_extra**
   * Establece la remuneración de 'horas_ext' adicionales para
   * un salario mensual bruto de 'salario_mensual_bruto'
    
**entrada**
   * salario_mensual_bruto : REAL  # Importe del salario mensual bruto
   * horas_ext : ENTERO  # Cantidad de horas extra del mes a pagar

**precondición**
   * salario_mensual_bruto > 0
   * horas_ext ≥ 0

**constante**
   * cantidad_semanas : ENTERO ← 52  # Cantidad de semanas de trabajo 
   * cantidad_horas_semana : ENTERO ← 35  # Cantidad legal de horas de trabajo semanales 
   * cantidad_horas_max : ENTERO ← 8  # Umbral de cambio de precio de remuneración
   * precio_1 : REAL ← 1,25  # Tarifa de remuneración de CANTIDAD_HORAS_MAX_1 primeras horas extra
   * precio_2 : REAL ← 1,50  # Tarifa de remuneración de las otras horas extra

**variable**
   * horas_ext_1 : ENTERO  # Cantidad de horas extra con PRECIO_1 %
   * horas_ext_2 : ENTERO  # Cantidad de horas extra con PRECIO_2 %
   * precio_hora : REAL  # Precio hora de la remuneración bruta básica

**realizacion**
```
# calcular el precio_hora de la remuneración bruta básica
    Resultado ← precio_hora x (inf(horas_ext, cantidad_horas_max_1) x precio_1 + sup(horas_ext – cantidad_horas_max_1, 0) x precio_2)
    
# Cálculo del precio_hora de la remuneración bruta básica
precio_hora ← salario_mensual_bruto x 12 / (REAL(CANTIDAD_HORAS_SEMANA) x REAL(CANTIDAD_SEMANAS))

```
postcondición

...

fin horas_extra

## Ejercicio 12

1.

tipo CUENTA estructura
   * saldo : REAL
   * descubierto : REAL
   * invariante
      * El descubierto no está autorizaddo  descubierto = 0
      * el saldo debe ser superior al descubierto autorizado   saldo ≥ descubierto
fin CUENTA

2.
#### **- Algoritmo abrir una cuenta**
abrir(c : CUENTA ; saldo_inicial : REAL)
   * Inicializar 'c' mediante un 'saldo_inicial'.

**Precondición**
   * saldo_inicial > 0

**realización**
```
 c.descubierto ← 0
 c.saldo ← saldo_inicial
```

**postcondición** 
```
c.descubierto = 0
     # El descubierto no está autorizado
antiguo(saldo_inicial) = saldo_inicial
c.saldo = saldo_inicial

fin abrir
```

#### **- Algoritmo abonar una cuenta**

abonar(c : CUENTA ; crédito : REAL)
   * Crédito 'c' de la suma `crédito'.

**Precondición**
   * c.saldo ≠ NULO
   * crédito ≠ NULO

**realización**
```
c.saldo ← c.saldo + crédito
```

postcondición
```
# El descubierto autorizado y el importe del crédito' no se modifican
antiguo(c).descubierto = descubierto
antiguo(c).crédito = crédito

# El saldo aumenta con el 'crédito'
c.saldo = antiguo(c).saldo + crédito

fin abonar
```

#### **- Algoritmo cargar una cuenta**

cargar(c : CUENTA ; débito : REAL)
   * Carga 'c' con la suma 'débito'.

**Precondición**
   * c.saldo ≠ NULO
   * débito ≠ NULO
   * c.saldo + c.descubierto ≥ débito ≥ 0

**realización**
```
 abonar(c, –débito)
```

**postcondición**
```
# El descubierto autorizado y el importe del 'débito' no se modifican
antiguo(c).descubierto = descubierto
antiguo(débito) = débito

# Al saldo se le resta el `débito'
c.saldo = antiguo(c).saldo – débito

fin cargar
```

#### **- Algoritmo consultar una cuenta**

consultar(c : CUENTA) : REAL
   * El 'saldo' de la cuenta 'c'.

**precondición**
   * c.saldo ≠ NULO

**realización**
```
Resultado ← c.saldo
```

**postcondición**
```
Resultado = c.saldo

fin consultar
```

#### **- Algoritmo es acreedora**

es_acreedora(c : CUENTA) : BOOLEANO
   * ¿'c' es acreedora?

**precondición**
   * c.saldo ≠ NULO

**Realización**
```
Resultado ← (c.saldo > 0)
```
**postcondición**
```
Resultado = (c.saldo > 0)

fin es_acreedora
```

#### **- Algoritmo es deudora**

es_deudora (c : CUENTA) : BOOLEANO
   * ¿`c' es deudora?

**precondición**
   * c.saldo ≠ NULO

**Realización**
```
Resultado ← (– c.descubierto ≤ c.saldo ≤ 0)
```

**postcondición**
```
Resultado = (– c.descubierto ≤ c.saldo ≤ 0)

fin es_deudora
```

3.

#### **- Algoritmo abrir una cuenta con descubierto autorizado**

abrir(c : CUENTA ; saldo_inicial : REAL ; descubierto_MAX : REAL)
   * Inicializar 'c' mediante un `saldo_inicial' y un 
   * 'descubierto_MAX'.

**Precondición**
   * saldo_inicial > 0
   * descubierto_MAX ≥ 0

**realización**
```
c.descubierto ← descubierto_MAX
c.saldo ← saldo_inicial
```

**postcondición**
```
c.descubierto = descubierto_MAX
c.saldo = saldo_inicial

fin abrir
```

Las demás operaciones seguirían igual
