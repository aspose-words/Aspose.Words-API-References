---
title: VbaReference
second_title: Aspose.Words for Java API Reference
description: Implements a reference to an Automation type library or VBA project.
type: docs
weight: 600
url: /java/com.aspose.words/vbareference/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public abstract class VbaReference implements Cloneable
```

Implements a reference to an Automation type library or VBA project.

To learn more, visit the [ Working with VBA Macros ][Working with VBA Macros] documentation article.


[Working with VBA Macros]: https://docs.aspose.com/words/java/working-with-vba-macros/
## Constructors

| Constructor | Description |
| --- | --- |
| [VbaReference()](#VbaReference) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getLibId()](#getLibId) | Gets a string value containing the identifier of an Automation type library. |
| [getType()](#getType) | Gets [VbaReferenceType](../../com.aspose.words/vbareferencetype) object that indicates the type of reference that a [VbaReference](../../com.aspose.words/vbareference) object represents. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### VbaReference() {#VbaReference}
```
public VbaReference()
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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getLibId() {#getLibId}
```
public abstract String getLibId()
```


Gets a string value containing the identifier of an Automation type library. Depending on reference type, the value of this property can be:

 *  a LibidReference specified at 2.1.1.8 LibidReference of [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/3737ef6e-d819-4186-a5f2-6e258ddf66a5
 *  a ProjectReference specified at 2.1.1.12 ProjectReference of [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/9a45ac1a-f1ff-4ebd-958e-537701aa8131

**Returns:**
java.lang.String - A string value containing the identifier of an Automation type library.
### getType() {#getType}
```
public abstract int getType()
```


Gets [VbaReferenceType](../../com.aspose.words/vbareferencetype) object that indicates the type of reference that a [VbaReference](../../com.aspose.words/vbareference) object represents.

**Returns:**
int - \{[VbaReferenceType](../../com.aspose.words/vbareferencetype) object that indicates the type of reference that a [VbaReference](../../com.aspose.words/vbareference) object represents. The returned value is one of [VbaReferenceType](../../com.aspose.words/vbareferencetype) constants.
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

