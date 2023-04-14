---
title: DocumentSecurity
linktitle: DocumentSecurity
second_title: Aspose.Words for Java API Reference
description: Used as a value for the BuiltInDocumentProperties.getSecurity / BuiltInDocumentProperties.setSecurityint property in Java.
type: docs
weight: 132
url: /java/com.aspose.words/documentsecurity/
---

**Inheritance:**
java.lang.Object
```
public class DocumentSecurity
```

Used as a value for the [BuiltInDocumentProperties.getSecurity()](../../com.aspose.words/builtindocumentproperties/\#getSecurity) / [BuiltInDocumentProperties.setSecurity(int)](../../com.aspose.words/builtindocumentproperties/\#setSecurity-int) property. Specifies the security level of a document as a numeric value.

 **Examples:** 

Shows how to use document properties to display the security level of a document.

```

 Document doc = new Document();

 Assert.assertEquals(DocumentSecurity.NONE, doc.getBuiltInDocumentProperties().getSecurity());

 // If we configure a document to be read-only, it will display this status using the "Security" built-in property.
 doc.getWriteProtection().setReadOnlyRecommended(true);
 doc.save(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyRecommended.docx");

 Assert.assertEquals(DocumentSecurity.READ_ONLY_RECOMMENDED,
         new Document(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyRecommended.docx").getBuiltInDocumentProperties().getSecurity());

 // Write-protect a document, and then verify its security level.
 doc = new Document();

 Assert.assertFalse(doc.getWriteProtection().isWriteProtected());

 doc.getWriteProtection().setPassword("MyPassword");

 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));
 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 doc.save(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyEnforced.docx");

 Assert.assertEquals(DocumentSecurity.READ_ONLY_ENFORCED,
         new Document(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyEnforced.docx").getBuiltInDocumentProperties().getSecurity());

 // "Security" is a descriptive property. We can edit its value manually.
 doc = new Document();

 doc.protect(ProtectionType.ALLOW_ONLY_COMMENTS, "MyPassword");
 doc.getBuiltInDocumentProperties().setSecurity(DocumentSecurity.READ_ONLY_EXCEPT_ANNOTATIONS);
 doc.save(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

 Assert.assertEquals(DocumentSecurity.READ_ONLY_EXCEPT_ANNOTATIONS,
         new Document(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx").getBuiltInDocumentProperties().getSecurity());
 
```
## Fields

| Field | Description |
| --- | --- |
| [NONE](#NONE) | There are no security states specified by the property. |
| [PASSWORD_PROTECTED](#PASSWORD-PROTECTED) | The document is password protected. |
| [READ_ONLY_ENFORCED](#READ-ONLY-ENFORCED) | The document to always be opened read-only. |
| [READ_ONLY_EXCEPT_ANNOTATIONS](#READ-ONLY-EXCEPT-ANNOTATIONS) | The document to always be opened read-only except for annotations. |
| [READ_ONLY_RECOMMENDED](#READ-ONLY-RECOMMENDED) | The document to be opened read-only if possible, but the setting can be overridden. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String documentSecurityName)](#fromName-java.lang.String) |  |
| [fromNames(Set documentSecurityNames)](#fromNames-java.util.Set) |  |
| [getClass()](#getClass) |  |
| [getName(int documentSecurity)](#getName-int) |  |
| [getNames(int documentSecurity)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int documentSecurity)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
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

### READ_ONLY_RECOMMENDED {#READ-ONLY-RECOMMENDED}
```
public static int READ_ONLY_RECOMMENDED
```


The document to be opened read-only if possible, but the setting can be overridden.

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
### fromName(String documentSecurityName) {#fromName-java.lang.String}
```
public static int fromName(String documentSecurityName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentSecurityName | java.lang.String |  |

**Returns:**
int
### fromNames(Set documentSecurityNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set documentSecurityNames)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentSecurityNames | java.util.Set |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int documentSecurity) {#getName-int}
```
public static String getName(int documentSecurity)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentSecurity | int |  |

**Returns:**
java.lang.String
### getNames(int documentSecurity) {#getNames-int}
```
public static Set getNames(int documentSecurity)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentSecurity | int |  |

**Returns:**
java.util.Set
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
### toString(int documentSecurity) {#toString-int}
```
public static String toString(int documentSecurity)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentSecurity | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| attr | int |  |

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

