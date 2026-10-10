---
title: "DocumentSecurity"
linktitle: "DocumentSecurity"
second_title: "Aspose.Words Java için"
description: "Java'da BuiltInDocumentProperties.getSecurity / BuiltInDocumentProperties.setSecurityint özelliği için bir değer olarak kullanılır."
type: docs
weight: 173
url: /tr/java/com.aspose.words/documentsecurity/
---

**Inheritance:**
java.lang.Object
```
public class DocumentSecurity
```

Bu, [BuiltInDocumentProperties.getSecurity()](../../com.aspose.words/builtindocumentproperties/\#getSecurity) / [BuiltInDocumentProperties.setSecurity(int)](../../com.aspose.words/builtindocumentproperties/\#setSecurity-int) özelliği için bir değer olarak kullanılır. Bir belgenin güvenlik seviyesini sayısal bir değer olarak belirtir.

 **Examples:** 

Belge özelliklerini kullanarak bir belgenin güvenlik seviyesini nasıl göstereceğinizi gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [NONE](#NONE) | Bu özellik tarafından belirtilen güvenlik durumu yoktur. |
| [PASSWORD_PROTECTED](#PASSWORD-PROTECTED) | Belge şifre korumalıdır. |
| [READ_ONLY_ENFORCED](#READ-ONLY-ENFORCED) | Belge her zaman yalnızca okunur olarak açılmalıdır. |
| [READ_ONLY_EXCEPT_ANNOTATIONS](#READ-ONLY-EXCEPT-ANNOTATIONS) | Belge, açıklamalar hariç, her zaman yalnızca okunur olarak açılmalıdır. |
| [READ_ONLY_RECOMMENDED](#READ-ONLY-RECOMMENDED) | Belge mümkünse yalnızca okunur olarak açılmalıdır, ancak bu ayar geçersiz kılınabilir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String documentSecurityName)](#fromName-java.lang.String) |  |
| [fromNames(Set documentSecurityNames)](#fromNames-java.util.Set) |  |
| [getName(int documentSecurity)](#getName-int) |  |
| [getNames(int documentSecurity)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int documentSecurity)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Bu özellik tarafından belirtilen güvenlik durumu yoktur.

### PASSWORD_PROTECTED {#PASSWORD-PROTECTED}
```
public static int PASSWORD_PROTECTED
```


Belge şifre korumalıdır. (Not: Şimdiye kadar bir belgede hiç görülmemiştir.)

### READ_ONLY_ENFORCED {#READ-ONLY-ENFORCED}
```
public static int READ_ONLY_ENFORCED
```


Belge her zaman yalnızca okunur olarak açılmalıdır.

### READ_ONLY_EXCEPT_ANNOTATIONS {#READ-ONLY-EXCEPT-ANNOTATIONS}
```
public static int READ_ONLY_EXCEPT_ANNOTATIONS
```


Belge, açıklamalar hariç, her zaman yalnızca okunur olarak açılmalıdır.

### READ_ONLY_RECOMMENDED {#READ-ONLY-RECOMMENDED}
```
public static int READ_ONLY_RECOMMENDED
```


Belge mümkünse yalnızca okunur olarak açılmalıdır, ancak bu ayar geçersiz kılınabilir.

### length {#length}
```
public static int length
```


### fromName(String documentSecurityName) {#fromName-java.lang.String}
```
public static int fromName(String documentSecurityName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| documentSecurityName | java.lang.String |  |

**Returns:**
int
### fromNames(Set documentSecurityNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set documentSecurityNames)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| documentSecurityNames | java.util.Set |  |

**Returns:**
int
### getName(int documentSecurity) {#getName-int}
```
public static String getName(int documentSecurity)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| documentSecurity | int |  |

**Returns:**
java.lang.String
### getNames(int documentSecurity) {#getNames-int}
```
public static Set getNames(int documentSecurity)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
### toString(int documentSecurity) {#toString-int}
```
public static String toString(int documentSecurity)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| documentSecurity | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
