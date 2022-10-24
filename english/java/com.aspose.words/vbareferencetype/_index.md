---
title: VbaReferenceType
second_title: Aspose.Words for Java API Reference
description: Allows to specify the type of a  object.
type: docs
weight: 599
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
| [REGISTERED](#REGISTERED) | Specifies an Automation type library reference type. |
| [PROJECT](#PROJECT) | Specified an external VBA project reference type. |
| [ORIGINAL](#ORIGINAL) | Specifies an original Automation type library reference type. |
| [CONTROL](#CONTROL) | Specifies a twiddled type library reference type. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int vbaReferenceType)](#getName-int-) |  |
| [toString(int vbaReferenceType)](#toString-int-) |  |
| [fromName(String vbaReferenceTypeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### REGISTERED {#REGISTERED}
```
public static int REGISTERED
```


Specifies an Automation type library reference type. This type corresponds to 2.3.4.2.2.5 REFERENCEREGISTERED Record of [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/6c39388e-96f5-4b93-b90a-ae625a063fcf

### PROJECT {#PROJECT}
```
public static int PROJECT
```


Specified an external VBA project reference type. This type corresponds to 2.3.4.2.2.6 REFERENCEPROJECT Record of [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/08280eb0-d628-495c-867f-5985ed020142

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


Specifies an original Automation type library reference type. This type corresponds to 2.3.4.2.2.4 REFERENCEORIGINAL Record of [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/3ba66994-8c7a-4634-b2da-f9331ace6686

### CONTROL {#CONTROL}
```
public static int CONTROL
```


Specifies a twiddled type library reference type. This type corresponds to 2.3.4.2.2.3 REFERENCECONTROL Record of [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/d64485fa-8562-4726-9c5e-11e8f01a81c0

### length {#length}
```
public static int length
```


### getName(int vbaReferenceType) {#getName-int-}
```
public static String getName(int vbaReferenceType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| vbaReferenceType | int |  |

**Returns:**
java.lang.String
### toString(int vbaReferenceType) {#toString-int-}
```
public static String toString(int vbaReferenceType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| vbaReferenceType | int |  |

**Returns:**
java.lang.String
### fromName(String vbaReferenceTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String vbaReferenceTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| vbaReferenceTypeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
