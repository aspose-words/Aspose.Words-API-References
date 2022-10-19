---
title: EndnoteOptions
second_title: Aspose.Words for Java API Reference
description: Represents the endnote numbering options for a document or section.
type: docs
weight: 146
url: /java/com.aspose.words/endnoteoptions/
---

**Inheritance:**
java.lang.Object
```
public class EndnoteOptions
```

Represents the endnote numbering options for a document or section.

To learn more, visit the **Working with Footnote and Endnote** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getPosition()](#getPosition--) | Specifies the endnotes position. |
| [setPosition(int value)](#setPosition-int-) | Specifies the endnotes position. |
| [getNumberStyle()](#getNumberStyle--) | Specifies the number format for automatically numbered endnotes. |
| [setNumberStyle(int value)](#setNumberStyle-int-) | Specifies the number format for automatically numbered endnotes. |
| [getStartNumber()](#getStartNumber--) | Specifies the starting number or character for the first automatically numbered endnotes. |
| [setStartNumber(int value)](#setStartNumber-int-) | Specifies the starting number or character for the first automatically numbered endnotes. |
| [getRestartRule()](#getRestartRule--) | Determines when automatic numbering restarts. |
| [setRestartRule(int value)](#setRestartRule-int-) | Determines when automatic numbering restarts. |
| [getLocation()](#getLocation--) |  |
| [setLocation(int value)](#setLocation-int-) |  |
### getPosition() {#getPosition--}
```
public int getPosition()
```


Specifies the endnotes position.

**Returns:**
int - The corresponding  int  value. The returned value is one of [EndnotePosition](../../com.aspose.words/endnoteposition) constants.
### setPosition(int value) {#setPosition-int-}
```
public void setPosition(int value)
```


Specifies the endnotes position.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [EndnotePosition](../../com.aspose.words/endnoteposition) constants. |

### getNumberStyle() {#getNumberStyle--}
```
public int getNumberStyle()
```


Specifies the number format for automatically numbered endnotes.

Not all number styles are applicable for this property. For the list of applicable number styles see the Insert Footnote or Endnote dialog box in Microsoft Word. If you select a number style that is not applicable, Microsoft Word will revert to a default value.

**Returns:**
int - The corresponding  int  value. The returned value is one of [NumberStyle](../../com.aspose.words/numberstyle) constants.
### setNumberStyle(int value) {#setNumberStyle-int-}
```
public void setNumberStyle(int value)
```


Specifies the number format for automatically numbered endnotes.

Not all number styles are applicable for this property. For the list of applicable number styles see the Insert Footnote or Endnote dialog box in Microsoft Word. If you select a number style that is not applicable, Microsoft Word will revert to a default value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [NumberStyle](../../com.aspose.words/numberstyle) constants. |

### getStartNumber() {#getStartNumber--}
```
public int getStartNumber()
```


Specifies the starting number or character for the first automatically numbered endnotes.

This property has effect only when [getRestartRule()](../../com.aspose.words/endnoteoptions\#getRestartRule--) / [setRestartRule(int)](../../com.aspose.words/endnoteoptions\#setRestartRule-int-) is set to [FootnoteNumberingRule.CONTINUOUS](../../com.aspose.words/footnotenumberingrule\#CONTINUOUS).

**Returns:**
int - The corresponding  int  value.
### setStartNumber(int value) {#setStartNumber-int-}
```
public void setStartNumber(int value)
```


Specifies the starting number or character for the first automatically numbered endnotes.

This property has effect only when [getRestartRule()](../../com.aspose.words/endnoteoptions\#getRestartRule--) / [setRestartRule(int)](../../com.aspose.words/endnoteoptions\#setRestartRule-int-) is set to [FootnoteNumberingRule.CONTINUOUS](../../com.aspose.words/footnotenumberingrule\#CONTINUOUS).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### getRestartRule() {#getRestartRule--}
```
public int getRestartRule()
```


Determines when automatic numbering restarts.

Not all values are applicable to endnotes. To ascertain which values are applicable see [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule).

**Returns:**
int - The corresponding  int  value. The returned value is one of [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule) constants.
### setRestartRule(int value) {#setRestartRule-int-}
```
public void setRestartRule(int value)
```


Determines when automatic numbering restarts.

Not all values are applicable to endnotes. To ascertain which values are applicable see [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule) constants. |

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

