---
title: VbaReferenceType
second_title: Aspose.Words for Java API Reference
description: Allows to specify the type of a  object.
type: docs
weight: 603
url: /java/com.aspose.words/vbareferencetype/
---

**Inheritance:**
java.lang.Object
```
public class VbaReferenceType
```

Allows to specify the type of a [VbaReference](../../com.aspose.words/vbareference) object.
## Fields

| Field | Description |
| --- | --- |
| [CONTROL](#CONTROL) | Specifies a twiddled type library reference type. |
| [ORIGINAL](#ORIGINAL) | Specifies an original Automation type library reference type. |
| [PROJECT](#PROJECT) | Specified an external VBA project reference type. |
| [REGISTERED](#REGISTERED) | Specifies an Automation type library reference type. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String vbaReferenceTypeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int vbaReferenceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int vbaReferenceType)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### CONTROL {#CONTROL}
```
public static int CONTROL
```


Specifies a twiddled type library reference type. This type corresponds to 2.3.4.2.2.3 REFERENCECONTROL Record of [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/d64485fa-8562-4726-9c5e-11e8f01a81c0

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


Specifies an original Automation type library reference type. This type corresponds to 2.3.4.2.2.4 REFERENCEORIGINAL Record of [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/3ba66994-8c7a-4634-b2da-f9331ace6686

### PROJECT {#PROJECT}
```
public static int PROJECT
```


Specified an external VBA project reference type. This type corresponds to 2.3.4.2.2.6 REFERENCEPROJECT Record of [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/08280eb0-d628-495c-867f-5985ed020142

### REGISTERED {#REGISTERED}
```
public static int REGISTERED
```


Specifies an Automation type library reference type. This type corresponds to 2.3.4.2.2.5 REFERENCEREGISTERED Record of [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/6c39388e-96f5-4b93-b90a-ae625a063fcf

### length {#length}
```
public static int length
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
### fromName(String vbaReferenceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String vbaReferenceTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| vbaReferenceTypeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int vbaReferenceType) {#getName-int}
```
public static String getName(int vbaReferenceType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| vbaReferenceType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
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
### toString(int vbaReferenceType) {#toString-int}
```
public static String toString(int vbaReferenceType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| vbaReferenceType | int |  |

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

