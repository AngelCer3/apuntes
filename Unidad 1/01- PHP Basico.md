1. Hola mundo
2. Para poder crear un documento en php primero es necesario inicializar los servicios de *apache* que nos da la instalación de *xampp* 
3. ![[Pasted image 20230824072657.png]]
4. Ahora bien vamos a crear una carpeta en htdocs ubicado en el disco local y hay crear una carpeta llamada *php-basico*
5. ![[Pasted image 20230824072828.png]]
6. En este caso vamos a abrir la carpeta con el editor de código en este caso **Visual Studio Code** y una vez hay creamos un documento en llamado *index.php*
7. ![[Pasted image 20230824073057.png]]
8. Ahora vamos a utilizar los tags respectivos de php los cuales son *(<?php ?>)* y en ello llamar la función print y echo para mostrar un hola mundo de distintas formas.
9. ![[Pasted image 20230824073505.png]]
## Variables
Para crear variables en *php* se tienen que declarar al inicio con el signo de *($)* y aparte si ocupamos la linea de código *var_dump()* para saber el tipo de dato y ademas php toma los datos por *inferencia* 
![[Pasted image 20230824074355.png]]
![[Pasted image 20230824074407.png]]
## Reglas de escritura en php
1. Usar únicamente *caracteres latinos (0-9,a-z,A-Z) y guion bajo*.
3. No utilizar *caracteres especiales*.
4. Si se puede utilizar *guion bajo al comienzo* del nombre de una variable
5. Nombrar las variables con *significado semántico*.
6. Tener en cuenta que *se distinguen entre nombres con mayúsculas y minúsculas*, **Ejemplo. apellidoMaterno** no es igual que  **apellidomaterno**
7. Evitar *palabras reservadas*.

### Constantes
Para definir una constante se hace con la funcion de *define()* y esta debe llevar de primera instancia un *nombre* y al siguiente lado va su *valor*. **Estas constantes pueden ser de cualquier tipo de dato.**
Para imprimir una concatenacion es la parte de la cadena y aparte es con el caracter de *" ."*
![[Pasted image 20230824075557.png]]

### Operaciones aritméticas

Las operaciones aritméticas en PHP no soy distintas a cualquier otro lenguaje de programación y estas son las siguientes:
![[Pasted image 20230824080114.png]]

### Operaciones Lógicas
Las operaciones lógicas son las siguientes:

| Nombre | Símbolo  |
| ------ | -------- |
| And    | && o And |
| Or     | Or I     | 
| Not    | !        |

![[Pasted image 20230824082743.png]]


### Operadores de comparación
Los operadores de comparación son los siguientes:

| Ejemplo        | Nombre            |
| -------------- | ----------------- |
| $a == $b       | igual             |
| $a=== $b       | idéntico          |
| $a != $b       | Diferente         |
| $a !== $b      | No idéntico       |
| $a <> $b       | Diferente         |
| $a < $b        | Menor que         |
| $a  > $b       | Mayor que         |
| $a <= $b       | Menor o igual que |
| $a >= $b       | Mayor o igual que |
| $a <=> $b      | Nave espacial     |
| $a ?? $b ?? $c | Fusión de null    |

### If else
La sentencia if nos permite comparar dos o mas variables y si la condición se cumple va a ejecutar un bloque de código. Y bien ahora vamos a ver un ejemplo de código.
```
<?php
    $edad = 18;
    
    if ($edad >= 18 && $edad < 30){

        print ("Eres mayor de edad");

    }else if($edad >= 30 && $edad < 60){

        print ("Eres un adulto");

    }else if ($edad >= 60){

        print ("Eres un adulto mayor");

    }else{

        print ("Eres menor de edad");
    }
?>
```

### Switch
Es una estructura de control que nos ayuda a *evaluar* la opción con algún de los case se ejecutara lo que este dentro de la sentencia del case y si no encuentra algún caso que sea igual este mandara al *default* para decirnos que no huno un caso.
```
<?php
    $opcion = "HTML";
    switch($opcion){
        case 'HTML':
            print ("Lenguaje de Maquetado");
            break;
        case 'CSS':
            print ("Hojas de estilo");
            break;
        case 'JS':
            print ("Lenguaje de programacion cliente");
            break;
        default:
            print ("No conozco ese lenguaje");
            break;
    }
?>
```

### While
While es una estructura de control que permite crear un bucle y lo que este dentro de ese bucle se ejecute el código. Y algo importante del while es que *evalúa* primero y después *ejecuta* 
```
<?php
    while ($a <= 10){
        print ($a)
        $a++;
    }
?>
```
### Do While
Do while se ejecuta una primera vez el bloque de código que este escrito y de hay va a seguir haciendo una comparación que si se cumple la condición.
```
do{
	 $a = 0;
	 	
     print ($a);

     $a++;

    }while($a <= 10);
```
### Arreglos
Los arreglos son una colección de datos que pueden ser numéricos, booleanos, cadenas y poder combinarlos sin problema. Ejemplo de un arreglo
```<?php

    $calificaciones = [100,90,80,78,67,78];

    $arreglo = ["hola", 23, true];

    echo "<pre>";

    print_r($calificaciones);

    echo "</pre>" //permite preformatear los arreglos

?>
```
### Objetos
Los objetos en PHP únicamente existe cuando son instancias de clase. También conocidos como *Arreglos Asociativos*.

