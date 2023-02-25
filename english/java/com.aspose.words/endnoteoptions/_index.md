---
title: EndnoteOptions
linktitle: EndnoteOptions
second_title: Aspose.Words for Java API Reference
description: Represents the endnote numbering options for a document or section in Java.
type: docs
weight: 147
url: /java/com.aspose.words/endnoteoptions/
---

**Inheritance:**
java.lang.Object
```
public class EndnoteOptions
```

Represents the endnote numbering options for a document or section.

To learn more, visit the [ Working with Footnote and Endnote ][Working with Footnote and Endnote] documentation article.


[Working with Footnote and Endnote]: https://docs.aspose.com/words/java/working-with-footnote-and-endnote/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getLocation()](#getLocation) |  |
| [getNumberStyle()](#getNumberStyle) | Specifies the number format for automatically numbered endnotes. |
| [getPosition()](#getPosition) | Specifies the endnotes position. |
| [getRestartRule()](#getRestartRule) | Determines when automatic numbering restarts. |
| [getStartNumber()](#getStartNumber) | Specifies the starting number or character for the first automatically numbered endnotes. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setLocation(int value)](#setLocation-int) |  |
| [setNumberStyle(int value)](#setNumberStyle-int) | Specifies the number format for automatically numbered endnotes. |
| [setPosition(int value)](#setPosition-int) | Specifies the endnotes position. |
| [setRestartRule(int value)](#setRestartRule-int) | Determines when automatic numbering restarts. |
| [setStartNumber(int value)](#setStartNumber-int) | Specifies the starting number or character for the first automatically numbered endnotes. |
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


Specifies the number format for automatically numbered endnotes.

Not all number styles are applicable for this property. For the list of applicable number styles see the Insert Footnote or Endnote dialog box in Microsoft Word. If you select a number style that is not applicable, Microsoft Word will revert to a default value.

**Returns:**
int - The corresponding  int  value. The returned value is one of [NumberStyle](../../com.aspose.words/numberstyle/) constants.
### getPosition() {#getPosition}
```
public int getPosition()
```


Specifies the endnotes position.

**Returns:**
int - The corresponding  int  value. The returned value is one of [EndnotePosition](../../com.aspose.words/endnoteposition/) constants.
### getRestartRule() {#getRestartRule}
```
public int getRestartRule()
```


Determines when automatic numbering restarts.

Not all values are applicable to endnotes. To ascertain which values are applicable see [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule/).

**Returns:**
int - The corresponding  int  value. The returned value is one of [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule/) constants.
### getStartNumber() {#getStartNumber}
```
public int getStartNumber()
```


Specifies the starting number or character for the first automatically numbered endnotes.

This property has effect only when [getRestartRule()](../../com.aspose.words/endnoteoptions/\#getRestartRule) / [setRestartRule(int)](../../com.aspose.words/endnoteoptions/\#setRestartRule-int) is set to [FootnoteNumberingRule.CONTINUOUS](../../com.aspose.words/footnotenumberingrule/\#CONTINUOUS).

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


Specifies the number format for automatically numbered endnotes.

Not all number styles are applicable for this property. For the list of applicable number styles see the Insert Footnote or Endnote dialog box in Microsoft Word. If you select a number style that is not applicable, Microsoft Word will revert to a default value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [NumberStyle](../../com.aspose.words/numberstyle/) constants. |

### setPosition(int value) {#setPosition-int}
```
public void setPosition(int value)
```


Specifies the endnotes position.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [EndnotePosition](../../com.aspose.words/endnoteposition/) constants. |

### setRestartRule(int value) {#setRestartRule-int}
```
public void setRestartRule(int value)
```


Determines when automatic numbering restarts.

Not all values are applicable to endnotes. To ascertain which values are applicable see [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule/) constants. |

### setStartNumber(int value) {#setStartNumber-int}
```
public void setStartNumber(int value)
```


Specifies the starting number or character for the first automatically numbered endnotes.

This property has effect only when [getRestartRule()](../../com.aspose.words/endnoteoptions/\#getRestartRule) / [setRestartRule(int)](../../com.aspose.words/endnoteoptions/\#setRestartRule-int) is set to [FootnoteNumberingRule.CONTINUOUS](../../com.aspose.words/footnotenumberingrule/\#CONTINUOUS).

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

