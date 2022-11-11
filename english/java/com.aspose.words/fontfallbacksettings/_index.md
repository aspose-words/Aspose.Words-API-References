---
title: FontFallbackSettings
second_title: Aspose.Words for Java API Reference
description: Specifies font fallback mechanism settings.
type: docs
weight: 277
url: /java/com.aspose.words/fontfallbacksettings/
---

**Inheritance:**
java.lang.Object
```
public class FontFallbackSettings
```

Specifies font fallback mechanism settings.

To learn more, visit the **Working with Fonts** documentation article.

By default fallback settings are initialized with predefined settings which mimics the Microsoft Word fallback.
## Methods

| Method | Description |
| --- | --- |
| [buildAutomatic()](#buildAutomatic--) | Automatically builds the fallback settings by scanning available fonts. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [hashCode()](#hashCode--) |  |
| [load(InputStream stream)](#load-java.io.InputStream-) |  |
| [load(String fileName)](#load-java.lang.String-) | Loads font fallback settings from XML file. |
| [loadMsOfficeFallbackSettings()](#loadMsOfficeFallbackSettings--) | Loads predefined fallback settings which mimics the Microsoft Word fallback and uses Microsoft office fonts. |
| [loadNotoFallbackSettings()](#loadNotoFallbackSettings--) | Loads predefined fallback settings which uses Google Noto fonts. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [save(OutputStream outputStream)](#save-java.io.OutputStream-) |  |
| [save(String fileName)](#save-java.lang.String-) | Saves the current fallback settings to file. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### buildAutomatic() {#buildAutomatic--}
```
public void buildAutomatic()
```


Automatically builds the fallback settings by scanning available fonts. This method may produce non-optimal fallback settings. Fonts are checked by [ Unicode Character Range ][Unicode Character Range] fields and not by the actual glyphs presence. Also Unicode ranges are checked individually and several ranges related to single language/script may use different fallback fonts.


[Unicode Character Range]: https://docs.microsoft.com/en-us/typography/opentype/spec/os2#ur

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### load(InputStream stream) {#load-java.io.InputStream-}
```
public void load(InputStream stream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### load(String fileName) {#load-java.lang.String-}
```
public void load(String fileName)
```


Loads font fallback settings from XML file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Input file name. |

### loadMsOfficeFallbackSettings() {#loadMsOfficeFallbackSettings--}
```
public void loadMsOfficeFallbackSettings()
```


Loads predefined fallback settings which mimics the Microsoft Word fallback and uses Microsoft office fonts.

### loadNotoFallbackSettings() {#loadNotoFallbackSettings--}
```
public void loadNotoFallbackSettings()
```


Loads predefined fallback settings which uses Google Noto fonts.

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### save(OutputStream outputStream) {#save-java.io.OutputStream-}
```
public void save(OutputStream outputStream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String-}
```
public void save(String fileName)
```


Saves the current fallback settings to file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Output file name. |

### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

