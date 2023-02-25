---
title: FontSettings
linktitle: FontSettings
second_title: Aspose.Words for Java API Reference
description: Specifies font settings for a document in Java.
type: docs
weight: 288
url: /java/com.aspose.words/fontsettings/
---

**Inheritance:**
java.lang.Object
```
public class FontSettings
```

Specifies font settings for a document.

To learn more, visit the [ Working with Fonts ][Working with Fonts] documentation article.

Aspose.Words uses font settings to resolve the fonts in the document. Fonts are resolved mostly when building document layout or rendering to fixed page formats. But when loading some formats, Aspose.Words also may require to resolve the fonts. For example, when loading HTML documents Aspose.Words may resolve the fonts to perform font fallback. So it is recommended that you set the font settings in [LoadOptions](../../com.aspose.words/loadoptions/) when loading the document. Or at least before building the layout or rendering the document to the fixed-page format.

By default all documents uses single static font settings instance. It could be accessed by [getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance) property.

Changing font settings is safe at any time from any thread. But it is recommended that you do not change the font settings while processing some documents which uses this settings. This can lead to the fact that the same font will be resolved differently in different parts of the document.


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Constructors

| Constructor | Description |
| --- | --- |
| [FontSettings()](#FontSettings) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getDefaultInstance()](#getDefaultInstance) | Static default font settings. |
| [getFallbackSettings()](#getFallbackSettings) | Settings related to font fallback mechanism. |
| [getFontsSources()](#getFontsSources) | Gets a copy of the array that contains the list of sources where Aspose.Words looks for TrueType fonts. |
| [getSubstitutionSettings()](#getSubstitutionSettings) | Settings related to font substitution mechanism. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [resetFontSources()](#resetFontSources) | Resets the fonts sources to the system default. |
| [saveSearchCache(OutputStream outputStream)](#saveSearchCache-java.io.OutputStream) |  |
| [setFontsFolder(String fontFolder, boolean recursive)](#setFontsFolder-java.lang.String-boolean) | Sets the folder where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts. |
| [setFontsFolders(String[] fontsFolders, boolean recursive)](#setFontsFolders-java.lang.String---boolean) | Sets the folders where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts. |
| [setFontsSources(FontSourceBase[] sources)](#setFontsSources-com.aspose.words.FontSourceBase) | Sets the sources where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts. |
| [setFontsSources(FontSourceBase[] sources, InputStream cacheInputStream)](#setFontsSources-com.aspose.words.FontSourceBase---java.io.InputStream) |  |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### FontSettings() {#FontSettings}
```
public FontSettings()
```


Initializes a new instance of this class.

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
### getDefaultInstance() {#getDefaultInstance}
```
public static FontSettings getDefaultInstance()
```


Static default font settings. This instance is used by default in a document unless [Document.getFontSettings()](../../com.aspose.words/document/\#getFontSettings) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document/\#setFontSettings-com.aspose.words.FontSettings) is specified.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getFallbackSettings() {#getFallbackSettings}
```
public FontFallbackSettings getFallbackSettings()
```


Settings related to font fallback mechanism.

**Returns:**
[FontFallbackSettings](../../com.aspose.words/fontfallbacksettings/) - The corresponding [FontFallbackSettings](../../com.aspose.words/fontfallbacksettings/) value.
### getFontsSources() {#getFontsSources}
```
public FontSourceBase[] getFontsSources()
```


Gets a copy of the array that contains the list of sources where Aspose.Words looks for TrueType fonts.

The returned value is a copy of the data that Aspose.Words uses. If you change the entries in the returned array, it will have no effect on document rendering. To specify new font sources use the [setFontsSources(com.aspose.words.FontSourceBase[])](../../com.aspose.words/fontsettings/\#setFontsSources-com.aspose.words.FontSourceBase) method.

**Returns:**
com.aspose.words.FontSourceBase[] - A copy of the current font sources.
### getSubstitutionSettings() {#getSubstitutionSettings}
```
public FontSubstitutionSettings getSubstitutionSettings()
```


Settings related to font substitution mechanism.

**Returns:**
[FontSubstitutionSettings](../../com.aspose.words/fontsubstitutionsettings/) - The corresponding [FontSubstitutionSettings](../../com.aspose.words/fontsubstitutionsettings/) value.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### resetFontSources() {#resetFontSources}
```
public void resetFontSources()
```


Resets the fonts sources to the system default.

### saveSearchCache(OutputStream outputStream) {#saveSearchCache-java.io.OutputStream}
```
public void saveSearchCache(OutputStream outputStream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |

### setFontsFolder(String fontFolder, boolean recursive) {#setFontsFolder-java.lang.String-boolean}
```
public void setFontsFolder(String fontFolder, boolean recursive)
```


Sets the folder where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts. This is a shortcut to [setFontsFolders(java.lang.String[], boolean)](../../com.aspose.words/fontsettings/\#setFontsFolders-java.lang.String----boolean) for setting only one font directory.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontFolder | java.lang.String | The folder that contains TrueType fonts. |
| recursive | boolean | True to scan the specified folders for fonts recursively. |

### setFontsFolders(String[] fontsFolders, boolean recursive) {#setFontsFolders-java.lang.String---boolean}
```
public void setFontsFolders(String[] fontsFolders, boolean recursive)
```


Sets the folders where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts.

By default, Aspose.Words looks for fonts installed to the system.

Setting this property resets the cache of all previously loaded fonts.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontsFolders | java.lang.String[] | An array of folders that contain TrueType fonts. |
| recursive | boolean | True to scan the specified folders for fonts recursively. |

### setFontsSources(FontSourceBase[] sources) {#setFontsSources-com.aspose.words.FontSourceBase}
```
public void setFontsSources(FontSourceBase[] sources)
```


Sets the sources where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts.

By default, Aspose.Words looks for fonts installed to the system.

Setting this property resets the cache of all previously loaded fonts.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sources | [FontSourceBase\[\]](../../com.aspose.words/fontsourcebase/) | An array of sources that contain TrueType fonts. |

### setFontsSources(FontSourceBase[] sources, InputStream cacheInputStream) {#setFontsSources-com.aspose.words.FontSourceBase---java.io.InputStream}
```
public void setFontsSources(FontSourceBase[] sources, InputStream cacheInputStream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sources | [FontSourceBase\[\]](../../com.aspose.words/fontsourcebase/) |  |
| cacheInputStream | java.io.InputStream |  |

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

