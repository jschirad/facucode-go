# Variables y Tipos de Datos

Ahora que ya tenemos nuestro espacio de trabajo listo, empecemos a utilizar nuestro lenguaje.

Vamos a empezar por las variables y tipos de datos. Como muchos otros lenguajes, Golang contiene: booleans, intergers, floats y strings. 

Antes de revisar los diferentes tipos de datos, veamos algunas diferencias entre golang y otros lenguajes. 


### The Zero Value

Golang, como muchos de otros lenguajes modernos, asignara el valor zero por defecto a todas las variables que estén declaradas, pero que no sean utilizadas. Esto nos evitará problemas a la hora de compilar nuestro código. 

Como hablamos de los diferentes tipo de variables, a medida que vayamos detallando cada tipo, iremos cubriendo el _**zero value**_ correspondiente.

### Booleans

Este tipo de dato representa una variable de tipo _**bool**_. Esta podra tener dos valores: _**true**_ o _**false**_. El valor _**zero**_ para un booleano es _**false**_.

```
var flag bool // no asignamos ningun valor, false por defecto
var isAwesome = true
```

### Tipos de Variables Numéricas

Golang tiene 12 tipos de variables numéricas que están agrupadas en 3 categorías. 

- Interger Type
- Float Type
- Complex Type

#### Interger

|Tipo/Nombre | Rango de Valor|
|------------|---------------|
|int8        |-128 to 127    |
|int16       |–32768 to 32767|
|int32       |–2147483648 to 2147483647|
|int64       |–9223372036854775808 to 9223372036854775807|
|unit8       |0 to 255|
|unit16      |0 to 65536|
|unit32      |0 to 4294967295|
|unit64      |0 to 18446744073709551615|

Puede ser obvio, pero el valor _**zero**_ por defecto es 0.

#### Interger Especiales

1. Go tiene algunos nombres especiales para sus variables de tipo interger. Un _**byte**_ es un alias para _**unit8**_. Esto quiere decir que podremos operar, comparar o asignar operaciones entre este tipo de variables. 

2. Otro nombre especial es _**int**_. En un PC con 32-bit CPU, un _**int**_ es equivalente a _**int32**_. En el caso de 64-bit CPU, _**int**_ es equivalente a _**int64**_. En este caso no será conveniente hacer comparaciones u opreaciones entre _**int**_ y _**int32**_ o _**int64**_ debido a que si nuestro codigo es alamacenado en otra plataforma, puede fallar al compilar. 

3. El tercer nombre especial que tendremos es _**unit**_ y sigue las mismas reglas de _**int**_. 

4. En cuarto lugar, tendremos dos tipos de nombres extras que son _**rune**_ y _**uintptr**_, si quieres saber más sobre ellos, te reto a seguir investigando y compartirlo por nuestro canal de slack. 

#### ¿Como escoger el tipo de Interger para mi programa?

Para poder elegir correctamente el tipo de variable que necesitamos, deberás seguir estas 3 reglas:

1. Si estás trabajando con ficheros binarios o protocolos de red que tienen variables específicas recomendadas, usa las variables correspondientes.

2. Si estás escribiendo una librería o funciones que puedan trabajar con cualquier tipo de interger, lo recomendado es que escribas un par de funciones, una de ellas que use _**int64**_ y la otra que utilice _**unit64**_.

3. Para todos los otros casos, simplemente usa _**int**_.

#### Float Type

Existen dos tipos de _**float**_ en Go:

|Nombre|Valor Absoluto|
|------|--------------|
|float32|3.40282346638528859811704183484516925440e+38|
|float64|1.797693134862315708145274237317043567981e+308|

Como los interger, el valor _**zero**_ para las variables de tipo _**float**_ es 0.

Como en muchos otros lenguajes, las variables de tipo _**float**_ son utilizadas para operaciones más complejas y que requieren mayor precisión. 

#### Complex Type 

Las variables complejas en Go son un tipo de dato que se utiliza para representar números complejos. Un número complejo está compuesto, por una parte real y una parte imaginaria, donde la parte imaginaria se representa mediante la letra "i".

En Go, las variables complejas se definen utilizando la función complex(), que toma dos argumentos: la parte real y la parte imaginaria del número complejo. Por ejemplo, la variable compleja z = complex(3, 4) representa el número complejo 3 + 4i.

Las variables complejas en Go se utilizan principalmente en cálculos matemáticos que involucran funciones como la transformada de Fourier y la teoría de funciones analíticas. También se utilizan en gráficos y visualizaciones, donde se pueden representar números complejos como puntos en un plano complejo.
