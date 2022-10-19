# BasicStructureReactNativeApp

Anleitung:
1. Folgende Ressourcen downloaden:
  Android Studio: https://developer.android.com/studio/archive?hl=de
  NodeJs: https://nodejs.org/download/release/v17.8.0/
  React Native: https://reactnative.dev/docs/environment-setup
  jdk11: https://www.oracle.com/java/technologies/downloads/#java11-windows

2. Bei der Installation folgende Reihenfolge beachten
  - Android Studio (Unterbrechen ab installation Sndroid SDK)
  - NodeJs installieren
  - JDK 11 installieren
  - Installation Android Studio fortsetzen
  
Android Studio einrichten
  - More Actions -> SDK Manager
    Hyper-V aktivieren im BIOS
    SDK Tools
      Intel x86 Emulator Accelerator (HAXM installer) abwählen
      Android SDK Build-Tools 33
        33.0.0 abwählen
        30.0.0 Haken setzen
      Android Emulator muss ein Haken gesetzt sein
      Android SDK Platform-Tools muss ein Haken gesetzt sein
    SDK Platforms
      Android 11.0(R)
        Android SDK Platform 30 Haken setzen
        Sourecs for Android 30 Haken setzen
        Intel x86 Atom_64 System Image Haken setzen
        Google APIs Intel x86 Atom_64 System Image Haken setzen
      Android Tiramisu
        Android SDK Platform 33 abwählen
        Sourecs for Android 33 abwählen
Systemumgebungsvariablen erstellen
  Windows-Taste -> Systemumgebungsvariablen bearbeiten -> Umgebungsvariablen...
    Systemvariablen -> NEU
      Namen der Variablen: ANDROID_HOME
      Wert der Variable: C:\User\<NAME>\AppData\Local\Android\Sdk
    Systemvariablen -> Path aus der Liste auswählen -> Bearbeiten...
      Neu -> C:\User\<NAME>\AppData\Local\Android\Sdk\platform-tools
    Systemvariablen -> NEU
      Namen der Variablen: JAVA_HOME
      Wert der Variable: C:\Program Files\Java\jdk-11.0.17
      
Android Studio Emulator erstellen
  New Project
  Empty Activity
  Name des Projektes eingeben
    Language: Java
    Minimum SDK: API 30: Android 11.0 (R)
  finish
  finish
  Abwarten bis unten in der Leiste alle installationen gemacht wurden
  Android Studio neu starten
  
Android Studio Einstellungen
  File -> Settings -> Build, Execution, Deployment -> Build Tools -> Gradle
    Gradle JDK: Android Studio java home
  Nach dem Einstellung einmal File -> Reload All from Disk ausführen
  
Android Studio Gerät erstellen
  unter Device Manager -> Virtual -> Create Device
    Category: Phone
    Name: Pixel XL
  Next
    x86 Images
      Release Name: R
      target: Android 11.0 (Google APIs)
  Next
    Show Advanced Settings
      Memory and Storage
        RAM: 1024
  Finish
    
Neues React Native Project erstellen
  npm uninstall -g react-native-cli @react-native-community/cli
  npx react-native init <NAME_PROJEKT> --version 0.69.0
  cd <NAME_PROJEKT>
  npx react-native run-android
  
  

Quelle: https://www.youtube.com/watch?v=6tEV6H07Fd8
