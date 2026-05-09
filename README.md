# Tutorial

This tutorial will guide you through setting up your desktop application with everything ready to go.

## 💖 Support the project and get featured as a contributor!

If this project has been helpful or inspiring, consider making a donation to help it grow.

As a thank you, your name will be proudly listed in the README.
[Donate now](https://buymeacoffee.com/plantfall)

## Getting the Application

Here you going to see how to initialize your own project.

See Video Tutorial
[Watch Now](https://youtu.be/HJPHG8Bqq98)

Initialize your own project:

1. Clone this project

```bash
git clone https://github.com/eliezer-dev-software-enginner/coesion-effect.git
```

Or download the release app:
[Download](https://github.com/eliezer-dev-software-enginner/coesion-effect/releases/edit/v1.0.2)

## Building your App

```bash
mvn clean package
```

## Distributing Your App

After you have built it you can distribute easily:

1. Open your terminal and run create-installer.bat

```bash
.\scripts\create-installer.bat
```

After that, your app will be generated in the `dist` folder:

- The `.exe` will be inside `dist/MyApp`
- The `.msi` installer will be inside `dist/`

## Customizing Your App

To update metadata like description, icon, version, and vendor name, edit the `jpackage` section inside `scripts/create-installer.bat.`

## Contribute

Want to contribute?
Feel free to open a PR and become part of the team behind this open-source project!

## Requirements

Make sure you have the following installed for building purposes:

- WiX Toolset (required to generate MSI installers)
  [Download WixToolset 3.14.1(wix314.exe)](https://github.com/wixtoolset/wix3/releases/tag/wix3141rtm)

Then install the app and procced with installation steps. After that you have to set the variable path.
![wix_tollset_path](https://github.com/user-attachments/assets/d92cc6ec-fdd9-4eac-bb82-1c878fa66937)


## Helping

## vm arguments for run application:
```bash
--module-path ./java_fx_modules/windows-25.0.1/lib --add-modules javafx.controls,javafx.graphics -Dprism.verbose=true --enable-native-access=javafx.graphics
```

## creating java runtime
```bash
--module-path ./java_fx_modules/windows-25.0.1/lib --add-modules javafx.controls,javafx.graphics -Dprism.verbose=true --enable-native-access=javafx.graphics
```

## testing
```bash
.\build\runtime\bin\java.exe "-Djava.library.path=build\bin" -cp "build\app.jar" my_app.Launch
```

## creating msi app (windows)
```bash
jpackage --input "build" --name "Meu App" --main-jar "app.jar" --main-class "my_app.Launch" --dest "dist" --type "msi" --runtime-image "build\runtime" --java-options "-Djava.library.path=$APPDIR\bin" --icon "src\main\resources\assets\app_ico.ico" 
```