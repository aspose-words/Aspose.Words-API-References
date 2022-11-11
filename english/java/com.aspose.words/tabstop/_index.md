---
title: TabStop
second_title: Aspose.Words for Java API Reference
description: Represents a single custom tab stop.
type: docs
weight: 546
url: /java/com.aspose.words/tabstop/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class TabStop implements Cloneable
```

Represents a single custom tab stop. The **TabStop** object is a member of the [TabStopCollection](../../com.aspose.words/tabstopcollection) collection.

To learn more, visit the **Aspose.Words Document Object Model (DOM)** documentation article.

Normally, a tab stop specifies a position where a tab stop exists. But because tab stops can be inherited from parent styles, it might be needed for the child object to define explicitly that there is no tab stop at a given position. To clear an inherited tab stop at a given position, create a **TabStop** object and set [getAlignment()](../../com.aspose.words/tabstop\#getAlignment--) / [setAlignment(int)](../../com.aspose.words/tabstop\#setAlignment-int-) to  TabAlignment.Clear .

For more information see [TabStopCollection](../../com.aspose.words/tabstopcollection).
## Constructors

| Constructor | Description |
| --- | --- |
| [TabStop(double position)](#TabStop-double-) | Initializes a new instance of this class. |
| [TabStop(double position, int alignment, int leader)](#TabStop-double-int-int-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [equals(TabStop rhs)](#equals-com.aspose.words.TabStop-) | Compares with the specified TabStop. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAlignment()](#getAlignment--) | Gets the alignment of text at this tab stop. |
| [getClass()](#getClass--) |  |
| [getLeader()](#getLeader--) | Gets the type of the leader line displayed under the tab character. |
| [getPosition()](#getPosition--) | Gets the position of the tab stop in points. |
| [hashCode()](#hashCode--) |  |
| [isClear()](#isClear--) | Returns true if this tab stop clears any existing tab stops in this position. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAlignment(int value)](#setAlignment-int-) | Sets the alignment of text at this tab stop. |
| [setLeader(int value)](#setLeader-int-) | Sets the type of the leader line displayed under the tab character. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### TabStop(double position) {#TabStop-double-}
```
public TabStop(double position)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| position | double |  |

### TabStop(double position, int alignment, int leader) {#TabStop-double-int-int-}
```
public TabStop(double position, int alignment, int leader)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| position | double |  |
| alignment | int |  |
| leader | int |  |

### equals(TabStop rhs) {#equals-com.aspose.words.TabStop-}
```
public boolean equals(TabStop rhs)
```


Compares with the specified TabStop.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rhs | [TabStop](../../com.aspose.words/tabstop) |  |

**Returns:**
boolean
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getAlignment() {#getAlignment--}
```
public int getAlignment()
```


Gets the alignment of text at this tab stop.

**Returns:**
int - The alignment of text at this tab stop. The returned value is one of [TabAlignment](../../com.aspose.words/tabalignment) constants.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getLeader() {#getLeader--}
```
public int getLeader()
```


Gets the type of the leader line displayed under the tab character.

**Returns:**
int - The type of the leader line displayed under the tab character. The returned value is one of [TabLeader](../../com.aspose.words/tableader) constants.
### getPosition() {#getPosition--}
```
public double getPosition()
```


Gets the position of the tab stop in points.

**Returns:**
double - The position of the tab stop in points.
### hashCode() {#hashCode--}
```
public int hashCode()
```




**Returns:**
int
### isClear() {#isClear--}
```
public boolean isClear()
```


Returns true if this tab stop clears any existing tab stops in this position.

**Returns:**
boolean - True if this tab stop clears any existing tab stops in this position.
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setAlignment(int value) {#setAlignment-int-}
```
public void setAlignment(int value)
```


Sets the alignment of text at this tab stop.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The alignment of text at this tab stop. The value must be one of [TabAlignment](../../com.aspose.words/tabalignment) constants. |

### setLeader(int value) {#setLeader-int-}
```
public void setLeader(int value)
```


Sets the type of the leader line displayed under the tab character.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The type of the leader line displayed under the tab character. The value must be one of [TabLeader](../../com.aspose.words/tableader) constants. |

### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

