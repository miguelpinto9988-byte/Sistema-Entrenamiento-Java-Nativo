# Sistema de Entrenamiento — Android Java Nativo

Repositorio para la migración inicial de una aplicación de entrenamiento a **Android nativo con Java**.

> **Estado:** versión parcial en desarrollo. No está verificado que compile ni que todas las funciones originales estén migradas.

## Estructura esperada

Copia a la **raíz** de este repositorio el contenido descomprimido del proyecto fuente:

- `app/` — módulo Android, Java, catálogos y medios locales.
- `build.gradle`, `settings.gradle`, `gradle.properties` — configuración Gradle.
- `gradle/wrapper/gradle-wrapper.properties` — versión de Gradle.
- `ESTADO_DE_MIGRACION.md` — funcionalidades migradas y pendientes.

No incluyas una carpeta externa adicional por encima de `app/`: GitHub Actions busca `app/build.gradle` en la raíz.

## Compilación automática

El flujo [Compilar APK Android](.github/workflows/android-apk.yml) ejecuta Gradle 8.9 con JDK 17 y SDK 35 cuando se publican cambios de la aplicación. También puede ejecutarse manualmente en **Actions → Compilar APK Android → Run workflow**.

Si la compilación finaliza correctamente, descarga la APK de prueba en **Actions → ejecución → Artifacts → apk-java-nativo-debug**.

**Atención:** la APK de depuración no es un paquete de publicación. No actualiza la antigua aplicación ni preserva automáticamente sus datos; instala un identificador diferente. No compartas claves privadas de firma.

## Migración pendiente

La versión fuente inicial contiene un catálogo de 2.000 fichas, recursos locales, pantallas nativas y registros básicos. Todavía faltan partes importantes de la interfaz avanzada y los motores antiguos. Los 800 ejercicios adicionales permanecen excluidos de la planificación automática hasta validación independiente.
