---
title: "ProtectionType"
linktitle: "ProtectionType"
second_title: "Aspose.Words لـ Java"
description: "نوع الحماية لمستند في جافا."
type: docs
weight: 556
url: /ar/java/com.aspose.words/protectiontype/
---

**Inheritance:**
java.lang.Object
```
public class ProtectionType
```

نوع الحماية للمستند.

 **Examples:** 

يوضح كيفية إيقاف الحماية لقسم.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [ALLOW_ONLY_COMMENTS](#ALLOW-ONLY-COMMENTS) | يمكن للمستخدم تعديل التعليقات فقط في المستند. |
| [ALLOW_ONLY_FORM_FIELDS](#ALLOW-ONLY-FORM-FIELDS) | يمكن للمستخدم إدخال البيانات فقط في حقول النموذج في المستند. |
| [ALLOW_ONLY_REVISIONS](#ALLOW-ONLY-REVISIONS) | يمكن للمستخدم إضافة علامات المراجعة فقط إلى المستند. |
| [NO_PROTECTION](#NO-PROTECTION) | المستند غير محمي. |
| [READ_ONLY](#READ-ONLY) | لا يُسمح بإجراء أي تغييرات على المستند. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String protectionTypeName)](#fromName-java.lang.String) |  |
| [getName(int protectionType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int protectionType)](#toString-int) |  |
### ALLOW_ONLY_COMMENTS {#ALLOW-ONLY-COMMENTS}
```
public static int ALLOW_ONLY_COMMENTS
```


يمكن للمستخدم تعديل التعليقات فقط في المستند.

### ALLOW_ONLY_FORM_FIELDS {#ALLOW-ONLY-FORM-FIELDS}
```
public static int ALLOW_ONLY_FORM_FIELDS
```


يمكن للمستخدم إدخال البيانات فقط في حقول النموذج في المستند.

### ALLOW_ONLY_REVISIONS {#ALLOW-ONLY-REVISIONS}
```
public static int ALLOW_ONLY_REVISIONS
```


يمكن للمستخدم إضافة علامات المراجعة فقط إلى المستند.

### NO_PROTECTION {#NO-PROTECTION}
```
public static int NO_PROTECTION
```


المستند غير محمي.

### READ_ONLY {#READ-ONLY}
```
public static int READ_ONLY
```


لا يُسمح بإجراء أي تغييرات على المستند. متاح منذ Microsoft Word 2003.

### length {#length}
```
public static int length
```


### fromName(String protectionTypeName) {#fromName-java.lang.String}
```
public static int fromName(String protectionTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| protectionTypeName | java.lang.String |  |

**Returns:**
int
### getName(int protectionType) {#getName-int}
```
public static String getName(int protectionType)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| protectionType | int |  |

**Returns:**
java.lang.String
