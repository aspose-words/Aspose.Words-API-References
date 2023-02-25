---
title: ReplacingArgs
linktitle: ReplacingArgs
second_title: Aspose.Words for Java API Reference
description: Provides data for a custom replace operation in Java.
type: docs
weight: 482
url: /java/com.aspose.words/replacingargs/
---

**Inheritance:**
java.lang.Object
```
public class ReplacingArgs
```

Provides data for a custom replace operation.

To learn more, visit the [ Find and Replace ][Find and Replace] documentation article.


[Find and Replace]: https://docs.aspose.com/words/java/find-and-replace/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getGroupIndex()](#getGroupIndex) | Identifies, by index, a captured group in the [getMatch()](../../com.aspose.words/replacingargs/\#getMatch) that is to be replaced with the [getReplacement()](../../com.aspose.words/replacingargs/\#getReplacement) / [setReplacement(java.lang.String)](../../com.aspose.words/replacingargs/\#setReplacement-java.lang.String) string. |
| [getMatch()](#getMatch) | The java.util.regex.Matcher resulting from a single regular expression match during a **Replace**. |
| [getMatchNode()](#getMatchNode) | Gets the node that contains the beginning of the match. |
| [getMatchOffset()](#getMatchOffset) | Gets the zero-based starting position of the match from the start of the node that contains the beginning of the match. |
| [getReplacement()](#getReplacement) | Gets the replacement string. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setGroupIndex(int value)](#setGroupIndex-int) | Identifies, by index, a captured group in the [getMatch()](../../com.aspose.words/replacingargs/\#getMatch) that is to be replaced with the [getReplacement()](../../com.aspose.words/replacingargs/\#getReplacement) / [setReplacement(java.lang.String)](../../com.aspose.words/replacingargs/\#setReplacement-java.lang.String) string. |
| [setReplacement(String value)](#setReplacement-java.lang.String) | Sets the replacement string. |
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
### getGroupIndex() {#getGroupIndex}
```
public int getGroupIndex()
```


Identifies, by index, a captured group in the [getMatch()](../../com.aspose.words/replacingargs/\#getMatch) that is to be replaced with the [getReplacement()](../../com.aspose.words/replacingargs/\#getReplacement) / [setReplacement(java.lang.String)](../../com.aspose.words/replacingargs/\#setReplacement-java.lang.String) string.

Default is zero.

**Returns:**
int - The corresponding  int  value.
### getMatch() {#getMatch}
```
public Matcher getMatch()
```


The java.util.regex.Matcher resulting from a single regular expression match during a **Replace**.

Matcher.start()  gets the zero-based starting position of the match from the start of the find and replace range.

**Returns:**
java.util.regex.Matcher - The corresponding java.util.regex.Matcher value.
### getMatchNode() {#getMatchNode}
```
public Node getMatchNode()
```


Gets the node that contains the beginning of the match.

**Returns:**
[Node](../../com.aspose.words/node/) - The node that contains the beginning of the match.
### getMatchOffset() {#getMatchOffset}
```
public int getMatchOffset()
```


Gets the zero-based starting position of the match from the start of the node that contains the beginning of the match.

**Returns:**
int - The zero-based starting position of the match from the start of the node that contains the beginning of the match.
### getReplacement() {#getReplacement}
```
public String getReplacement()
```


Gets the replacement string.

**Returns:**
java.lang.String - The replacement string.
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




### setGroupIndex(int value) {#setGroupIndex-int}
```
public void setGroupIndex(int value)
```


Identifies, by index, a captured group in the [getMatch()](../../com.aspose.words/replacingargs/\#getMatch) that is to be replaced with the [getReplacement()](../../com.aspose.words/replacingargs/\#getReplacement) / [setReplacement(java.lang.String)](../../com.aspose.words/replacingargs/\#setReplacement-java.lang.String) string.

Default is zero.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setReplacement(String value) {#setReplacement-java.lang.String}
```
public void setReplacement(String value)
```


Sets the replacement string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The replacement string. |

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

