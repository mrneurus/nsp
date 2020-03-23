# No seas pelotudo

Alguna vez como tanta veces, 
conoci personas que decian las matematicas no sirven para nada, probablemente alguno de ellos o le esta tirando piedras a la policia , o esta tomando mate en monte hermoso o esta llamando a la insurreccion contra la cuarentena , porque Bakunin o Trotsky asi lo hubiesen querido.

## Entonces de que va esto ?
---

Mira las Matematicas del secundario, ese que odiabas , te puede ayudar o demostrar que la cosa se puede poner picante en tu país que exporta materia prima, que hace años esta estancado en la falsa dicotomia de Peronismo SI , Peronismo NO, que Marx, que los '70,y blaaa y blaaa, y que al momento de una crisis determinante todo lo que hasta el momento era de una forma se puede ir al tacho, basicamente por tu estupidez una vez mas.


### Vamos a hacer una simple tabla de valores

 Curva de contagio en Argentina al dia 21 de Marzo del 2020.

| DIA           | Casos Confirmados|
| ------------- |:-------------:|
| DIA 1 : 3 DE MARZO         |      1 |
| DIA 2 : 4 DE MARZO        |      1 |
| DIA 3 : 5 DE MARZO        |      1 |
| DIA 4 : 6 DE MARZO        |      2 |
| DIA 5  : 7 DE MARZO       |       6|
| DIA 6   : 8 DE MARZO      |       8|
| DIA 7   : 9 DE MARZO      |       11|
| DIA 8   : 10 DE MARZO      |       19|
| DIA 9   : 11 DE MARZO     |       21|
| DIA 10  : 12 DE MARZO       |      31 |
| DIA 11   :13 DE MARZO      |       34|
| DIA 12  : 14 DE MARZO       |       45|
| DIA 13  : 15 DE MARZO       |       56|
| DIA 14   : 16 DE MARZO      |       65|
| DIA 15  : 17 DE MARZO       |       79|
| DIA 16   : 18 DE MARZO      |       97|
| DIA 17    : 19 DE MARZO     |       128|
| DIA 18    : 20 DE MARZO     |       159|
| DIA 19    : 21 DE MARZO     |       225|



Ahora pensemos esto , que cantidad de infectados confirmados existen entre el dia de hoy y ayer, es decir los nuevos infectados de un dia respecto al dia anterior.
Si miramos la tabla vemos que lo que tengo hoy es mayor a lo de ayer , es decir :
 
 ```
 NUEVOS INFECTADOS = CANT_DIA_EN_EL QUE ESTOY - CANT_DIA_ATERIOR.

 ```
 Si quiero ver los nuevos infectados al día de hoy simplemente hago lo siguiente : 


 
 ```
 NUEVOS INFECTADOS AL 21DEMARZO = 225 - 159
    NUEVOS INFECTADOS AL 21DEMARZO = 66

 ```

 Vamos a llamar a los NUEVOS_INFECTADOS detectados por dia **VARIACION_DE_INFECTADOS**

 ## OK, Entonces de que depende la variacion de infectados ??

Imaginate este escenario , una persona en su casa una tarde decide cubrir todo su cuerpo con pintura,( *despreciemos el tiempo de secado de la misma* ), esa noche  se manda al barsucho de birras mas piola y concurrido de Palermo Soho, que crees que puede pasar??

Dos posibilidades:

Si esa noche el Beer explota, porque  en vez de ir al Álamo todos fueron al Barsucho, es mas que probable que nuestro amigo pintado deje sus marcas en principio en la barra, en el vaso y en muchas de las personas que estuvieron en contacto con él o se cruzaron con él a una distaancia muy cercana, en las personas que lo saludaron,etc, etc.

Pero si esa noche se hubiese quedado en la casa ?? y si al Barsucho no concurria nadie?? o estaba cerrado??  Que crees que pasaria??
Muy bien Watson, probablemente no hubiese manchado a NADIE.

> Esta fábula, esta inspirada en ficciones como : *Me voy de vaciones a Pinamar en medio de la Cuarentena*, y *Me escapo del hospital y me tomo un Buquebus con 400 personas*. 

¿Entonces? Lo que podemos ver es que la cantidad de NUEVOS_INFECTADOS, depende de la **EXPOSICION**.
Tambien depende de las conductas de riesgo que tenga uno, por ejemplo la higiene, no lavarse las manos, toser o estornudar sin taparse con debida precaucion, etc... o tener 40° de Fiebre y salir a comprar cigarrillos.
A esto lo vamos a llamar  *FACTOR_RIESGO*

