---
title: "NativeLibSettings"
linktitle: "NativeLibSettings"
second_title: "Aspose.Words para Java"
description: "Esta clase ayuda a establecer varias opciones, como la carpeta temporal para las bibliotecas nativas de Aspose.Words y si las bibliotecas nativas deben cargarse y usarse en Java."
type: docs
weight: 475
url: /es/java/com.aspose.words/nativelibsettings/
---

**Inheritance:**
java.lang.Object
```
public class NativeLibSettings
```

Esta clase ayuda a establecer varias opciones, como la carpeta temporal para las bibliotecas nativas de Aspose.Words y si las bibliotecas nativas deben cargarse y usarse.
## Métodos

| Método | Descripción |
| --- | --- |
| [clearAsposeNativeTmpDirectory()](#clearAsposeNativeTmpDirectory) | Borra el directorio donde se almacenan las bibliotecas temporales de Aspose. |
| [getInterruptThreadIfImageExceptionThrown()](#getInterruptThreadIfImageExceptionThrown) | Devuelve el valor actual de la propiedad que controla la interrupción del hilo en excepciones de imagen. |
| [getTmpDirectoryPath()](#getTmpDirectoryPath) | Devuelve la ruta al directorio temporal de las bibliotecas nativas. |
| [getUseJAIImageRendering()](#getUseJAIImageRendering) | Obtiene un valor que determina si JAI (Java Advanced Imaging) se emplea durante la renderización de imágenes del documento. |
| [isHarfBuzzNativeLibLoaded()](#isHarfBuzzNativeLibLoaded) | Devuelve `true` si se cargan las bibliotecas HarfBuzz. |
| [isWinNativeLibLoaded()](#isWinNativeLibLoaded) | Devuelve `true` si se cargan las bibliotecas WindowsNativeCall. |
| [loadHarfBuzzNativeLib()](#loadHarfBuzzNativeLib) | Establece cargar y usar las bibliotecas harfbuzz-shaping-engine-dll.dll. |
| [loadWinNativeLib()](#loadWinNativeLib) | Sets to load and use WindowsNativeCall\_x86 | \_x64.dll bibliotecas. |
| [setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown)](#setInterruptThreadIfImageExceptionThrown-boolean) | Establece la propiedad que define el comportamiento al manejar excepciones de imagen. |
| [setTmpDirectoryPath(String path)](#setTmpDirectoryPath-java.lang.String) | Especifica la ruta al directorio temporal de las bibliotecas nativas. |
| [setUseJAIImageRendering(boolean useJAIImageRendering)](#setUseJAIImageRendering-boolean) | Establece un valor que determina si JAI (Java Advanced Imaging) se emplea durante la renderización de imágenes del documento. |
| [skipHarfBuzzNativeLib()](#skipHarfBuzzNativeLib) | Omite la carga y usa las bibliotecas harfbuzz-shaping-engine-dll.dll. |
| [skipWinNativeLib()](#skipWinNativeLib) | Skip loading and use WindowsNativeCall\_x86 | \_x64.dll bibliotecas. |
### clearAsposeNativeTmpDirectory() {#clearAsposeNativeTmpDirectory}
```
public static void clearAsposeNativeTmpDirectory()
```


Borra el directorio donde se almacenan las bibliotecas temporales de Aspose.

### getInterruptThreadIfImageExceptionThrown() {#getInterruptThreadIfImageExceptionThrown}
```
public static boolean getInterruptThreadIfImageExceptionThrown()
```


Devuelve el valor actual de la propiedad que controla la interrupción del hilo en excepciones de imagen.

**Remarks:**

El valor predeterminado es `false`.

**Returns:**
boolean - indica si el hilo debe interrumpirse en excepciones de imagen.
### getTmpDirectoryPath() {#getTmpDirectoryPath}
```
public static String getTmpDirectoryPath()
```


Devuelve la ruta al directorio temporal de las bibliotecas nativas.

**Returns:**
java.lang.String
### getUseJAIImageRendering() {#getUseJAIImageRendering}
```
public static boolean getUseJAIImageRendering()
```


Obtiene un valor que determina si JAI (Java Advanced Imaging) se emplea durante la renderización de imágenes del documento. En algunos casos, esto puede mejorar el rendimiento.

**Remarks:**

El valor predeterminado es `true`.

JAI solo se utilizará si se incluye como una dependencia como se describe [aquí][]. Ciertas imágenes podrían no renderizarse correctamente si JAI está deshabilitado.


[here]: https://docs.aspose.com/words/java/system-requirements/#optional-dependencies

**Returns:**
boolean - indica si JAI se usa.
### isHarfBuzzNativeLibLoaded() {#isHarfBuzzNativeLibLoaded}
```
public static boolean isHarfBuzzNativeLibLoaded()
```


Devuelve `true` si se cargan las bibliotecas HarfBuzz. Por defecto, se cargan las bibliotecas nativas.

**Returns:**
boolean
### isWinNativeLibLoaded() {#isWinNativeLibLoaded}
```
public static boolean isWinNativeLibLoaded()
```


Devuelve `true` si se cargan las bibliotecas WindowsNativeCall. Por defecto, se cargan las bibliotecas nativas.

**Returns:**
boolean
### loadHarfBuzzNativeLib() {#loadHarfBuzzNativeLib}
```
public static void loadHarfBuzzNativeLib()
```


Establece cargar y usar las bibliotecas harfbuzz-shaping-engine-dll.dll. Por defecto, se cargan las bibliotecas nativas.

### loadWinNativeLib() {#loadWinNativeLib}
```
public static void loadWinNativeLib()
```


Establece la carga y uso de las bibliotecas WindowsNativeCall\_x86|\_x64.dll. Por defecto, las bibliotecas nativas se cargan.

### setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown) {#setInterruptThreadIfImageExceptionThrown-boolean}
```
public static void setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown)
```


Establece la propiedad que define el comportamiento al manejar excepciones de imagen. Si la propiedad se establece en true, el hilo de ejecución se interrumpirá cuando ocurra una excepción durante el procesamiento de la imagen.

**Remarks:**

El valor predeterminado es `false`.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| abortSavingIfImageExceptionThrown | boolean | true - interrumpir el hilo en excepciones de imagen, false - no interrumpir |

### setTmpDirectoryPath(String path) {#setTmpDirectoryPath-java.lang.String}
```
public static void setTmpDirectoryPath(String path)
```


Especifica la ruta al directorio temporal de las bibliotecas nativas.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| ruta | java.lang.String | la ruta al directorio temporal de bibliotecas nativas. |

### setUseJAIImageRendering(boolean useJAIImageRendering) {#setUseJAIImageRendering-boolean}
```
public static void setUseJAIImageRendering(boolean useJAIImageRendering)
```


Establece un valor que determina si se emplea JAI (Java Advanced Imaging) durante el renderizado de imágenes de documentos. En algunos casos, esto puede mejorar el rendimiento.

**Remarks:**

El valor predeterminado es `true`.

JAI solo se utilizará si se incluye como una dependencia como se describe [aquí][]. Ciertas imágenes podrían no renderizarse correctamente si JAI está deshabilitado.


[here]: https://docs.aspose.com/words/java/system-requirements/#optional-dependencies

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| useJAIImageRendering | boolean | ¿es necesario usar JAI? |

### skipHarfBuzzNativeLib() {#skipHarfBuzzNativeLib}
```
public static void skipHarfBuzzNativeLib()
```


Omitir la carga y usar las bibliotecas harfbuzz-shaping-engine-dll.dll. Por defecto, se cargan las bibliotecas nativas.

### skipWinNativeLib() {#skipWinNativeLib}
```
public static void skipWinNativeLib()
```


Omitir la carga y usar las bibliotecas WindowsNativeCall\_x86|\_x64.dll. Por defecto, se cargan las bibliotecas nativas.

