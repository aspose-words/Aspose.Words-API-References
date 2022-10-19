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
| [load(String fileName)](#load-java.lang.String-) | Loads font fallback settings from XML file. |
| [load(InputStream stream)](#load-java.io.InputStream-) |  |
| [loadMsOfficeFallbackSettings()](#loadMsOfficeFallbackSettings--) | Loads predefined fallback settings which mimics the Microsoft Word fallback and uses Microsoft office fonts. |
| [loadNotoFallbackSettings()](#loadNotoFallbackSettings--) | Loads predefined fallback settings which uses Google Noto fonts. |
| [save(OutputStream outputStream)](#save-java.io.OutputStream-) |  |
| [save(String fileName)](#save-java.lang.String-) | Saves the current fallback settings to file. |
| [buildAutomatic()](#buildAutomatic--) | Automatically builds the fallback settings by scanning available fonts. |
### load(String fileName) {#load-java.lang.String-}
```
public void load(String fileName)
```


Loads font fallback settings from XML file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Input file name. |

### load(InputStream stream) {#load-java.io.InputStream-}
```
public void load(InputStream stream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |

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

### buildAutomatic() {#buildAutomatic--}
```
public void buildAutomatic()
```


Automatically builds the fallback settings by scanning available fonts. This method may produce non-optimal fallback settings. Fonts are checked by [ Unicode Character Range ][Unicode Character Range] fields and not by the actual glyphs presence. Also Unicode ranges are checked individually and several ranges related to single language/script may use different fallback fonts.


[Unicode Character Range]: https://docs.microsoft.com/en-us/typography/opentype/spec/os2#ur

