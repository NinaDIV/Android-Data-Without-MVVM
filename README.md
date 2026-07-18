# Android — Consumo de Datos sin MVVM (Laboratorio 07)

![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat&logo=kotlin&logoColor=white)
![Android](https://img.shields.io/badge/Android-3DDC84?style=flat&logo=android&logoColor=white)
![Gradle](https://img.shields.io/badge/Gradle-02303A?style=flat&logo=gradle&logoColor=white)

Proyecto Android en Kotlin que implementa el consumo y manejo de datos **sin** utilizar el patrón de arquitectura MVVM. Sirve como punto de comparación para entender por qué MVVM mejora la organización, el desacoplamiento y la testabilidad del código.

## 📋 Temas cubiertos

- Acceso a datos directamente desde Activities
- Manejo de estado sin ViewModel
- Llamadas de red sin capa de abstracción

## 🛠️ Tecnologías

| Tecnología | Uso |
|---|---|
| Kotlin | Lenguaje principal de la app |
| Android SDK | Plataforma de destino |
| Gradle (Kotlin DSL) | Sistema de build (`build.gradle.kts`, `settings.gradle.kts`) |

## ✅ Requisitos previos

Antes de ejecutar el proyecto necesitas tener instalado:

- **Android Studio** (versión reciente, con el Android SDK incluido)
- **JDK 17** (requerido por las versiones actuales del Android Gradle Plugin)
- Un **emulador de Android** configurado en el AVD Manager, o un **dispositivo físico** con la depuración USB activada

No se requieren variables de entorno, claves de API ni servicios externos adicionales.

## 🚀 Instalación y ejecución

1. Clona el repositorio:

   ```bash
   git clone https://github.com/NinaDIV/Android-Data-Without-MVVM.git
   cd Android-Data-Without-MVVM
   ```

2. Abre la carpeta del proyecto en **Android Studio** (`File > Open`) y espera a que Gradle sincronice las dependencias automáticamente.

3. Selecciona un emulador o conecta tu dispositivo físico.

4. Ejecuta la app con el botón **Run** (▶) o desde la terminal:

   ```bash
   ./gradlew installDebug
   ```

   En Windows:

   ```bash
   gradlew.bat installDebug
   ```

5. La aplicación se instalará y abrirá en el emulador o dispositivo seleccionado.

Para generar un APK de depuración sin instalarlo:

```bash
./gradlew assembleDebug
```

El APK queda en `app/build/outputs/apk/debug/`.

## 📂 Estructura del proyecto

```
Android-Data-Without-MVVM/
├── app/                    # Módulo principal de la aplicación Android
├── LAB07/                  # Material del laboratorio 07
├── LAB07.zip               # Copia comprimida del laboratorio
├── gradle/                 # Wrapper de Gradle
├── build.gradle.kts        # Configuración de build (raíz)
├── settings.gradle.kts     # Configuración de módulos
├── gradle.properties       # Propiedades de Gradle
├── gradlew / gradlew.bat   # Scripts del wrapper (Linux/macOS y Windows)
└── README.md
```

## 💡 Lección aprendida

Este enfoque muestra los problemas comunes de acoplamiento cuando no se separan las responsabilidades entre la UI y la lógica de negocio: las Activities terminan concentrando acceso a datos, estado y presentación. Compara este proyecto con su versión refactorizada usando MVVM para ver la diferencia práctica.
