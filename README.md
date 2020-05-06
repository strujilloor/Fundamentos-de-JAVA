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

