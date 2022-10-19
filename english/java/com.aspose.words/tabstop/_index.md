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
| [hashCode()](#hashCode--) |  |
| [getPosition()](#getPosition--) | Gets the position of the tab stop in points. |
| [getAlignment()](#getAlignment--) | Gets the alignment of text at this tab stop. |
| [setAlignment(int value)](#setAlignment-int-) | Sets the alignment of text at this tab stop. |
| [getLeader()](#getLeader--) | Gets the type of the leader line displayed under the tab character. |
| [setLeader(int value)](#setLeader-int-) | Sets the type of the leader line displayed under the tab character. |
| [isClear()](#isClear--) | Returns true if this tab stop clears any existing tab stops in this position. |
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
### hashCode() {#hashCode--}
```
public int hashCode()
```




**Returns:**
int
### getPosition() {#getPosition--}
```
public double getPosition()
```


Gets the position of the tab stop in points.

**Returns:**
double - The position of the tab stop in points.
### getAlignment() {#getAlignment--}
```
public int getAlignment()
```


Gets the alignment of text at this tab stop.

**Returns:**
int - The alignment of text at this tab stop. The returned value is one of [TabAlignment](../../com.aspose.words/tabalignment) constants.
### setAlignment(int value) {#setAlignment-int-}
```
public void setAlignment(int value)
```


Sets the alignment of text at this tab stop.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The alignment of text at this tab stop. The value must be one of [TabAlignment](../../com.aspose.words/tabalignment) constants. |

### getLeader() {#getLeader--}
```
public int getLeader()
```


Gets the type of the leader line displayed under the tab character.

**Returns:**
int - The type of the leader line displayed under the tab character. The returned value is one of [TabLeader](../../com.aspose.words/tableader) constants.
### setLeader(int value) {#setLeader-int-}
```
public void setLeader(int value)
```


Sets the type of the leader line displayed under the tab character.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The type of the leader line displayed under the tab character. The value must be one of [TabLeader](../../com.aspose.words/tableader) constants. |

### isClear() {#isClear--}
```
public boolean isClear()
```


Returns true if this tab stop clears any existing tab stops in this position.

**Returns:**
boolean - True if this tab stop clears any existing tab stops in this position.
