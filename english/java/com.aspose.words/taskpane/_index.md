---
title: TaskPane
linktitle: TaskPane
second_title: Aspose.Words for Java API Reference
description: Represents an add-in task pane object in Java.
type: docs
weight: 561
url: /java/com.aspose.words/taskpane/
---

**Inheritance:**
java.lang.Object
```
public class TaskPane
```

Represents an add-in task pane object.

To learn more, visit the [ Work with Office Add-ins ][Work with Office Add-ins] documentation article.


[Work with Office Add-ins]: https://docs.aspose.com/words/java/work-with-office-add-ins/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getDockState()](#getDockState) | Specifies the last-docked location of this task pane object. |
| [getRow()](#getRow) | Specifies the index, enumerating from the outside to the inside, of this task pane among other persisted task panes docked in the same default location. |
| [getWebExtension()](#getWebExtension) | Represents an web extension object. |
| [getWidth()](#getWidth) | Specifies the default width value for this task pane instance. |
| [hashCode()](#hashCode) |  |
| [isLocked()](#isLocked) | Specifies whether the task pane is locked to the document in the UI and cannot be closed by the user. |
| [isLocked(boolean value)](#isLocked-boolean) | Specifies whether the task pane is locked to the document in the UI and cannot be closed by the user. |
| [isVisible()](#isVisible) | Specifies whether the task pane shows as visible by default when the document opens. |
| [isVisible(boolean value)](#isVisible-boolean) | Specifies whether the task pane shows as visible by default when the document opens. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setDockState(int value)](#setDockState-int) | Specifies the last-docked location of this task pane object. |
| [setRow(int value)](#setRow-int) | Specifies the index, enumerating from the outside to the inside, of this task pane among other persisted task panes docked in the same default location. |
| [setWidth(double value)](#setWidth-double) | Specifies the default width value for this task pane instance. |
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
### getDockState() {#getDockState}
```
public int getDockState()
```


Specifies the last-docked location of this task pane object.

**Returns:**
int - The corresponding  int  value. The returned value is one of [TaskPaneDockState](../../com.aspose.words/taskpanedockstate/) constants.
### getRow() {#getRow}
```
public int getRow()
```


Specifies the index, enumerating from the outside to the inside, of this task pane among other persisted task panes docked in the same default location.

**Returns:**
int - The corresponding  int  value.
### getWebExtension() {#getWebExtension}
```
public WebExtension getWebExtension()
```


Represents an web extension object.

**Returns:**
[WebExtension](../../com.aspose.words/webextension/) - The corresponding [WebExtension](../../com.aspose.words/webextension/) value.
### getWidth() {#getWidth}
```
public double getWidth()
```


Specifies the default width value for this task pane instance.

**Returns:**
double - The corresponding  double  value.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isLocked() {#isLocked}
```
public boolean isLocked()
```


Specifies whether the task pane is locked to the document in the UI and cannot be closed by the user.

**Returns:**
boolean - The corresponding  boolean  value.
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


Specifies whether the task pane is locked to the document in the UI and cannot be closed by the user.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### isVisible() {#isVisible}
```
public boolean isVisible()
```


Specifies whether the task pane shows as visible by default when the document opens.

**Returns:**
boolean - The corresponding  boolean  value.
### isVisible(boolean value) {#isVisible-boolean}
```
public void isVisible(boolean value)
```


Specifies whether the task pane shows as visible by default when the document opens.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### setDockState(int value) {#setDockState-int}
```
public void setDockState(int value)
```


Specifies the last-docked location of this task pane object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [TaskPaneDockState](../../com.aspose.words/taskpanedockstate/) constants. |

### setRow(int value) {#setRow-int}
```
public void setRow(int value)
```


Specifies the index, enumerating from the outside to the inside, of this task pane among other persisted task panes docked in the same default location.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setWidth(double value) {#setWidth-double}
```
public void setWidth(double value)
```


Specifies the default width value for this task pane instance.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

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

