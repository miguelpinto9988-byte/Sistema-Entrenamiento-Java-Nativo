# Sistema de Entrenamiento — Android Java Nativo

Este repositorio aloja el proceso de migración a Android nativo (Java).

> **Estado:** migración inicial y parcial; todavía no hay una compilación APK verificada ni equivalencia funcional completa con la aplicación original.

## Cómo importar el proyecto completo sin subir miles de archivos

1. Descarga `Sistema_Entrenamiento_Java_Nativo_Proyecto.zip` desde el archivo facilitado en la conversación.
2. Abre [Crear nueva publicación de GitHub](https://github.com/miguelpinto9988-byte/Sistema-Entrenamiento-Java-Nativo/releases/new).
3. En **Choose a tag**, crea `v0.1.0-java` desde `main`.
4. Pon como título `Proyecto Android Java nativo — primera migración`.
5. Adjunta **el ZIP completo**, sin descomprimirlo. Debe conservar el nombre exacto `Sistema_Entrenamiento_Java_Nativo_Proyecto.zip`.
6. Pulsa **Publish release**.

La publicación dispara automáticamente [GitHub Actions](https://github.com/miguelpinto9988-byte/Sistema-Entrenamiento-Java-Nativo/actions). El flujo descarga el ZIP, lo descomprime, añade los archivos a `main` e intenta generar una APK de depuración. El flujo necesita permiso de escritura de GitHub Actions al repositorio; si falla al hacer push, revisa **Settings → Actions → General → Workflow permissions**.

Si la compilación termina correctamente, la APK aparecerá en **Actions → ejecución → Artifacts → apk-java-nativo-debug**.

## Estructura esperada

- `app/`: código Java, catálogo y recursos multimedia.
- `settings.gradle`, `build.gradle`, `gradle.properties`: configuración Android.
- `gradle/wrapper/`: propiedades de Gradle.
- `ESTADO_DE_MIGRACION.md`: funciones completadas y pendientes.

## Alcance y seguridad

El proyecto fuente contiene fichas de 2.000 ejercicios, recursos multimedia locales y una interfaz nativa inicial. Los 800 ejercicios adicionales no están habilitados para planificación automática. Aún falta migrar funciones avanzadas del sistema original y probar el proyecto en dispositivos Android.

No publiques claves privadas, contraseñas ni archivos de firma de producción. La APK debug es solo para pruebas y no actualiza automáticamente la versión Android antigua.
