---
title: TxtSaveOptions
second_title: Aspose.Words for Java API Reference
description: Can be used to specify additional options when saving a document into the  format.
type: docs
weight: 585
url: /java/com.aspose.words/txtsaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions), [com.aspose.words.TxtSaveOptionsBase](../../com.aspose.words/txtsaveoptionsbase)
```
public class TxtSaveOptions extends TxtSaveOptionsBase
```

Can be used to specify additional options when saving a document into the [SaveFormat.TEXT](../../com.aspose.words/saveformat\#TEXT) format.

To learn more, visit the **Specify Save Options** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getSaveFormat()](#getSaveFormat--) | Specifies the format in which the document will be saved if this save options object is used. |
| [setSaveFormat(int value)](#setSaveFormat-int-) | Specifies the format in which the document will be saved if this save options object is used. |
| [getSimplifyListLabels()](#getSimplifyListLabels--) | Specifies whether the program should simplify list labels in case of complex label formatting not being adequately represented by plain text. |
| [setSimplifyListLabels(boolean value)](#setSimplifyListLabels-boolean-) | Specifies whether the program should simplify list labels in case of complex label formatting not being adequately represented by plain text. |
| [getAddBidiMarks()](#getAddBidiMarks--) | Specifies whether to add bi-directional marks before each BiDi run when exporting in plain text format. |
| [setAddBidiMarks(boolean value)](#setAddBidiMarks-boolean-) | Specifies whether to add bi-directional marks before each BiDi run when exporting in plain text format. |
| [getListIndentation()](#getListIndentation--) | Gets a ListIndentation object that specifies how many and which character to use for indentation of list levels. |
| [getPreserveTableLayout()](#getPreserveTableLayout--) | Specifies whether the program should attempt to preserve layout of tables when saving in the plain text format. |
| [setPreserveTableLayout(boolean value)](#setPreserveTableLayout-boolean-) | Specifies whether the program should attempt to preserve layout of tables when saving in the plain text format. |
| [getMaxCharactersPerLine()](#getMaxCharactersPerLine--) | Gets an integer value that specifies the maximum number of characters per one line. |
| [setMaxCharactersPerLine(int value)](#setMaxCharactersPerLine-int-) | Sets an integer value that specifies the maximum number of characters per one line. |
### getSaveFormat() {#getSaveFormat--}
```
public int getSaveFormat()
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.TEXT](../../com.aspose.words/saveformat\#TEXT).

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat) constants.
### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.TEXT](../../com.aspose.words/saveformat\#TEXT).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat) constants. |

### getSimplifyListLabels() {#getSimplifyListLabels--}
```
public boolean getSimplifyListLabels()
```


Specifies whether the program should simplify list labels in case of complex label formatting not being adequately represented by plain text.

If set to **true**, numbered list labels are written in simple numeric format and itemized list labels as simple ASCII characters. The default value is **false**.

**Returns:**
boolean - The corresponding  boolean  value.
### setSimplifyListLabels(boolean value) {#setSimplifyListLabels-boolean-}
```
public void setSimplifyListLabels(boolean value)
```


Specifies whether the program should simplify list labels in case of complex label formatting not being adequately represented by plain text.

If set to **true**, numbered list labels are written in simple numeric format and itemized list labels as simple ASCII characters. The default value is **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getAddBidiMarks() {#getAddBidiMarks--}
```
public boolean getAddBidiMarks()
```


Specifies whether to add bi-directional marks before each BiDi run when exporting in plain text format.

The default value is **false**.

**Returns:**
boolean - The corresponding  boolean  value.
### setAddBidiMarks(boolean value) {#setAddBidiMarks-boolean-}
```
public void setAddBidiMarks(boolean value)
```


Specifies whether to add bi-directional marks before each BiDi run when exporting in plain text format.

The default value is **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getListIndentation() {#getListIndentation--}
```
public TxtListIndentation getListIndentation()
```


Gets a ListIndentation object that specifies how many and which character to use for indentation of list levels. By default it is zero count of character '\\0', that means no indentation.

**Returns:**
[TxtListIndentation](../../com.aspose.words/txtlistindentation) - A ListIndentation object that specifies how many and which character to use for indentation of list levels.
### getPreserveTableLayout() {#getPreserveTableLayout--}
```
public boolean getPreserveTableLayout()
```


Specifies whether the program should attempt to preserve layout of tables when saving in the plain text format. The default value is **false**.

**Returns:**
boolean - The corresponding  boolean  value.
### setPreserveTableLayout(boolean value) {#setPreserveTableLayout-boolean-}
```
public void setPreserveTableLayout(boolean value)
```


Specifies whether the program should attempt to preserve layout of tables when saving in the plain text format. The default value is **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getMaxCharactersPerLine() {#getMaxCharactersPerLine--}
```
public int getMaxCharactersPerLine()
```


Gets an integer value that specifies the maximum number of characters per one line. The default value is 0, that means no limit.

**Returns:**
int - An integer value that specifies the maximum number of characters per one line.
### setMaxCharactersPerLine(int value) {#setMaxCharactersPerLine-int-}
```
public void setMaxCharactersPerLine(int value)
```


Sets an integer value that specifies the maximum number of characters per one line. The default value is 0, that means no limit.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | An integer value that specifies the maximum number of characters per one line. |

