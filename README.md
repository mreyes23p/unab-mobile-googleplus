# unab-mobile-googleplus

Proyecto Apache cordova de Ejemplo para login con Google Plus

Plugin usado: https://github.com/EddyVerbruggen/cordova-plugin-googleplus

Pasos para crear el proyecto:

1. $cordova create unab-mobile-googleplus com.unab.mobile.googleplus
2. ``` $cordova platform add android ```
3. ``` $cordova build ```
4. Chequear que dispositivo este contectado y reconocido por el notebook
5. ``` $adb devices ```
6. ``` $cordova run android ```
7. Abrir proyecto en un editor como Atom.io o Brackets.io
8. Agregar plugin de google plus para cordova
	a. ``` $cordova plugin add nl.x-services.plugins.googleplus ```
9. Google plus API Setup https://developers.google.com/+/mobile/android/samples/quickstart-android
	a. Ir a Google Developer Console https://console.developers.google.com/project
	b. Agregar un proyecto. Indicar un nombre, crear y esperar a que se cree el proyecto
  c. Ir a APIs & Auth/APIs y habilitar Google+ Api
  d. Ir a APIs & Auth/Consent Screen e indicar un correo y "product name”
  e. Ir a APIs & Auth/Credentials y crear "Client ID" y seleccionar "Installed App” + Android
    i. Indicar el package name del punto 1. (i.e com.unab.mobile.googleplus)
    ii.Indicar el "Signing certificate fingerprint (sha1)”. Mas info en: https://developer.android.com/tools/publishing/app-signing.html y https://developers.google.com/+/mobile/android/samples/quickstart-android
      1. Comando: ``` $keytool -exportcert -alias androiddebugkey -keystore <path-to-debug-or-production-keystore> -list -v ```
      2. Copiar el valor de la linea que dice Sha1
    iii.Presionar “Create Client Id”
10. Para efectos de testing, volver al proyecto en el editor de código y copiar el contenido del archivo ${RAIZ_PROYECTO}/plugins/nl.x-services.plugins.googleplus/demo/index.html en ${RAIZ_PROYECTO}/www/index.html
11. Ejecutar Paso 3, 4 y 5

 
