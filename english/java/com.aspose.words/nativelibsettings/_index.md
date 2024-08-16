---
title: NativeLibSettings
linktitle: NativeLibSettings
second_title: Aspose.Words for Java
description: This class helps to set various options such as temporary folder for Aspose.Words native libraries and whether native libraries should be loaded and used in Java.
type: docs
weight: 443
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
| [getTmpDirectoryPath()](#getTmpDirectoryPath) | Return the path to the temporary directory of native libraries. |
| [isHarfBuzzNativeLibLoaded()](#isHarfBuzzNativeLibLoaded) | Returns `true` if HarfBuzz libraries is loaded. |
| [isWinNativeLibLoaded()](#isWinNativeLibLoaded) | Returns `true` if WindowsNativeCall libraries is loaded. |
| [loadHarfBuzzNativeLib()](#loadHarfBuzzNativeLib) | Sets to load and use harfbuzz-shaping-engine-dll.dll libraries. |
| [loadWinNativeLib()](#loadWinNativeLib) | Sets to load and use WindowsNativeCall\_x86|\_x64.dll libraries. |
| [setTmpDirectoryPath(String path)](#setTmpDirectoryPath-java.lang.String) | Specifies the path to the temporary directory of native libraries. |
| [skipHarfBuzzNativeLib()](#skipHarfBuzzNativeLib) | Skip loading and use harfbuzz-shaping-engine-dll.dll libraries. |
| [skipWinNativeLib()](#skipWinNativeLib) | Skip loading and use WindowsNativeCall\_x86|\_x64.dll libraries. |
### getTmpDirectoryPath() {#getTmpDirectoryPath}
```
public static String getTmpDirectoryPath()
```


Return the path to the temporary directory of native libraries.

**Returns:**
java.lang.String
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