Una cosa mas, si en vez de una persona pintada esa noche hubieran existido tres personas?Si la cantidad de personas pintadas hubiese sido mayor a uno , muy seguramente muchas personas mas esa noche se habrian ido con alguna marca de pintura .
Entonces, quiere decir que a mayor INFECTADOS, mayor probabilidad de contagio ??? SI, EXACTO WATSON!!!

> Segun la OMS, la probabilidad de contagio de una persona con COVID-19 es de 2,5 personas,es decir una persona infectada pude infectar al menos a 2 personas en promedio.

Si llegaste hasta aca , resulta que todo esto lo podemos poner en una formula:

```
VARIACION_DE_INFECTADOS= EXPOSICION * FACTOR_RIESGO*CANT_TOTAL_DE_INFECTADOS

```
Imaginate otro escenario, donde todos estemos en la calle y quietos, y tenemos tres personas infectadas, las mismas al menos van a contagiar a dos mas Tendriamos algo asi:
     
     P1-INFECTADA
        P1-CONTAGIO 1-2
        P1-CONATGIO 2-2
     P2-INFECTADA
        P2-CONTAGIO 1-2
        P2-CONTAGIO 2-2
     P3-INFECTADA
        P1-CONTAGIO 1-2
        P1-CONTAGIO 2 -2     

Con tres personas infectadas y ESTANDO TODOS QUIETOS, ahora tenemos 6 infectados nuevos, es decir en total 9 INFECTADOS.
Ahora pensa que esos 6 nuevos infectados contagian a sus correspondientes dos personas a contagiar:
     
     P1-INFECTADA
        P1-CONTAGIO 1
            P1C-CONTAGIO-1
            P2C-CONTAGIO-2
        P1-CONATGIO 2
            P1C-CONTAGIO-1
            P1C-CONTAGIO-2
        P1-CONTAGIO SEGUNDO DIA-1
        P1-CONTAGIO SEGUNDO DIA -2   
     P2-INFECTADA
        P2-CONTAGIO 1
            P2C-CONTAGIO-1
            P2C-CONTAGIO-2
        P2-CONTAGIO 2
            P2C-CONTAGIO-1
            P2C-CONTAGIO-2
        P2-CONTAGIO SEGUNDO DIA-1
        P2-CONTAGIO SEGUNDO DIA -2    
     P3-INFECTADA
        P1-CONTAGIO 1
            P3C-CONTAGIO-1
            P3C-CONTAGIO-1
        P1-CONTAGIO 2
            P3C-CONTAGIO-1
            P3C-CONTAGIO-2   
        P3-CONTAGIO SEGUNDO DIA-1
        P3-CONTAGIO SEGUNDO DIA -2
Cuanto tenemos ahora ??  **27 casos en total** , de 3 casos de infectados en la segunda ronda pasamos a 27 casos,  y eso considerando que las personas estan quietas y no entrando, saliendo , yendo a Monte Hermoso o Pinamar.

Habiamos dicho que VARIACION_DE_INFECTADOS = a los infectados en un dia - los infectados el dia anterior.Es decir si yo quiero saber los infectados nuevos que existen entre el dia 7  y el dia 8 deberia hacer esto :

```
    VARIACION DEL DIA 7 = INFECTADOS_DIA_8 - INFECTADOS_DIA_7 
```
Con esto estamos diciendo que la variacion de cualquier dia a saber depende del día en  que estoy menos el  día anterior, eso ahora lo vamos a expresar asi

$$VARIACION.DE.INFECTADOS= I_{n+1} - I_{n}$$


Entonces nuestra formula seria algo asi :
 
$$I_{n+1}-I_{n} = EXPOSICION * FACTORRIESGO* CANT.TOT.DE.INFECTADOS$$

Matematicamente mas estetico : 

$$I_{n+1} - I_{n} = E*FR*I_{N}$$

Ahora hagamos que la formula nos hable sobre cualquier dia que querramos saber para eso tenemos que depejar de la formula :

$$I_{n+1}$$

nos quedaria algo asi : 

$$I_{n+1} - I_{n} = E*FR*I_{N}$$
$$I_{n+1} = E*FR*I_{N} +  I_{n}$$

Si hacemos unos trucos mas como agrupar y factor comun llegamos a una regla mas general: 

$$I_{n+1} = E*FR *I_{N} +  I_{n}$$
$$I_{n+1} =  I_{n}(E*FR + 1 )$$

Mira a lo que llegamos , una regla que nos dice que si queremos saber en un dia cualquiera la cantidad de infectados , esa cantidad va a depender de los infectados que tengamos al momento multiplicado por el factor Exposicion y Factores de riesgo.

