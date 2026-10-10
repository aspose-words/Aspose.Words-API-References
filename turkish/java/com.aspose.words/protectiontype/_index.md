---
title: "ProtectionType"
linktitle: "ProtectionType"
second_title: "Aspose.Words Java için"
description: "Java'da bir belge için koruma türü."
type: docs
weight: 556
url: /tr/java/com.aspose.words/protectiontype/
---

**Inheritance:**
java.lang.Object
```
public class ProtectionType
```

Bir belge için koruma türü.

 **Examples:** 

Bir bölüm için korumayı nasıl kapatacağınızı gösterir.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Section 1. Hello world!");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 builder.writeln("Section 2. Hello again!");
 builder.write("Please enter text here: ");
 builder.insertTextInput("TextInput1", TextFormFieldType.REGULAR, "", "Placeholder text", 0);

 // Apply write protection to every section in the document.
 doc.protect(ProtectionType.ALLOW_ONLY_FORM_FIELDS);

 // Turn off write protection for the first section.
 doc.getSections().get(0).setProtectedForForms(false);

 // In this output document, we will be able to edit the first section freely,
 // and we will only be able to edit the contents of the form field in the second section.
 doc.save(getArtifactsDir() + "Section.Protect.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [ALLOW_ONLY_COMMENTS](#ALLOW-ONLY-COMMENTS) | Kullanıcı yalnızca belgede yorumları değiştirebilir. |
| [ALLOW_ONLY_FORM_FIELDS](#ALLOW-ONLY-FORM-FIELDS) | Kullanıcı yalnızca belgede form alanlarına veri girebilir. |
| [ALLOW_ONLY_REVISIONS](#ALLOW-ONLY-REVISIONS) | Kullanıcı yalnızca belgeye revizyon işaretleri ekleyebilir. |
| [NO_PROTECTION](#NO-PROTECTION) | Belge korunmamaktadır. |
| [READ_ONLY](#READ-ONLY) | Belgeye hiçbir değişiklik yapılmasına izin verilmez. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String protectionTypeName)](#fromName-java.lang.String) |  |
| [getName(int protectionType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int protectionType)](#toString-int) |  |
### ALLOW_ONLY_COMMENTS {#ALLOW-ONLY-COMMENTS}
```
public static int ALLOW_ONLY_COMMENTS
```


Kullanıcı yalnızca belgede yorumları değiştirebilir.

### ALLOW_ONLY_FORM_FIELDS {#ALLOW-ONLY-FORM-FIELDS}
```
public static int ALLOW_ONLY_FORM_FIELDS
```


Kullanıcı yalnızca belgede form alanlarına veri girebilir.

### ALLOW_ONLY_REVISIONS {#ALLOW-ONLY-REVISIONS}
```
public static int ALLOW_ONLY_REVISIONS
```


Kullanıcı yalnızca belgeye revizyon işaretleri ekleyebilir.

### NO_PROTECTION {#NO-PROTECTION}
```
public static int NO_PROTECTION
```


Belge korunmamaktadır.

### READ_ONLY {#READ-ONLY}
```
public static int READ_ONLY
```


Belgeye hiçbir değişiklik yapılmasına izin verilmez. Microsoft Word 2003'ten beri kullanılabilir.

### length {#length}
```
public static int length
```


### fromName(String protectionTypeName) {#fromName-java.lang.String}
```
public static int fromName(String protectionTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| protectionTypeName | java.lang.String |  |

**Returns:**
int
### getName(int protectionType) {#getName-int}
```
public static String getName(int protectionType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| protectionType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int protectionType) {#toString-int}
```
public static String toString(int protectionType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| protectionType | int |  |

**Returns:**
java.lang.String
