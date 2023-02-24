---
title: CustomXmlProperty
linktitle: CustomXmlProperty
second_title: Aspose.Words for Java API Reference
description: Represents a single custom XML attribute or a smart tag property in Java.
type: docs
weight: 107
url: /java/com.aspose.words/customxmlproperty/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class CustomXmlProperty implements Cloneable
```

Represents a single custom XML attribute or a smart tag property.

To learn more, visit the [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control] documentation article.

Used as an item of a [CustomXmlPropertyCollection](../../com.aspose.words/customxmlpropertycollection/) collection.


[Structured Document Tags or Content Control]: https://docs.aspose.com/words/java/working-with-content-control-sdt/
## Constructors

| Constructor | Description |
| --- | --- |
| [CustomXmlProperty(String name, String uri, String value)](#CustomXmlProperty-java.lang.String-java.lang.String-java.lang.String) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getName()](#getName) | Specifies the name of the custom XML attribute or smart tag property. |
| [getUri()](#getUri) | Gets the namespace URI of the custom XML attribute or smart tag property. |
| [getValue()](#getValue) | Gets the value of the custom XML attribute or smart tag property. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setUri(String value)](#setUri-java.lang.String) | Sets the namespace URI of the custom XML attribute or smart tag property. |
| [setValue(String value)](#setValue-java.lang.String) | Sets the value of the custom XML attribute or smart tag property. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### CustomXmlProperty(String name, String uri, String value) {#CustomXmlProperty-java.lang.String-java.lang.String-java.lang.String}
```
public CustomXmlProperty(String name, String uri, String value)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the property. Cannot be  null . |
| uri | java.lang.String | The namespace URI of the property. Cannot be  null . |
| value | java.lang.String | The value of the property. Cannot be  null . |

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
### getName() {#getName}
```
public String getName()
```


Specifies the name of the custom XML attribute or smart tag property.

Cannot be  null .

Default is empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getUri() {#getUri}
```
public String getUri()
```


Gets the namespace URI of the custom XML attribute or smart tag property.

Cannot be  null .

Default is empty string.

**Returns:**
java.lang.String - The namespace URI of the custom XML attribute or smart tag property.
### getValue() {#getValue}
```
public String getValue()
```


Gets the value of the custom XML attribute or smart tag property.

Cannot be  null .

Default is empty string.

**Returns:**
java.lang.String - The value of the custom XML attribute or smart tag property.
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




### setUri(String value) {#setUri-java.lang.String}
```
public void setUri(String value)
```


Sets the namespace URI of the custom XML attribute or smart tag property.

Cannot be  null .

Default is empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The namespace URI of the custom XML attribute or smart tag property. |

### setValue(String value) {#setValue-java.lang.String}
```
public void setValue(String value)
```


Sets the value of the custom XML attribute or smart tag property.

Cannot be  null .

Default is empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The value of the custom XML attribute or smart tag property. |

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

