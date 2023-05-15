---
title: NativeLibSettings
linktitle: NativeLibSettings
second_title: Aspose.Words for Java
description: This class helps to set various options such as temporary folder for Aspose.Words native libraries and whether native libraries should be loaded and used in Java.
type: docs
weight: 417
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
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getTmpDirectoryPath()](#getTmpDirectoryPath) | Return the path to the temporary directory of native libraries. |
| [hashCode()](#hashCode) |  |
| [isHarfBuzzNativeLibLoaded()](#isHarfBuzzNativeLibLoaded) | Returns `true` if HarfBuzz libraries is loaded. |
| [isWinNativeLibLoaded()](#isWinNativeLibLoaded) | Returns `true` if WindowsNativeCall libraries is loaded. |
| [loadHarfBuzzNativeLib()](#loadHarfBuzzNativeLib) | Sets to load and use harfbuzz-shaping-engine-dll.dll libraries. |
| [loadWinNativeLib()](#loadWinNativeLib) | Sets to load and use WindowsNativeCall\_x86|\_x64.dll libraries. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setTmpDirectoryPath(String path)](#setTmpDirectoryPath-java.lang.String) | Specifies the path to the temporary directory of native libraries. |
| [skipHarfBuzzNativeLib()](#skipHarfBuzzNativeLib) | Skip loading and use harfbuzz-shaping-engine-dll.dll libraries. |
| [skipWinNativeLib()](#skipWinNativeLib) | Skip loading and use WindowsNativeCall\_x86|\_x64.dll libraries. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getTmpDirectoryPath() {#getTmpDirectoryPath}
```
public static String getTmpDirectoryPath()
```


Return the path to the temporary directory of native libraries.

**Returns:**
java.lang.String
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
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

### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




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

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