$$I_{n+1} =  I_{n}(E*FR + 1 )$$

Aca en este parentesis esta la verdad de la milonga : 

$$(E*FR + 1 )$$

Si ese parentesis nos diera 0 mira lo que pasa cuando le preguntamos que cantidad de Infectados vamos a tener en argentina el dia 23 de Marzo : 

$$I_{n+1} =  I_{n}(E*FR + 1 )$$
$$I_{23 de Marzo } = 266 *(0)$$
$$I_{23 de Marzo } = 0$$

> Si esa constante llegara a valer 0 , MAÑANA no tendriamos personas contagiadas.


Lamentablemente esa constante no vale 0, sabes por que ?? la respuesta te sorprendera!!! 


## ¿ Cuanto vale esa contante entonces al dia de hoy ?

Simple, hagamos la formula , a esa contasnte la vamos a llamar constante de riesgo  o simplemente CR y nos queda algo asi: 

$$CR = (EFR + 1 )$$

Entonces mira , lo podemos averiguar remplazando RC en la regla general : 

$$I_{n+1} =  I_{n}*CR$$

Y si ahora teniendo los datos de infectados de  Hoy y los datos de infectados de ayer tal vez podemos sacar cuanto vale nuesta CR : 

$$I_{n+1} =  I_{n}*CR$$ 
$$266 = 225 * CR$$
$$CR =  {266\over225}$$

$$CR =  1.18$$

>Hoy nuestra constante de riesgo es de **1.18**

Mira si le pregunto cuantos vamos a tener el de 23 de Marzo en condiciones exactamente iguales a las de ayer, y hoy : 

```Math
$$
I_{23 de Marzo} =  266*1,18
$$
$$I_{23 de Marzo} = 314$$
```
Mira si hago una tabla asi hasta el  3 de abril con un factor de **1,18**



| DIA           | Casos Confirmados|
| ------------- |:-------------:|
| DIA 1 : 3 DE MARZO         |      1 |
| DIA 2 : 4 DE MARZO        |      1 |
| DIA 3 : 5 DE MARZO        |      1 |
| DIA 4 : 6 DE MARZO        |      2 |
| DIA 5  : 7 DE MARZO       |       6|
| DIA 6   : 8 DE MARZO      |       8|
| DIA 7   : 9 DE MARZO      |       11|
| DIA 8   : 10 DE MARZO      |       19|
| DIA 9   : 11 DE MARZO     |       21|
| DIA 10  : 12 DE MARZO       |      31 |
| DIA 11   :13 DE MARZO      |       34|
| DIA 12  : 14 DE MARZO       |       45|
| DIA 13  : 15 DE MARZO       |       56|
| DIA 14   : 16 DE MARZO      |       65|
| DIA 15  : 17 DE MARZO       |       79|
| DIA 16   : 18 DE MARZO      |       97|
| DIA 17    : 19 DE MARZO     |       128|
| DIA 18    : 20 DE MARZO     |       159|
| DIA 19    : 21 DE MARZO     |       225|
| DIA 20    : 22 DE MARZO     |       266|
| DIA 21    : 23 DE MARZO     |       314|
| DIA 22     :24 DE MARZO    |       370|
| DIA 23    : 25 DE MARZO     |       436|
| DIA 24    : 26 DE MARZO     |       514|
| DIA 25    : 27 DE MARZO     |       607|
| DIA 26    : 28 DE MARZO     |       716|
| DIA 27    : 29 DE MARZO     |       844|
| DIA 28    : 30 DE MARZO     |       995|
| DIA 29     : 31 DE MARZO    |       1174|
| DIA 30     : 1 DE ABRIL    |       1385|
| DIA 31    : 2 DE ABRIL     |       1635|
| DIA 32    : 3 DE ABRIL     |       1929|

> Segun este modelo, simplemente con los datos que existen al momento no teniendo en cuenta las restricciones totales tendriamos solo en 32 dias , 1930 casos aproximados.

A este modelo le falta tener en cuenta varias cosas como la cantidad de test que se hacen por dia.
Pero lo importante del modelo en si es que tenemos una constante que cuanto mas cerca del 0 este,  mas posibilidad de controlar la pandemia vamos a estar. 
Y volvemos con el bambi, sabes de que depende de que te NO TE EXPONGAS , si vos,
amigo Bolche, vos transgresor/ar, vos hippie/ia, vos perro/a,vos rocha , vos loro,  vos cheto/a de Devoto, vos , si vos NO SEAS COMO VENIS SIENDO HACE TANTO TIEMPO.... A VECES ES BUENO CAMBIAR !!!!!!

