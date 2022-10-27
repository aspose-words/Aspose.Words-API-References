---
title: DocumentSecurity
second_title: Aspose.Words for Java API Reference
description: Used as a value for the  /  property.
type: docs
weight: 130
url: /java/com.aspose.words/documentsecurity/
---

**Inheritance:**
java.lang.Object
```
public class DocumentSecurity
```

Used as a value for the [BuiltInDocumentProperties.getSecurity()](../../com.aspose.words/builtindocumentproperties\#getSecurity--) / [BuiltInDocumentProperties.setSecurity(int)](../../com.aspose.words/builtindocumentproperties\#setSecurity-int-) property. Specifies the security level of a document as a numeric value.
## Fields

| Field | Description |
| --- | --- |
| [NONE](#NONE) | There are no security states specified by the property. |
| [PASSWORD_PROTECTED](#PASSWORD-PROTECTED) | The document is password protected. |
| [READ_ONLY_RECOMMENDED](#READ-ONLY-RECOMMENDED) | The document to be opened read-only if possible, but the setting can be overridden. |
| [READ_ONLY_ENFORCED](#READ-ONLY-ENFORCED) | The document to always be opened read-only. |
| [READ_ONLY_EXCEPT_ANNOTATIONS](#READ-ONLY-EXCEPT-ANNOTATIONS) | The document to always be opened read-only except for annotations. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int documentSecurity)](#getName-int-) |  |
| [getNames(int documentSecurity)](#getNames-int-) |  |
| [toString(int documentSecurity)](#toString-int-) |  |
| [toStringSet(int attr)](#toStringSet-int-) |  |
| [fromName(String documentSecurityName)](#fromName-java.lang.String-) |  |
| [fromNames(Set documentSecurityNames)](#fromNames-java.util.Set-) |  |
| [getValues()](#getValues--) |  |
### NONE {#NONE}
```
public static int NONE
```


There are no security states specified by the property.

### PASSWORD_PROTECTED {#PASSWORD-PROTECTED}
```
public static int PASSWORD_PROTECTED
```


The document is password protected. (Note has never been seen in a document so far).

### READ_ONLY_RECOMMENDED {#READ-ONLY-RECOMMENDED}
```
public static int READ_ONLY_RECOMMENDED
```


The document to be opened read-only if possible, but the setting can be overridden.

### READ_ONLY_ENFORCED {#READ-ONLY-ENFORCED}
```
public static int READ_ONLY_ENFORCED
```


The document to always be opened read-only.

### READ_ONLY_EXCEPT_ANNOTATIONS {#READ-ONLY-EXCEPT-ANNOTATIONS}
```
public static int READ_ONLY_EXCEPT_ANNOTATIONS
```


The document to always be opened read-only except for annotations.

### length {#length}
```
public static int length
```


### getName(int documentSecurity) {#getName-int-}
```
public static String getName(int documentSecurity)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentSecurity | int |  |

**Returns:**
java.lang.String
### getNames(int documentSecurity) {#getNames-int-}
```
public static Set getNames(int documentSecurity)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentSecurity | int |  |

**Returns:**
java.util.Set
### toString(int documentSecurity) {#toString-int-}
```
public static String toString(int documentSecurity)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentSecurity | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int-}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
### fromName(String documentSecurityName) {#fromName-java.lang.String-}
```
public static int fromName(String documentSecurityName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentSecurityName | java.lang.String |  |

**Returns:**
int
### fromNames(Set documentSecurityNames) {#fromNames-java.util.Set-}
```
public static int fromNames(Set documentSecurityNames)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentSecurityNames | java.util.Set |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
