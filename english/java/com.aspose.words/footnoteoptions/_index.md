---
title: FootnoteOptions
second_title: Aspose.Words for Java API Reference
description: Represents the footnote numbering options for a document or section.
type: docs
weight: 293
url: /java/com.aspose.words/footnoteoptions/
---

**Inheritance:**
java.lang.Object
```
public class FootnoteOptions
```

Represents the footnote numbering options for a document or section.

To learn more, visit the **Working with Footnote and Endnote** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getPosition()](#getPosition--) | Specifies the footnotes position. |
| [setPosition(int value)](#setPosition-int-) | Specifies the footnotes position. |
| [getNumberStyle()](#getNumberStyle--) | Specifies the number format for automatically numbered footnotes. |
| [setNumberStyle(int value)](#setNumberStyle-int-) | Specifies the number format for automatically numbered footnotes. |
| [getStartNumber()](#getStartNumber--) | Specifies the starting number or character for the first automatically numbered footnotes. |
| [setStartNumber(int value)](#setStartNumber-int-) | Specifies the starting number or character for the first automatically numbered footnotes. |
| [getRestartRule()](#getRestartRule--) | Determines when automatic numbering restarts. |
| [setRestartRule(int value)](#setRestartRule-int-) | Determines when automatic numbering restarts. |
| [getColumns()](#getColumns--) | Specifies the number of columns with which the footnotes area is formatted. |
| [setColumns(int value)](#setColumns-int-) | Specifies the number of columns with which the footnotes area is formatted. |
| [getLocation()](#getLocation--) |  |
| [setLocation(int value)](#setLocation-int-) |  |
### getPosition() {#getPosition--}
```
public int getPosition()
```


Specifies the footnotes position.

**Returns:**
int - The corresponding  int  value. The returned value is one of [FootnotePosition](../../com.aspose.words/footnoteposition) constants.
### setPosition(int value) {#setPosition-int-}
```
public void setPosition(int value)
```


Specifies the footnotes position.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [FootnotePosition](../../com.aspose.words/footnoteposition) constants. |

### getNumberStyle() {#getNumberStyle--}
```
public int getNumberStyle()
```


Specifies the number format for automatically numbered footnotes.

Not all number styles are applicable for this property. For the list of applicable number styles see the Insert Footnote or Endnote dialog box in Microsoft Word. If you select a number style that is not applicable, Microsoft Word will revert to a default value.

**Returns:**
int - The corresponding  int  value. The returned value is one of [NumberStyle](../../com.aspose.words/numberstyle) constants.
### setNumberStyle(int value) {#setNumberStyle-int-}
```
public void setNumberStyle(int value)
```


Specifies the number format for automatically numbered footnotes.

Not all number styles are applicable for this property. For the list of applicable number styles see the Insert Footnote or Endnote dialog box in Microsoft Word. If you select a number style that is not applicable, Microsoft Word will revert to a default value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [NumberStyle](../../com.aspose.words/numberstyle) constants. |

### getStartNumber() {#getStartNumber--}
```
public int getStartNumber()
```


Specifies the starting number or character for the first automatically numbered footnotes.

This property has effect only when [getRestartRule()](../../com.aspose.words/footnoteoptions\#getRestartRule--) / [setRestartRule(int)](../../com.aspose.words/footnoteoptions\#setRestartRule-int-) is set to [FootnoteNumberingRule.CONTINUOUS](../../com.aspose.words/footnotenumberingrule\#CONTINUOUS).

**Returns:**
int - The corresponding  int  value.
### setStartNumber(int value) {#setStartNumber-int-}
```
public void setStartNumber(int value)
```


Specifies the starting number or character for the first automatically numbered footnotes.

This property has effect only when [getRestartRule()](../../com.aspose.words/footnoteoptions\#getRestartRule--) / [setRestartRule(int)](../../com.aspose.words/footnoteoptions\#setRestartRule-int-) is set to [FootnoteNumberingRule.CONTINUOUS](../../com.aspose.words/footnotenumberingrule\#CONTINUOUS).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### getRestartRule() {#getRestartRule--}
```
public int getRestartRule()
```


Determines when automatic numbering restarts.

**Returns:**
int - The corresponding  int  value. The returned value is one of [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule) constants.
### setRestartRule(int value) {#setRestartRule-int-}
```
public void setRestartRule(int value)
```


Determines when automatic numbering restarts.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule) constants. |

### getColumns() {#getColumns--}
```
public int getColumns()
```


Specifies the number of columns with which the footnotes area is formatted. If this property has the value of 0, the footnotes area is formatted with a number of columns based on the number of columns on the displayed page. The default value is 0.

**Returns:**
int - The corresponding  int  value.
### setColumns(int value) {#setColumns-int-}
```
public void setColumns(int value)
```


Specifies the number of columns with which the footnotes area is formatted. If this property has the value of 0, the footnotes area is formatted with a number of columns based on the number of columns on the displayed page. The default value is 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### getLocation() {#getLocation--}
```
public int getLocation()
```




**Returns:**
int
### setLocation(int value) {#setLocation-int-}
```
public void setLocation(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

