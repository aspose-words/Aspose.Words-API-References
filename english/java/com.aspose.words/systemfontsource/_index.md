---
title: SystemFontSource
second_title: Aspose.Words for Java API Reference
description: Represents all TrueType fonts installed to the system.
type: docs
weight: 543
url: /java/com.aspose.words/systemfontsource/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase)
```
public class SystemFontSource extends FontSourceBase
```

Represents all TrueType fonts installed to the system.

To learn more, visit the **Working with Fonts** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [SystemFontSource()](#SystemFontSource--) | Ctor. |
| [SystemFontSource(int priority)](#SystemFontSource-int-) | Ctor. |
## Methods

| Method | Description |
| --- | --- |
| [getType()](#getType--) | Returns the type of the font source. |
| [getFontDataInternal()](#getFontDataInternal--) |  |
| [getSystemFontFolders()](#getSystemFontFolders--) | Returns system font folders or empty array if folders are not accessible. |
### SystemFontSource() {#SystemFontSource--}
```
public SystemFontSource()
```


Ctor.

### SystemFontSource(int priority) {#SystemFontSource-int-}
```
public SystemFontSource(int priority)
```


Ctor.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| priority | int | Font source priority. See the [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase\#getPriority--) property description for more information. |

### getType() {#getType--}
```
public int getType()
```


Returns the type of the font source.

**Returns:**
int - The type of the font source. The returned value is one of [FontSourceType](../../com.aspose.words/fontsourcetype) constants.
### getFontDataInternal() {#getFontDataInternal--}
```
public Iterable getFontDataInternal()
```




**Returns:**
java.lang.Iterable
### getSystemFontFolders() {#getSystemFontFolders--}
```
public static String[] getSystemFontFolders()
```


Returns system font folders or empty array if folders are not accessible. On some platforms Aspose.Words could search system fonts not only through folders but in other sources too. For example, on Windows platform Aspose.Words search fonts also in the registry.

**Returns:**
java.lang.String[]
