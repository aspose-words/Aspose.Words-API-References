---
title: Rule
second_title: Aspose.Words for Java API Reference
description: Indicates the action that occurs when a  is enforced.
type: docs
weight: 36
url: /java/com.aspose.words.net.system.data/rule/
---

**Inheritance:**
java.lang.Object, java.lang.Enum
```
public enum Rule extends Enum<System.Data.Rule>
```

Indicates the action that occurs when a [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint) is enforced.
## Fields

| Field | Description |
| --- | --- |
| [CASCADE](#CASCADE) | Delete or update related rows. |
| [NONE](#NONE) | No action taken on related rows. |
| [SET_DEFAULT](#SET-DEFAULT) | Set values in related rows to the value contained in the [DataColumn.getDefaultValue()](../../com.aspose.words.net.system.data/datacolumn\#getDefaultValue) / [DataColumn.setDefaultValue(java.lang.Object)](../../com.aspose.words.net.system.data/datacolumn\#setDefaultValue-java.lang.Object) property. |
| [SET_NULL](#SET-NULL) | Set values in related rows to DBNull. |
## Methods

| Method | Description |
| --- | --- |
| [<T>valueOf(Class<T> arg0, String arg1)](#-T-valueOf-java.lang.Class-T--java.lang.String) |  |
| [compareTo(E arg0)](#compareTo-E) |  |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getDeclaringClass()](#getDeclaringClass) |  |
| [hashCode()](#hashCode) |  |
| [name()](#name) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [ordinal()](#ordinal) |  |
| [toString()](#toString) |  |
| [valueOf(String name)](#valueOf-java.lang.String) |  |
| [values()](#values) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### CASCADE {#CASCADE}
```
public static final System.Data.Rule CASCADE
```


Delete or update related rows. This is the default.

### NONE {#NONE}
```
public static final System.Data.Rule NONE
```


No action taken on related rows.

### SET_DEFAULT {#SET-DEFAULT}
```
public static final System.Data.Rule SET_DEFAULT
```


Set values in related rows to the value contained in the [DataColumn.getDefaultValue()](../../com.aspose.words.net.system.data/datacolumn\#getDefaultValue) / [DataColumn.setDefaultValue(java.lang.Object)](../../com.aspose.words.net.system.data/datacolumn\#setDefaultValue-java.lang.Object) property.

### SET_NULL {#SET-NULL}
```
public static final System.Data.Rule SET_NULL
```


Set values in related rows to DBNull.

### <T>valueOf(Class<T> arg0, String arg1) {#-T-valueOf-java.lang.Class-T--java.lang.String}
```
public static T <T>valueOf(Class<T> arg0, String arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Class<T> |  |
| arg1 | java.lang.String |  |

**Returns:**
T
### compareTo(E arg0) {#compareTo-E}
```
public final int compareTo(E arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | E |  |

**Returns:**
int
### equals(Object arg0) {#equals-java.lang.Object}
```
public final boolean equals(Object arg0)
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
### getDeclaringClass() {#getDeclaringClass}
```
public final Class<E> getDeclaringClass()
```




**Returns:**
java.lang.Class<E>
### hashCode() {#hashCode}
```
public final int hashCode()
```




**Returns:**
int
### name() {#name}
```
public final String name()
```




**Returns:**
java.lang.String
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### ordinal() {#ordinal}
```
public final int ordinal()
```




**Returns:**
int
### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### valueOf(String name) {#valueOf-java.lang.String}
```
public static System.Data.Rule valueOf(String name)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String |  |

**Returns:**
[Rule](../../com.aspose.words.net.system.data/rule)
### values() {#values}
```
public static System.Data.Rule[] values()
```




**Returns:**
com.aspose.words.net.System.Data.Rule[]
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

