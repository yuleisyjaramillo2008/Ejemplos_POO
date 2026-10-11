```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
public class EjemploBufferedReaderSencillo {
    // Agregamos 'throws IOException' para no complicar el código con try-catch
    public static void main(String[] args) throws IOException {

        // 1. InputStreamReader convierte los bytes de System.in a caracteres.
        //    BufferedReader envuelve ese flujo para guardarlo en un búfer en memoria.
        BufferedReader lector = new BufferedReader(new InputStreamReader(System.in));

        // 2. Leemos una línea de texto con readLine()
        System.out.print("Ingresa tu nombre: ");
        String nombre = lector.readLine();

        // 3. Leemos la edad. A diferencia de Scanner, readLine() siempre
        //    devuelve String, así que la convertimos manualmente con Integer.parseInt
        System.out.print("Ingresa tu edad: ");
        int edad = Integer.parseInt(lector.readLine());

        // 4. Mostramos el resultado en pantalla
        System.out.println("Hola, " + nombre + ". Tienes " + edad + " años.");
    }
}
```
