# Fundamentos de JAVA
Fundamentos de JAVA del curso Universidad JAVA

# Manejo de Variables en JAVA

Tipos de datos en Java: 

- Tipos Primitivos
  - Tipos Enteros
  - Tipos Flotantes
- Tipos Referenciados (Tipo Object)
  - Clases 
  - Interfaces
  - Arreglos

## Tipos Primitivos 

- Tipos Enteros
  - byte ocupa (8 bits) **Default**: 0
  - Short (16 bits) **Default**: 0
  - char (16 bits) pero maneja el código Unicode **Default**: \u0000
  - int (32 bits) **Default**: 0
  - long (64 bits) **Default**: 0
  
- Tipos Flotantes
  - float (32 bits) **Default**: 0.0
  - double (64 bits) **Default**: 0.0

El tipo **boolean** también es un tipo primitivo y puede almacenar solo el valor de **true** o **false**. su valor por defecto es **false**.

___
# Manejo de Cadenas (Strings)

En Java el manejo de cadenas es un tipo object. (en Java es necesario el uso del operador new para crear un nuevo Objeto). Sin embargo cuando hablamos de cadenas, esto no es necesario. podemos simplemente declarar un tipo String y asignar un valor directamente a esta variable. es por ello que pareciera que el tipo String es un tipo primitivo, pero no es así.

Ej:
```Java
// String nombreVariable = valor;
String saludo = "Hola Mundo"; 
```

Al comparar objetos no utilizamos el simbolo == como lo hacemos con los tipos primitivos, si no que vamos a utilizar el método equals. en el caso de cadenas esto nos permitirá comparar el contenido de la cadena.

Comparación:
```Java
// nombreVariable.equals(String);
saludo.equals("Hola Mundo");
```
## Caracteres de Escape al Utilizar Cadenas

<table>
  <tr>
    <th>Secuencia de Escape</th>
    <th>Descripción</th>
  </tr>
  <tr>
    <td>\t</td>
    <td>Inserta un tabulador</td>
  </tr>
  <tr>
    <td>\b</td>
    <td>Inserta un retroceso (backspace)</td>
  </tr>
  <tr>
    <td>\n</td>
    <td>Inserta una nueva línea</td>
  </tr>
  <tr>
    <td>\r</td>
    <td>Inserta un retorno de carro</td>
  </tr>
  <tr>
    <td>\f</td>
    <td>Se mueve a la siguiente página (Form feed) Se utiliza para impresoras, no en consolas</td>
  </tr>
  <tr>
    <td>\'</td>
    <td>Inserta una comilla simple</td>
  </tr>
  <tr>
    <td>\"</td>
    <td>Inserta una comilla doble</td>
  </tr>
  <tr>
    <td>\\</td>
    <td>Inserta una barra invertida</td>
  </tr>
</table>

___
# Concatenación en Java

```Java
public class Main
{
  public static void main(String[] args)
  {
    String usuario = "Stiven";
    String saludar = "Hola";
    
    System.out.println( saludar + " " + usuario );
    // output: Hola Stiven
    
    System.out.println( "Hola mi nombre es: " + usuario );
    // output: Hola mi nombre es: Stiven
    
    //shortcut: soutv
    System.out.println( "saludar = " + saludar );
    // output: saludar = Hola
  }
}
```
___
# Caracteres Especiales en Java (Ejercicio) 

```Java
public class Main
{
  public static void main(String[] args)
  {
    String nombre = "Lisbeth";
    String apellido = "Cifuentes";
    
    System.out.println( nombre + "\t" + apellido ); // output: Lisbeth Cifuentes
    
    System.out.println( "Nueva linea: \n" + nombre ); 
    // output: Nueva linea: 
    // Lisbeth
    
    System.out.println( "tabulador: \t" + nombre ); 
    // output: tabulador: 	Lisbeth
    
    System.out.println( "retroceso: \b" + nombre ); 
    // output: retroceso:Lisbeth
    
    System.out.println( "retorno de carro: \r" + nombre ); // note: se va al inicio de esta linea
    // output: Lisbeth
    
    System.out.println( "comilla simple: \'" + nombre + "\'"); 
    // output: comilla simple: 'Lisbeth'
    
    System.out.println( "comilla doble: \"" + nombre + "\"" ); 
    // output: comilla doble: "Lisbeth"
    
  }
}
```
___
# Clase Scanner en Java

Capturar información desde la consola del usuario.

```Java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in); // definir una variable para poder leer los valores que proporcione el usuario
        
        System.out.println("Proporciona tu nombre:"); // indiquemos al usuario que debe proporcionarlo
        String usuario = scanner.nextLine(); 
        String saludar = "Saludos";
        System.out.println(saludar + " " + usuario);
    }
}
```
___
# Conversión de tipos primitivos en Java

```Java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // String to Double
        double valorPi = Double.parseDouble("3.14"); 
        System.out.println("valorPi = " + valorPi);
        // output: valorPi = 3.14

        // String to char
        char c = "hola".charAt(0); // charAt(indice de la cadena)
        System.out.println("c = " + c);
        // output: c = h

        // Ejemplo: 
        Scanner scanner = new Scanner(System.in);
        char caracter = scanner.nextLine().charAt(0); // de una cadena ingresada por el usuario, toma el primer character
        System.out.println("caracter = " + caracter);

        // Tipo primitivo to String
        String valorPiTexto = String.valueOf(valorPi);
        System.out.println("valorPiTexto = " + valorPiTexto);

        // También se puede hacer de esta forma
        String valorPiTexto2 = "" + valorPi;
        System.out.println("valorPiTexto2 = " + valorPiTexto2);

        // Podemos meter un tipo byte dentro de un short
        byte b = 10;
        short s = b;

        // Error: pero no podemos meter un short dentro de un byte por su tamaño
        short s2 = 15;
        byte b2 = (byte) s2; // pero podemos hacer un Casting de esta forma
        // si tenemos una expresión debemos meterla en parentesis: (byte) (s2 + 1)
    }
}

```
