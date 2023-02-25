---
title: CompareOptions
linktitle: CompareOptions
second_title: Aspose.Words for Java API Reference
description: Allows to choose advanced options for document comparison operation in Java.
type: docs
weight: 82
url: /java/com.aspose.words/compareoptions/
---

**Inheritance:**
java.lang.Object
```
public class CompareOptions
```

Allows to choose advanced options for document comparison operation.

To learn more, visit the [ Compare Documents ][Compare Documents] documentation article.


[Compare Documents]: https://docs.aspose.com/words/java/compare-documents/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getCompareMoves()](#getCompareMoves) | Specifies whether to compare differences in **T:Aspose.Words.Revisions.MoveRevision** between the two documents. |
| [getGranularity()](#getGranularity) | Specifies whether changes are tracked by character or by word. |
| [getIgnoreCaseChanges()](#getIgnoreCaseChanges) | True indicates that documents comparison is case insensitive. |
| [getIgnoreComments()](#getIgnoreComments) | Specifies whether to compare differences in comments. |
| [getIgnoreDmlUniqueId()](#getIgnoreDmlUniqueId) | Specifies whether to ignore difference in DrawingML unique Id. |
| [getIgnoreFields()](#getIgnoreFields) | Specifies whether to compare differences in fields. |
| [getIgnoreFootnotes()](#getIgnoreFootnotes) | Specifies whether to compare differences in footnotes and endnotes. |
| [getIgnoreFormatting()](#getIgnoreFormatting) | True indicates that formatting is ignored. |
| [getIgnoreHeadersAndFooters()](#getIgnoreHeadersAndFooters) | True indicates that headers and footers content is ignored. |
| [getIgnoreTables()](#getIgnoreTables) | Specifies whether to compare the differences in data contained in tables. |
| [getIgnoreTextboxes()](#getIgnoreTextboxes) | Specifies whether to compare differences in the data contained within text boxes. |
| [getTarget()](#getTarget) | Specifies which document shall be used as a target during comparison. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setCompareMoves(boolean value)](#setCompareMoves-boolean) | Specifies whether to compare differences in **T:Aspose.Words.Revisions.MoveRevision** between the two documents. |
| [setGranularity(int value)](#setGranularity-int) | Specifies whether changes are tracked by character or by word. |
| [setIgnoreCaseChanges(boolean value)](#setIgnoreCaseChanges-boolean) | True indicates that documents comparison is case insensitive. |
| [setIgnoreComments(boolean value)](#setIgnoreComments-boolean) | Specifies whether to compare differences in comments. |
| [setIgnoreDmlUniqueId(boolean value)](#setIgnoreDmlUniqueId-boolean) | Specifies whether to ignore difference in DrawingML unique Id. |
| [setIgnoreFields(boolean value)](#setIgnoreFields-boolean) | Specifies whether to compare differences in fields. |
| [setIgnoreFootnotes(boolean value)](#setIgnoreFootnotes-boolean) | Specifies whether to compare differences in footnotes and endnotes. |
| [setIgnoreFormatting(boolean value)](#setIgnoreFormatting-boolean) | True indicates that formatting is ignored. |
| [setIgnoreHeadersAndFooters(boolean value)](#setIgnoreHeadersAndFooters-boolean) | True indicates that headers and footers content is ignored. |
| [setIgnoreTables(boolean value)](#setIgnoreTables-boolean) | Specifies whether to compare the differences in data contained in tables. |
| [setIgnoreTextboxes(boolean value)](#setIgnoreTextboxes-boolean) | Specifies whether to compare differences in the data contained within text boxes. |
| [setTarget(int value)](#setTarget-int) | Specifies which document shall be used as a target during comparison. |
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
### getCompareMoves() {#getCompareMoves}
```
public boolean getCompareMoves()
```


Specifies whether to compare differences in **T:Aspose.Words.Revisions.MoveRevision** between the two documents. By default move revisions are not produced.

**Returns:**
boolean - The corresponding  boolean  value.
### getGranularity() {#getGranularity}
```
public int getGranularity()
```


Specifies whether changes are tracked by character or by word. Default value is [Granularity.WORD\_LEVEL](../../com.aspose.words/granularity/\#WORD-LEVEL).

**Returns:**
int - The corresponding  int  value. The returned value is one of [Granularity](../../com.aspose.words/granularity/) constants.
### getIgnoreCaseChanges() {#getIgnoreCaseChanges}
```
public boolean getIgnoreCaseChanges()
```


True indicates that documents comparison is case insensitive. By default comparison is case sensitive.

**Returns:**
boolean - The corresponding  boolean  value.
### getIgnoreComments() {#getIgnoreComments}
```
public boolean getIgnoreComments()
```


Specifies whether to compare differences in comments. By default comments are not ignored.

**Returns:**
boolean - The corresponding  boolean  value.
### getIgnoreDmlUniqueId() {#getIgnoreDmlUniqueId}
```
public boolean getIgnoreDmlUniqueId()
```


Specifies whether to ignore difference in DrawingML unique Id. Default value is  false .

**Returns:**
boolean - The corresponding  boolean  value.
### getIgnoreFields() {#getIgnoreFields}
```
public boolean getIgnoreFields()
```


Specifies whether to compare differences in fields. By default fields are not ignored.

**Returns:**
boolean - The corresponding  boolean  value.
### getIgnoreFootnotes() {#getIgnoreFootnotes}
```
public boolean getIgnoreFootnotes()
```


Specifies whether to compare differences in footnotes and endnotes. By default footnotes are not ignored.

**Returns:**
boolean - The corresponding  boolean  value.
### getIgnoreFormatting() {#getIgnoreFormatting}
```
public boolean getIgnoreFormatting()
```


True indicates that formatting is ignored. By default document formatting is not ignored.

**Returns:**
boolean - The corresponding  boolean  value.
### getIgnoreHeadersAndFooters() {#getIgnoreHeadersAndFooters}
```
public boolean getIgnoreHeadersAndFooters()
```


True indicates that headers and footers content is ignored. By default headers and footers are not ignored.

**Returns:**
boolean - The corresponding  boolean  value.
### getIgnoreTables() {#getIgnoreTables}
```
public boolean getIgnoreTables()
```


Specifies whether to compare the differences in data contained in tables. By default tables are not ignored.

**Returns:**
boolean - The corresponding  boolean  value.
### getIgnoreTextboxes() {#getIgnoreTextboxes}
```
public boolean getIgnoreTextboxes()
```


Specifies whether to compare differences in the data contained within text boxes. By default textboxes are not ignored.

**Returns:**
boolean - The corresponding  boolean  value.
### getTarget() {#getTarget}
```
public int getTarget()
```


Specifies which document shall be used as a target during comparison.

**Returns:**
int - The corresponding  int  value. The returned value is one of [ComparisonTargetType](../../com.aspose.words/comparisontargettype/) constants.
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




### setCompareMoves(boolean value) {#setCompareMoves-boolean}
```
public void setCompareMoves(boolean value)
```


Specifies whether to compare differences in **T:Aspose.Words.Revisions.MoveRevision** between the two documents. By default move revisions are not produced.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setGranularity(int value) {#setGranularity-int}
```
public void setGranularity(int value)
```


Specifies whether changes are tracked by character or by word. Default value is [Granularity.WORD\_LEVEL](../../com.aspose.words/granularity/\#WORD-LEVEL).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [Granularity](../../com.aspose.words/granularity/) constants. |

### setIgnoreCaseChanges(boolean value) {#setIgnoreCaseChanges-boolean}
```
public void setIgnoreCaseChanges(boolean value)
```


True indicates that documents comparison is case insensitive. By default comparison is case sensitive.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setIgnoreComments(boolean value) {#setIgnoreComments-boolean}
```
public void setIgnoreComments(boolean value)
```


Specifies whether to compare differences in comments. By default comments are not ignored.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setIgnoreDmlUniqueId(boolean value) {#setIgnoreDmlUniqueId-boolean}
```
public void setIgnoreDmlUniqueId(boolean value)
```


Specifies whether to ignore difference in DrawingML unique Id. Default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setIgnoreFields(boolean value) {#setIgnoreFields-boolean}
```
public void setIgnoreFields(boolean value)
```


Specifies whether to compare differences in fields. By default fields are not ignored.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setIgnoreFootnotes(boolean value) {#setIgnoreFootnotes-boolean}
```
public void setIgnoreFootnotes(boolean value)
```


Specifies whether to compare differences in footnotes and endnotes. By default footnotes are not ignored.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setIgnoreFormatting(boolean value) {#setIgnoreFormatting-boolean}
```
public void setIgnoreFormatting(boolean value)
```


True indicates that formatting is ignored. By default document formatting is not ignored.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setIgnoreHeadersAndFooters(boolean value) {#setIgnoreHeadersAndFooters-boolean}
```
public void setIgnoreHeadersAndFooters(boolean value)
```


True indicates that headers and footers content is ignored. By default headers and footers are not ignored.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setIgnoreTables(boolean value) {#setIgnoreTables-boolean}
```
public void setIgnoreTables(boolean value)
```


Specifies whether to compare the differences in data contained in tables. By default tables are not ignored.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setIgnoreTextboxes(boolean value) {#setIgnoreTextboxes-boolean}
```
public void setIgnoreTextboxes(boolean value)
```


Specifies whether to compare differences in the data contained within text boxes. By default textboxes are not ignored.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setTarget(int value) {#setTarget-int}
```
public void setTarget(int value)
```


Specifies which document shall be used as a target during comparison.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [ComparisonTargetType](../../com.aspose.words/comparisontargettype/) constants. |

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

