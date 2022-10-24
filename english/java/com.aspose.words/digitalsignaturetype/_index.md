---
title: DigitalSignatureType
second_title: Aspose.Words for Java API Reference
description: Specifies the type of a digital signature.
type: docs
weight: 113
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
| [UNKNOWN](#UNKNOWN) | Indicates an error, unknown digital signature type. |
| [CRYPTO_API](#CRYPTO-API) | The Crypto API signature method used in Microsoft Word 97-2003 .DOC binary documents. |
| [XML_DSIG](#XML-DSIG) | The XmlDsig signature method used in OOXML and OpenDocument documents. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int digitalSignatureType)](#getName-int-) |  |
| [toString(int digitalSignatureType)](#toString-int-) |  |
| [fromName(String digitalSignatureTypeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Indicates an error, unknown digital signature type.

### CRYPTO_API {#CRYPTO-API}
```
public static int CRYPTO_API
```


The Crypto API signature method used in Microsoft Word 97-2003 .DOC binary documents.

### XML_DSIG {#XML-DSIG}
```
public static int XML_DSIG
```


The XmlDsig signature method used in OOXML and OpenDocument documents.

### length {#length}
```
public static int length
```


### getName(int digitalSignatureType) {#getName-int-}
```
public static String getName(int digitalSignatureType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| digitalSignatureType | int |  |

**Returns:**
java.lang.String
### toString(int digitalSignatureType) {#toString-int-}
```
public static String toString(int digitalSignatureType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| digitalSignatureType | int |  |

**Returns:**
java.lang.String
### fromName(String digitalSignatureTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String digitalSignatureTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| digitalSignatureTypeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