### Arreglos Asociativos
Están conformados por una clase o valor para acceder algún valor del arreglo asociativo tiene que ser por mediante sus *claves o llaves*.
```
<?php

    $persona = [

        "nombre" => "Angel",

        "edad" => 23,

        "direccion" => [

            "cuidad" => "CDMX",

            "Alcaldia" => "Tlahuac",

            "Pueblo" => "San Juan Ixtayopan"

        ],

         "calificaciones" => [12,23,45,65,78,99]

        ];

    echo "<pre>";

    print_r ($persona);

    print ($persona["direccion"]["Alcaldia"]);

    print ($persona["calificaciones"][3]);

    echo "</pre>";

?>
```

### For
Nos permite hacer bucles de y ejecuta el bloque de código que tiene adentro además de que nos ayuda a recorrer arreglos mas fácilmente. Además seguirá recorriendo hasta que la condición se deje de cumplir.
```
<?php

    $calificaciones = [100,90,80,78,67,78];

    $arreglo = ["hola", 23, true];

    for($i = 0; $i < count($calificaciones); $i++){

        print ($calificaciones[$i]);

        echo "<br>";
    }
    echo "<br>";

    for($i = 0; $i < count($arreglo); $i++){

        print ($arreglo[$i]);

        echo "<br>";
    }
?>
```

### Foreach
Es una estructura de bucle para lograr recorrer arreglos de manera un poco mas sintetizada.
```
<?php

     $calificaciones = [100,90,80,78,67,78];

  

     $arreglo = ["hola", 23, true];

  

     $persona = [

        "nombre" => "Angel",

        "edad" => 23,

        "direccion" => [

            "cuidad" => "CDMX",

            "Alcaldia" => "Tlahuac",

            "Pueblo" => "San Juan Ixtayopan"

        ],

         "calificaciones" => [12,23,45,65,78,99]

        ];

   /*  foreach( $calificaciones as $calificacion ){
        print($calificacion);
        echo "<br>";
    }
    echo "<br>";

    foreach($arreglo as $lista):

        print($lista);

        echo "<br>";

    endforeach; */
    echo "<br>";
    foreach ($persona as $llave => $valor){
	      if(is_array($valor)){ 
            foreach($valor as $llave2 => $valor2){
                print_r ("Llave: ". $llave2. " valor ". $valor2);
                echo "<br>";
            }
        }else{
            print_r ("Llave: ". $llave. " valor ". $valor);
            echo "<br>";
        }
    }
?>
```

### Funciones
Se declaran con la palabra reservada **function** y se a completa con el nombre de tu función y esta puede llevar **parámetros** de invocación o no. Y estas deben resolver únicamente una tarea.
```
<?php
    function saludar($nombre, $apellido){
        return "Hola " . $nombre . " " . $apellido;
    }
    print(saludar("Angel", "Cerezo"));

?>
```
### Clases
En una clase se pueden tener **atributos**, **funciones o métodos** y estas llevan un método constructor y lo que se hará referencia.
Aquí un ejemplo de como crear una instancia de clase.
```
<?php
    class Persona{
        public function __construct(public $nombre, public $apellido, public $edad){
        }

    }
    class Alumno{
        public $matricula;
        public $nombre;
        public $apellido;
        public $edad;

        public function __construct($matricula, $nombre, $apellido, $edad){
            $this -> matricula = $matricula;
            $this -> nombre = $nombre;
            $this -> apellido = $apellido;
            $this -> edad = $edad;
        }
    }
    $angel = new Persona("Angel", "Cerezo", 23);
    $alumno = new Alumno(201190059, "Angel", "Cerezo", 23);
    echo "<pre>";

    print_r($angel);

    echo "</pre>";

    echo "<br>";

    echo "<pre>";

    print_r($alumno);

    echo "</pre>";

?>
```
### Encapsulación
**Consiste en agrupar una líneas de código fuertemente relacionadas, darles un nombre y encapsularlas en un método o una clase**.
```
<?php

    class Producto{

        public function __construct(protected $nombre , protected $precio, protected $caducidad){}

        static public function obtenerProducto($nombre){

            if($nombre === $this-> nombre){

                return "Producto :" . $this->nombre . " Precio: " . $this->precio . " Caducidad: " . $this->caducidad;

            }else{

                return "El producto no existe";

            }

        }

    }

    $galletas = new Producto("Principe", 20, "29/09/2023");

    echo "<pre>";

    print_r($galletas -> obtenerProducto("Marias"));

    echo "<br>";
  
    print_r($galletas -> obtenerProducto("Principe"));

    echo "<br>";
  
    print_r(Producto::obtenerProducto()); //Los ":" significan accediendo a un metodo estatico
    
    echo "</pre>";

?>
```
### Funciones Estáticas
En el contexto de clases y objetos **la palabra reservada static permite definir métodos y propiedades estáticos** (lo que no tiene que ver con el concepto de variables estáticas).
```
<?php
    class Persona{
        public static $edad;

        protected static $nombre;

        protected static $apellido;

        public function __construct($nombre, $apellido , $edad) {

            self::$nombre = $nombre;

            self::$apellido = $apellido;

            self::$edad = $edad;

        }
  
        public static function obtenerPersona(){

            return "Nombre: " . self::$nombre . " Apellido " . self::$apellido. " Edad: " . self::$edad;

        }

    }

    $persona = new Persona("Angel", "Cerezo", 23);

    print_r($persona ->obtenerPersona()); //Con instancia de clase

    print($persona::obtenerPersona()); //Sin instancia de clase y se accede a un metodo estatico

?>
```
