---
title: FolderFontSource
second_title: Aspose.Words for Java API Reference
description: Represents the folder that contains TrueType font files.
type: docs
weight: 274
url: /java/com.aspose.words/folderfontsource/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase)
```
public class FolderFontSource extends FontSourceBase
```

Represents the folder that contains TrueType font files.

To learn more, visit the **Working with Fonts** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [FolderFontSource(String folderPath, boolean scanSubfolders)](#FolderFontSource-java.lang.String-boolean-) | Ctor. |
| [FolderFontSource(String folderPath, boolean scanSubfolders, int priority)](#FolderFontSource-java.lang.String-boolean-int-) | Ctor. |
## Methods

| Method | Description |
| --- | --- |
| [getFolderPath()](#getFolderPath--) | Path to the folder. |
| [getScanSubfolders()](#getScanSubfolders--) | Determines whether or not to scan the subfolders. |
| [getType()](#getType--) | Returns the type of the font source. |
| [getFontDataInternal()](#getFontDataInternal--) |  |
### FolderFontSource(String folderPath, boolean scanSubfolders) {#FolderFontSource-java.lang.String-boolean-}
```
public FolderFontSource(String folderPath, boolean scanSubfolders)
```


Ctor.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| folderPath | java.lang.String | Path to folder. |
| scanSubfolders | boolean | Determines whether or not to scan subfolders. |

### FolderFontSource(String folderPath, boolean scanSubfolders, int priority) {#FolderFontSource-java.lang.String-boolean-int-}
```
public FolderFontSource(String folderPath, boolean scanSubfolders, int priority)
```


Ctor.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| folderPath | java.lang.String | Path to folder. |
| scanSubfolders | boolean | Determines whether or not to scan subfolders. |
| priority | int | Font source priority. See the [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase\#getPriority--) property description for more information. |

### getFolderPath() {#getFolderPath--}
```
public String getFolderPath()
```


Path to the folder.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getScanSubfolders() {#getScanSubfolders--}
```
public boolean getScanSubfolders()
```


Determines whether or not to scan the subfolders.

**Returns:**
boolean - The corresponding  boolean  value.
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
