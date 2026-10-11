```java
import java.util.Scanner;

public class EjemploScannerSencillo {
    public static void main(String[] args) {
        // 1. Conectamos Scanner directamente con la entrada estándar (System.in)
        Scanner teclado = new Scanner(System.in);

        // 2. Leemos una línea completa de texto con nextLine()
        System.out.print("Ingresa tu nombre: ");
        String nombre = teclado.nextLine();

        // 3. Leemos un número entero directamente con nextInt().
        //    A diferencia de BufferedReader, Scanner convierte el dato por nosotros
        System.out.print("Ingresa tu edad: ");
        int edad = teclado.nextInt();

        // 4. Mostramos el resultado en pantalla
        System.out.println("Hola, " + nombre + ". Tienes " + edad + " años.");

        // 5. Cerramos el objeto Scanner
        teclado.close();
    }
}

```
