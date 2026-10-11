```java
import java.io.Console;
import java.util.Arrays;

public class EjemploConsole {
    public static void main(String[] args) {
        // 1. Obtenemos la consola del sistema
        Console consola = System.console();

        // 2. Verificamos que la consola esté disponible
        if (consola == null) {
            System.err.println("No hay consola disponible en este entorno.");
            return;
        }

        // 3. Leemos el nombre de usuario (texto normal)
        String usuario = consola.readLine("Ingresa tu usuario: ");

        // 4. Leemos la clave sin mostrar los caracteres
        char[] clave = consola.readPassword("Ingresa tu clave: ");

        // 5. Mostramos el saludo
        consola.printf("¡Bienvenido/a, %s! Sesión iniciada.%n", usuario);

        // 6. Borramos la clave de la memoria, porque ya no se necesita
        Arrays.fill(clave, ' ');
    }
}

```
