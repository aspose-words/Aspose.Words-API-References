---
title: DigitalSignatureType
second_title: Aspose.Words for Java API Reference
description: Specifies the type of a digital signature.
type: docs
weight: 114
url: /java/com.aspose.words/digitalsignaturetype/
---

**Inheritance:**
java.lang.Object
```
public class DigitalSignatureType
```

Specifies the type of a digital signature.
## Fields

| Field | Description |
| --- | --- |
| [CRYPTO_API](#CRYPTO-API) | The Crypto API signature method used in Microsoft Word 97-2003 .DOC binary documents. |
| [UNKNOWN](#UNKNOWN) | Indicates an error, unknown digital signature type. |
| [XML_DSIG](#XML-DSIG) | The XmlDsig signature method used in OOXML and OpenDocument documents. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String digitalSignatureTypeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int digitalSignatureType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int digitalSignatureType)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### CRYPTO_API {#CRYPTO-API}
```
public static int CRYPTO_API
```


The Crypto API signature method used in Microsoft Word 97-2003 .DOC binary documents.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Indicates an error, unknown digital signature type.

### XML_DSIG {#XML-DSIG}
```
public static int XML_DSIG
```


The XmlDsig signature method used in OOXML and OpenDocument documents.

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
### fromName(String digitalSignatureTypeName) {#fromName-java.lang.String}
```
public static int fromName(String digitalSignatureTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| digitalSignatureTypeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int digitalSignatureType) {#getName-int}
```
public static String getName(int digitalSignatureType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| digitalSignatureType | int |  |

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
### toString(int digitalSignatureType) {#toString-int}
```
public static String toString(int digitalSignatureType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| digitalSignatureType | int |  |

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

