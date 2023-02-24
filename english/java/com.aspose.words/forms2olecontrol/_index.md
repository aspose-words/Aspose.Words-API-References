---
title: Forms2OleControl
linktitle: Forms2OleControl
second_title: Aspose.Words for Java API Reference
description: Represents Microsoft Forms 2.0 OLE control in Java.
type: docs
weight: 300
url: /java/com.aspose.words/forms2olecontrol/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.OleControl](../../com.aspose.words/olecontrol/)
```
public abstract class Forms2OleControl extends OleControl
```

Represents Microsoft Forms 2.0 OLE control.

To learn more, visit the [ Working with Ole Objects ][Working with Ole Objects] documentation article.


[Working with Ole Objects]: https://docs.aspose.com/words/java/working-with-ole-objects/
## Constructors

| Constructor | Description |
| --- | --- |
| [Forms2OleControl()](#Forms2OleControl) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getCaption()](#getCaption) | Gets Caption property of control. |
| [getChildNodes()](#getChildNodes) | Gets collection of immediate child controls. |
| [getClass()](#getClass) |  |
| [getClsidInternal()](#getClsidInternal) |  |
| [getEnabled()](#getEnabled) | Returns  true  if control is in enabled state. |
| [getExtensionForUser(String progId)](#getExtensionForUser-java.lang.String) |  |
| [getFileNameForUser()](#getFileNameForUser) |  |
| [getId()](#getId) |  |
| [getName()](#getName) | Gets name of the ActiveX control. |
| [getType()](#getType) | Gets type of Forms 2.0 control. |
| [getValue()](#getValue) | Gets underlying Value property which often represents control state. |
| [hashCode()](#hashCode) |  |
| [isForms2OleControl()](#isForms2OleControl) | Returns  true  if the control is a [Forms2OleControl](../../com.aspose.words/forms2olecontrol/). |
| [isForms2OleControlInternal()](#isForms2OleControlInternal) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setId(int value)](#setId-int) |  |
| [setName(String value)](#setName-java.lang.String) | Gets name of the ActiveX control. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### Forms2OleControl() {#Forms2OleControl}
```
public Forms2OleControl()
```


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
### getCaption() {#getCaption}
```
public String getCaption()
```


Gets Caption property of control. Default value is an empty string.

**Returns:**
java.lang.String - Caption property of control.
### getChildNodes() {#getChildNodes}
```
public Forms2OleControlCollection getChildNodes()
```


Gets collection of immediate child controls. Returns  null  if this control can not have children.

**Returns:**
[Forms2OleControlCollection](../../com.aspose.words/forms2olecontrolcollection/) - Collection of immediate child controls.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getClsidInternal() {#getClsidInternal}
```
public String getClsidInternal()
```




**Returns:**
java.lang.String
### getEnabled() {#getEnabled}
```
public boolean getEnabled()
```


Returns  true  if control is in enabled state.

**Returns:**
boolean - \{ true  if control is in enabled state.
### getExtensionForUser(String progId) {#getExtensionForUser-java.lang.String}
```
public String getExtensionForUser(String progId)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| progId | java.lang.String |  |

**Returns:**
java.lang.String
### getFileNameForUser() {#getFileNameForUser}
```
public String getFileNameForUser()
```




**Returns:**
java.lang.String
### getId() {#getId}
```
public int getId()
```




**Returns:**
int
### getName() {#getName}
```
public String getName()
```


Gets name of the ActiveX control.

**Returns:**
java.lang.String - Name of the ActiveX control.
### getType() {#getType}
```
public abstract int getType()
```


Gets type of Forms 2.0 control.

**Returns:**
int - Type of Forms 2.0 control. The returned value is one of [Forms2OleControlType](../../com.aspose.words/forms2olecontroltype/) constants.
### getValue() {#getValue}
```
public String getValue()
```


Gets underlying Value property which often represents control state. For example checked option button has '1' value while unchecked has '0'. Default value is an empty string.

**Returns:**
java.lang.String - Underlying Value property which often represents control state.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isForms2OleControl() {#isForms2OleControl}
```
public boolean isForms2OleControl()
```


Returns  true  if the control is a [Forms2OleControl](../../com.aspose.words/forms2olecontrol/).

**Returns:**
boolean - \{ true  if the control is a [Forms2OleControl](../../com.aspose.words/forms2olecontrol/).
### isForms2OleControlInternal() {#isForms2OleControlInternal}
```
public boolean isForms2OleControlInternal()
```




**Returns:**
boolean
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### setId(int value) {#setId-int}
```
public void setId(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Gets name of the ActiveX control.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Name of the ActiveX control. |

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

