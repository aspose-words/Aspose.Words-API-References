---
title: TableSubstitutionRule
linktitle: TableSubstitutionRule
second_title: Aspose.Words for Java API Reference
description: Table font substitution rule in Java.
type: docs
weight: 560
url: /java/com.aspose.words/tablesubstitutionrule/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSubstitutionRule](../../com.aspose.words/fontsubstitutionrule/)
```
public class TableSubstitutionRule extends FontSubstitutionRule
```

Table font substitution rule.

To learn more, visit the [ Working with Fonts ][Working with Fonts] documentation article.

This rule defines the list of substitute font names to be used if the original font is not available. Substitutes will be checked for the font name and the [FontInfo.getAltName()](../../com.aspose.words/fontinfo/\#getAltName) / [FontInfo.setAltName(java.lang.String)](../../com.aspose.words/fontinfo/\#setAltName-java.lang.String) (if any).


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Methods

| Method | Description |
| --- | --- |
| [addSubstitutes(String originalFontName, String[] substituteFontNames)](#addSubstitutes-java.lang.String-java.lang.String...) | Adds substitute font names for given original font name. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getEnabled()](#getEnabled) | Specifies whether the rule is enabled or not. |
| [getSubstitutes(String originalFontName)](#getSubstitutes-java.lang.String) | Returns array containing substitute font names for the specified original font name. |
| [hashCode()](#hashCode) |  |
| [load(InputStream stream)](#load-java.io.InputStream) |  |
| [load(String fileName)](#load-java.lang.String) | Loads table substitution settings from XML file. |
| [loadAndroidSettings()](#loadAndroidSettings) | Loads predefined table substitution settings for Android platform. |
| [loadLinuxSettings()](#loadLinuxSettings) | Loads predefined table substitution settings for Linux platform. |
| [loadWindowsSettings()](#loadWindowsSettings) | Loads predefined table substitution settings for Windows platform. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [save(OutputStream outputStream)](#save-java.io.OutputStream) |  |
| [save(String fileName)](#save-java.lang.String) | Saves the current table substitution settings to file. |
| [setEnabled(boolean value)](#setEnabled-boolean) | Specifies whether the rule is enabled or not. |
| [setSubstitutes(String originalFontName, String[] substituteFontNames)](#setSubstitutes-java.lang.String-java.lang.String...) | Override substitute font names for given original font name. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### addSubstitutes(String originalFontName, String[] substituteFontNames) {#addSubstitutes-java.lang.String-java.lang.String...}
```
public void addSubstitutes(String originalFontName, String[] substituteFontNames)
```


Adds substitute font names for given original font name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| originalFontName | java.lang.String | Original font name. |
| substituteFontNames | java.lang.String[] | List of alternative font names. |

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
### getEnabled() {#getEnabled}
```
public boolean getEnabled()
```


Specifies whether the rule is enabled or not.

**Returns:**
boolean - The corresponding  boolean  value.
### getSubstitutes(String originalFontName) {#getSubstitutes-java.lang.String}
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
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### load(InputStream stream) {#load-java.io.InputStream}
```
public void load(InputStream stream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### load(String fileName) {#load-java.lang.String}
```
public void load(String fileName)
```


Loads table substitution settings from XML file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Input file name. |

### loadAndroidSettings() {#loadAndroidSettings}
```
public void loadAndroidSettings()
```


Loads predefined table substitution settings for Android platform.

### loadLinuxSettings() {#loadLinuxSettings}
```
public void loadLinuxSettings()
```


Loads predefined table substitution settings for Linux platform.

### loadWindowsSettings() {#loadWindowsSettings}
```
public void loadWindowsSettings()
```


Loads predefined table substitution settings for Windows platform.

### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### save(OutputStream outputStream) {#save-java.io.OutputStream}
```
public void save(OutputStream outputStream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String}
```
public void save(String fileName)
```


Saves the current table substitution settings to file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Output file name. |

### setEnabled(boolean value) {#setEnabled-boolean}
```
public void setEnabled(boolean value)
```


Specifies whether the rule is enabled or not.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setSubstitutes(String originalFontName, String[] substituteFontNames) {#setSubstitutes-java.lang.String-java.lang.String...}
```
public void setSubstitutes(String originalFontName, String[] substituteFontNames)
```


Override substitute font names for given original font name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| originalFontName | java.lang.String | Original font name. |
| substituteFontNames | java.lang.String[] | List of alternative font names. |

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

