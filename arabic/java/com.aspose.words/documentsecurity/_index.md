---
title: "DocumentSecurity"
linktitle: "DocumentSecurity"
second_title: "Aspose.Words لـ Java"
description: "يُستخدم كقيمة لخاصية BuiltInDocumentProperties.getSecurity / BuiltInDocumentProperties.setSecurityint في Java."
type: docs
weight: 173
url: /ar/java/com.aspose.words/documentsecurity/
---

**Inheritance:**
java.lang.Object
```
public class DocumentSecurity
```

يُستخدم كقيمة لخاصية [BuiltInDocumentProperties.getSecurity()](../../com.aspose.words/builtindocumentproperties/\#getSecurity) / [BuiltInDocumentProperties.setSecurity(int)](../../com.aspose.words/builtindocumentproperties/\#setSecurity-int). يحدد مستوى أمان المستند كقيمة رقمية.

 **Examples:** 

يوضح كيفية استخدام خصائص المستند لعرض مستوى أمان المستند.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [NONE](#NONE) | لا توجد حالات أمان محددة بواسطة الخاصية. |
| [PASSWORD_PROTECTED](#PASSWORD-PROTECTED) | المستند محمي بكلمة مرور. |
| [READ_ONLY_ENFORCED](#READ-ONLY-ENFORCED) | المستند يُفتح دائمًا للقراءة فقط. |
| [READ_ONLY_EXCEPT_ANNOTATIONS](#READ-ONLY-EXCEPT-ANNOTATIONS) | المستند يُفتح دائمًا للقراءة فقط باستثناء التعليقات. |
| [READ_ONLY_RECOMMENDED](#READ-ONLY-RECOMMENDED) | المستند يُفتح للقراءة فقط إذا أمكن، ولكن يمكن تجاوز الإعداد. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
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


لا توجد حالات أمان محددة بواسطة الخاصية.

### PASSWORD_PROTECTED {#PASSWORD-PROTECTED}
```
public static int PASSWORD_PROTECTED
```


المستند محمي بكلمة مرور. (ملاحظة: لم يُرَ هذا أبداً في أي مستند حتى الآن).

### READ_ONLY_ENFORCED {#READ-ONLY-ENFORCED}
```
public static int READ_ONLY_ENFORCED
```


المستند يُفتح دائمًا للقراءة فقط.

### READ_ONLY_EXCEPT_ANNOTATIONS {#READ-ONLY-EXCEPT-ANNOTATIONS}
```
public static int READ_ONLY_EXCEPT_ANNOTATIONS
```


المستند يُفتح دائمًا للقراءة فقط باستثناء التعليقات.

### READ_ONLY_RECOMMENDED {#READ-ONLY-RECOMMENDED}
```
public static int READ_ONLY_RECOMMENDED
```


المستند يُفتح للقراءة فقط إذا أمكن، ولكن يمكن تجاوز الإعداد.

### length {#length}
```
public static int length
```


### fromName(String documentSecurityName) {#fromName-java.lang.String}
```
public static int fromName(String documentSecurityName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| documentSecurityName | java.lang.String |  |

**Returns:**
int
### fromNames(Set documentSecurityNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set documentSecurityNames)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| documentSecurityNames | java.util.Set |  |

**Returns:**
int
### getName(int documentSecurity) {#getName-int}
```
public static String getName(int documentSecurity)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| documentSecurity | int |  |

**Returns:**
java.lang.String
### getNames(int documentSecurity) {#getNames-int}
```
public static Set getNames(int documentSecurity)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| documentSecurity | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
