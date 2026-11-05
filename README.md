# Sistema de Entrenamiento — Android Java nativo

Proyecto de migración **parcial** a Android nativo con Java. El código fuente y los recursos multimedia se entregaron en un archivo ZIP dentro del chat. La compilación y el funcionamiento no han sido verificados.

## Estado del repositorio

**Pendiente de importación:** aún no se han añadido `app/`, `gradle/` ni los archivos de configuración del proyecto.

La conexión de GitHub utilizada para preparar este repositorio permite crear archivos de texto y flujos de trabajo, pero **no puede transferir directamente el ZIP de unos 153 MB adjunto en ChatGPT**.

## Importar el archivo completo de una sola vez

1. Descargar desde el chat **las diez partes ZIP** del proyecto, de `Proyecto_Java_Parte_01_de_10.zip` a `Proyecto_Java_Parte_10_de_10.zip` (cada parte se abre como archivo ZIP independiente).
2. Abrir [Crear publicación](https://github.com/miguelpinto9988-byte/Sistema-Entrenamiento-Java-Nativo/releases/new).
3. Crear la etiqueta `v0.1.0-java` (dirigida a la rama `main`).
4. **Adjuntar las diez partes ZIP** a la misma publicación **antes** de pulsar `Publish release`, sin cambiar sus nombres.
5. Publicar. El flujo [Importar proyecto completo desde ZIP](.github/workflows/importar-proyecto-zip.yml) descargará los diez adjuntos, comprobará los ~3.557 archivos y tratará de publicarlos en `main`.

El importador también acepta el ZIP original si se dispone del archivo único de 153 MB. No es necesario unir manualmente las diez partes.

Si la importación no termina, revisar [Actions](../../actions) y los mensajes de error. Algunas cuentas necesitan permitir a GitHub Actions escribir en el repositorio en *Settings → Actions → General → Workflow permissions*.

## Compilación automática

Después de que el código esté publicado, el flujo [Compilar APK Android (Java)](.github/workflows/android-apk.yml) intentará compilar con JDK 17, Android SDK 35, Gradle 8.9 y Android Gradle Plugin 8.7.3.

Si tiene éxito, la APK de depuración estará en **Actions → ejecución → Artifacts** como `apk-java-nativo-debug`.

## Alcance y precauciones

- 2.000 fichas de ejercicios y multimedia local.
- Perfil, consulta, registros básicos y navegación nativa.
- No es aún equivalente a la aplicación anterior: faltan módulos y animaciones.
- Los 800 ejercicios posteriores no están autorizados para planificación automática sin validación.
- La APK de depuración utiliza un identificador diferente y no migra datos automáticamente.
- No publicar contraseñas, tokens ni claves privadas de firma.

