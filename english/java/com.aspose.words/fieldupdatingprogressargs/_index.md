---
title: FieldUpdatingProgressArgs
linktitle: FieldUpdatingProgressArgs
second_title: Aspose.Words for Java
description: Provides data for the field updating progress event in Java.
type: docs
weight: 270
url: /java/com.aspose.words/fieldupdatingprogressargs/
---

**Inheritance:**
java.lang.Object
```
public class FieldUpdatingProgressArgs
```

Provides data for the field updating progress event.
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getTotalFieldsCount()](#getTotalFieldsCount) | Gets the total fields count to be updated. |
| [getUpdateCompleted()](#getUpdateCompleted) | Gets a value indicating whether field updating is completed. |
| [getUpdatedFieldsCount()](#getUpdatedFieldsCount) | Gets the number of updated fields. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
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
### getTotalFieldsCount() {#getTotalFieldsCount}
```
public int getTotalFieldsCount()
```


Gets the total fields count to be updated.

 **Remarks:** 

The value is not constant and may be increased during updating process.

**Returns:**
int - The total fields count to be updated.
### getUpdateCompleted() {#getUpdateCompleted}
```
public boolean getUpdateCompleted()
```


Gets a value indicating whether field updating is completed.

**Returns:**
boolean - A value indicating whether field updating is completed.
### getUpdatedFieldsCount() {#getUpdatedFieldsCount}
```
public int getUpdatedFieldsCount()
```


Gets the number of updated fields.

**Returns:**
int - The number of updated fields.
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

