> 🧩 HomeCinema: fork enfocado en español. Consulta [SPANISH_FORK.md](SPANISH_FORK.md).

<div align="center">

  <img src="homecinema-icon.png" alt="HomeCinema" width="320" />

  <p>
    Una app de cine en casa libre y de código abierto para tu teléfono, tu escritorio
    y la tele que ya tienes. Español por defecto, sin filtrar contenido.
  </p>

  [Sitio web](https://nuvio.tv) · [Releases](https://github.com/Hernandezelite/HomeCinema/releases/latest) · [Apoyar](https://nuvio.tv/support)

</div>

## Descargar HomeCinema

- [Android APK](https://github.com/Hernandezelite/HomeCinema/releases/latest)
- iOS con AltStore o SideStore: añade esta URL de fuente en la sección Sources de la app:
  https://raw.githubusercontent.com/Hernandezelite/HomeCinema/cmp-rewrite/store.json
- iOS beta: usa esta otra fuente para incluir pre-releases:
  https://raw.githubusercontent.com/Hernandezelite/HomeCinema/cmp-rewrite/store-beta.json

## Compilar desde el código

```bash
git clone https://github.com/Hernandezelite/HomeCinema.git
cd HomeCinema
```

### Android

Requiere Android Studio y el SDK de Android.

```bash
./gradlew :androidApp:assembleDebug -Pnuvio.android.distribution=full
```

### iOS

Requiere macOS y Xcode.

```bash
env NUVIO_IOS_DISTRIBUTION=full xcodebuild \
  -project iosApp/iosApp.xcodeproj \
  -scheme iosApp \
  -configuration Debug \
  -sdk iphonesimulator \
  -derivedDataPath build/ios-derived-full-simulator \
  CODE_SIGNING_ALLOWED=NO \
  build
```

La app compartida está construida con Kotlin Multiplatform y Compose Multiplatform.

## Licencia

[GNU General Public License v3.0](./LICENSE)
