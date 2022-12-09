---
title: FootnoteOptions
second_title: Aspose.Words for Java API Reference
description: Represents the footnote numbering options for a document or section.
type: docs
weight: 295
url: /java/com.aspose.words/footnoteoptions/
---

**Inheritance:**
java.lang.Object
```
public class FootnoteOptions
```

Represents the footnote numbering options for a document or section.

To learn more, visit the [ Working with Footnote and Endnote ][Working with Footnote and Endnote] documentation article.


[Working with Footnote and Endnote]: https://docs.aspose.com/words/java/working-with-footnote-and-endnote/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getColumns()](#getColumns) | Specifies the number of columns with which the footnotes area is formatted. |
| [getLocation()](#getLocation) |  |
| [getNumberStyle()](#getNumberStyle) | Specifies the number format for automatically numbered footnotes. |
| [getPosition()](#getPosition) | Specifies the footnotes position. |
| [getRestartRule()](#getRestartRule) | Determines when automatic numbering restarts. |
| [getStartNumber()](#getStartNumber) | Specifies the starting number or character for the first automatically numbered footnotes. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setColumns(int value)](#setColumns-int) | Specifies the number of columns with which the footnotes area is formatted. |
| [setLocation(int value)](#setLocation-int) |  |
| [setNumberStyle(int value)](#setNumberStyle-int) | Specifies the number format for automatically numbered footnotes. |
| [setPosition(int value)](#setPosition-int) | Specifies the footnotes position. |
| [setRestartRule(int value)](#setRestartRule-int) | Determines when automatic numbering restarts. |
| [setStartNumber(int value)](#setStartNumber-int) | Specifies the starting number or character for the first automatically numbered footnotes. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
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
### getColumns() {#getColumns}
```
public int getColumns()
```


Specifies the number of columns with which the footnotes area is formatted. If this property has the value of 0, the footnotes area is formatted with a number of columns based on the number of columns on the displayed page. The default value is 0.

**Returns:**
int - The corresponding  int  value.
### getLocation() {#getLocation}
```
public int getLocation()
```




**Returns:**
int
### getNumberStyle() {#getNumberStyle}
```
public int getNumberStyle()
```


Specifies the number format for automatically numbered footnotes.

Not all number styles are applicable for this property. For the list of applicable number styles see the Insert Footnote or Endnote dialog box in Microsoft Word. If you select a number style that is not applicable, Microsoft Word will revert to a default value.

**Returns:**
int - The corresponding  int  value. The returned value is one of [NumberStyle](../../com.aspose.words/numberstyle) constants.
### getPosition() {#getPosition}
```
public int getPosition()
```


Specifies the footnotes position.

**Returns:**
int - The corresponding  int  value. The returned value is one of [FootnotePosition](../../com.aspose.words/footnoteposition) constants.
### getRestartRule() {#getRestartRule}
```
public int getRestartRule()
```


Determines when automatic numbering restarts.

**Returns:**
int - The corresponding  int  value. The returned value is one of [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule) constants.
### getStartNumber() {#getStartNumber}
```
public int getStartNumber()
```


Specifies the starting number or character for the first automatically numbered footnotes.

This property has effect only when [getRestartRule()](../../com.aspose.words/footnoteoptions\#getRestartRule) / [setRestartRule(int)](../../com.aspose.words/footnoteoptions\#setRestartRule-int) is set to [FootnoteNumberingRule.CONTINUOUS](../../com.aspose.words/footnotenumberingrule\#CONTINUOUS).

**Returns:**
int - The corresponding  int  value.
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




### setColumns(int value) {#setColumns-int}
```
public void setColumns(int value)
```


Specifies the number of columns with which the footnotes area is formatted. If this property has the value of 0, the footnotes area is formatted with a number of columns based on the number of columns on the displayed page. The default value is 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setLocation(int value) {#setLocation-int}
```
public void setLocation(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setNumberStyle(int value) {#setNumberStyle-int}
```
public void setNumberStyle(int value)
```


Specifies the number format for automatically numbered footnotes.

Not all number styles are applicable for this property. For the list of applicable number styles see the Insert Footnote or Endnote dialog box in Microsoft Word. If you select a number style that is not applicable, Microsoft Word will revert to a default value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [NumberStyle](../../com.aspose.words/numberstyle) constants. |

### setPosition(int value) {#setPosition-int}
```
public void setPosition(int value)
```


Specifies the footnotes position.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [FootnotePosition](../../com.aspose.words/footnoteposition) constants. |

### setRestartRule(int value) {#setRestartRule-int}
```
public void setRestartRule(int value)
```


Determines when automatic numbering restarts.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule) constants. |

### setStartNumber(int value) {#setStartNumber-int}
```
public void setStartNumber(int value)
```


Specifies the starting number or character for the first automatically numbered footnotes.

This property has effect only when [getRestartRule()](../../com.aspose.words/footnoteoptions\#getRestartRule) / [setRestartRule(int)](../../com.aspose.words/footnoteoptions\#setRestartRule-int) is set to [FootnoteNumberingRule.CONTINUOUS](../../com.aspose.words/footnotenumberingrule\#CONTINUOUS).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

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

