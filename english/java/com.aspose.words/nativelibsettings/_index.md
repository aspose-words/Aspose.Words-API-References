---
title: NativeLibSettings
linktitle: NativeLibSettings
second_title: Aspose.Words for Java
description: This class helps to set various options such as temporary folder for Aspose.Words native libraries and whether native libraries should be loaded and used in Java.
type: docs
weight: 470
url: /java/com.aspose.words/nativelibsettings/
---

**Inheritance:**
java.lang.Object
```
public class NativeLibSettings
```

This class helps to set various options such as temporary folder for Aspose.Words native libraries and whether native libraries should be loaded and used.
## Methods

| Method | Description |
| --- | --- |
| [clearAsposeNativeTmpDirectory()](#clearAsposeNativeTmpDirectory) | Clears the directory where Aspose temporary libraries are stored. |
| [getTmpDirectoryPath()](#getTmpDirectoryPath) | Return the path to the temporary directory of native libraries. |
| [getUseJAIImageRendering()](#getUseJAIImageRendering) | Gets a value that determines whether JAI (Java Advanced Imaging) is employed during the rendering of document images. |
| [isHarfBuzzNativeLibLoaded()](#isHarfBuzzNativeLibLoaded) | Returns `true` if HarfBuzz libraries is loaded. |
| [isWinNativeLibLoaded()](#isWinNativeLibLoaded) | Returns `true` if WindowsNativeCall libraries is loaded. |
| [loadHarfBuzzNativeLib()](#loadHarfBuzzNativeLib) | Sets to load and use harfbuzz-shaping-engine-dll.dll libraries. |
| [loadWinNativeLib()](#loadWinNativeLib) | Sets to load and use WindowsNativeCall\_x86|\_x64.dll libraries. |
| [setTmpDirectoryPath(String path)](#setTmpDirectoryPath-java.lang.String) | Specifies the path to the temporary directory of native libraries. |
| [setUseJAIImageRendering(boolean useJAIImageRendering)](#setUseJAIImageRendering-boolean) | Sets a value that determines whether JAI (Java Advanced Imaging) is employed during the rendering of document images. |
| [skipHarfBuzzNativeLib()](#skipHarfBuzzNativeLib) | Skip loading and use harfbuzz-shaping-engine-dll.dll libraries. |
| [skipWinNativeLib()](#skipWinNativeLib) | Skip loading and use WindowsNativeCall\_x86|\_x64.dll libraries. |
### clearAsposeNativeTmpDirectory() {#clearAsposeNativeTmpDirectory}
```
public static void clearAsposeNativeTmpDirectory()
```


Clears the directory where Aspose temporary libraries are stored.

### getTmpDirectoryPath() {#getTmpDirectoryPath}
```
public static String getTmpDirectoryPath()
```


Return the path to the temporary directory of native libraries.

**Returns:**
java.lang.String
### getUseJAIImageRendering() {#getUseJAIImageRendering}
```
public static boolean getUseJAIImageRendering()
```


Gets a value that determines whether JAI (Java Advanced Imaging) is employed during the rendering of document images. In some cases, this may improve performance.

**Remarks:**

The default value is `true`.

JAI will only be utilized if it is included as a dependency as described [here][]. Certain images might not render correctly if JAI is disabled.


[here]: https://docs.aspose.com/words/java/system-requirements/#optional-dependencies

**Returns:**
boolean - is JAI used.
### isHarfBuzzNativeLibLoaded() {#isHarfBuzzNativeLibLoaded}
```
public static boolean isHarfBuzzNativeLibLoaded()
```


Returns `true` if HarfBuzz libraries is loaded. By default, native libraries are loaded.

**Returns:**
boolean
### isWinNativeLibLoaded() {#isWinNativeLibLoaded}
```
public static boolean isWinNativeLibLoaded()
```


Returns `true` if WindowsNativeCall libraries is loaded. By default, native libraries are loaded.

**Returns:**
boolean
### loadHarfBuzzNativeLib() {#loadHarfBuzzNativeLib}
```
public static void loadHarfBuzzNativeLib()
```


Sets to load and use harfbuzz-shaping-engine-dll.dll libraries. By default, native libraries are loaded.

### loadWinNativeLib() {#loadWinNativeLib}
```
public static void loadWinNativeLib()
```


Sets to load and use WindowsNativeCall\_x86|\_x64.dll libraries. By default, native libraries are loaded.

### setTmpDirectoryPath(String path) {#setTmpDirectoryPath-java.lang.String}
```
public static void setTmpDirectoryPath(String path)
```


Specifies the path to the temporary directory of native libraries.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| path | java.lang.String | the path to the temporary directory of native libraries. |

### setUseJAIImageRendering(boolean useJAIImageRendering) {#setUseJAIImageRendering-boolean}
```
public static void setUseJAIImageRendering(boolean useJAIImageRendering)
```


Sets a value that determines whether JAI (Java Advanced Imaging) is employed during the rendering of document images. In some cases, this may improve performance.

**Remarks:**

The default value is `true`.

JAI will only be utilized if it is included as a dependency as described [here][]. Certain images might not render correctly if JAI is disabled.


[here]: https://docs.aspose.com/words/java/system-requirements/#optional-dependencies

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| useJAIImageRendering | boolean | is it necessary to use JAI. |

### skipHarfBuzzNativeLib() {#skipHarfBuzzNativeLib}
```
public static void skipHarfBuzzNativeLib()
```


Skip loading and use harfbuzz-shaping-engine-dll.dll libraries. By default, native libraries are loaded.

### skipWinNativeLib() {#skipWinNativeLib}
```
public static void skipWinNativeLib()
```


Skip loading and use WindowsNativeCall\_x86|\_x64.dll libraries. By default, native libraries are loaded.

