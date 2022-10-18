---
title: TableSubstitutionRule
second_title: Aspose.Words for Java API Reference
description: Table font substitution rule.
type: docs
weight: 554
url: /java/com.aspose.words/tablesubstitutionrule/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSubstitutionRule](../../com.aspose.words/fontsubstitutionrule)
```
public class TableSubstitutionRule extends FontSubstitutionRule
```

Table font substitution rule.

To learn more, visit the **Working with Fonts** documentation article.

This rule defines the list of substitute font names to be used if the original font is not available. Substitutes will be checked for the font name and the [FontInfo.getAltName()](../../com.aspose.words/fontinfo\#getAltName--) / [FontInfo.setAltName(java.lang.String)](../../com.aspose.words/fontinfo\#setAltName-java.lang.String-) (if any).
## Methods

| Method | Description |
| --- | --- |
| [load(String fileName)](#load-java.lang.String-) | Loads table substitution settings from XML file. |
| [load(InputStream stream)](#load-java.io.InputStream-) |  |
| [loadWindowsSettings()](#loadWindowsSettings--) | Loads predefined table substitution settings for Windows platform. |
| [loadLinuxSettings()](#loadLinuxSettings--) | Loads predefined table substitution settings for Linux platform. |
| [loadAndroidSettings()](#loadAndroidSettings--) | Loads predefined table substitution settings for Linux platform. |
| [save(String fileName)](#save-java.lang.String-) | Saves the current table substitution settings to file. |
| [save(OutputStream outputStream)](#save-java.io.OutputStream-) |  |
| [getSubstitutes(String originalFontName)](#getSubstitutes-java.lang.String-) | Returns array containing substitute font names for the specified original font name. |
| [setSubstitutes(String originalFontName, String[] substituteFontNames)](#setSubstitutes-java.lang.String-java.lang.String...-) | Override substitute font names for given original font name. |
| [addSubstitutes(String originalFontName, String[] substituteFontNames)](#addSubstitutes-java.lang.String-java.lang.String...-) | Adds substitute font names for given original font name. |
### load(String fileName) {#load-java.lang.String-}
```
public void load(String fileName)
```


Loads table substitution settings from XML file.

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

### loadWindowsSettings() {#loadWindowsSettings--}
```
public void loadWindowsSettings()
```


Loads predefined table substitution settings for Windows platform.

### loadLinuxSettings() {#loadLinuxSettings--}
```
public void loadLinuxSettings()
```


Loads predefined table substitution settings for Linux platform.

### loadAndroidSettings() {#loadAndroidSettings--}
```
public void loadAndroidSettings()
```


Loads predefined table substitution settings for Linux platform.

### save(String fileName) {#save-java.lang.String-}
```
public void save(String fileName)
```


Saves the current table substitution settings to file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Output file name. |

### save(OutputStream outputStream) {#save-java.io.OutputStream-}
```
public void save(OutputStream outputStream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |

### getSubstitutes(String originalFontName) {#getSubstitutes-java.lang.String-}
```
public Iterable getSubstitutes(String originalFontName)
```


Returns array containing substitute font names for the specified original font name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| originalFontName | java.lang.String | Original font name. |

**Returns:**
java.lang.Iterable - List of alternative font names.
### setSubstitutes(String originalFontName, String[] substituteFontNames) {#setSubstitutes-java.lang.String-java.lang.String...-}
```
public void setSubstitutes(String originalFontName, String[] substituteFontNames)
```


Override substitute font names for given original font name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| originalFontName | java.lang.String | Original font name. |
| substituteFontNames | java.lang.String[] | List of alternative font names. |

### addSubstitutes(String originalFontName, String[] substituteFontNames) {#addSubstitutes-java.lang.String-java.lang.String...-}
```
public void addSubstitutes(String originalFontName, String[] substituteFontNames)
```


Adds substitute font names for given original font name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| originalFontName | java.lang.String | Original font name. |
| substituteFontNames | java.lang.String[] | List of alternative font names. |

