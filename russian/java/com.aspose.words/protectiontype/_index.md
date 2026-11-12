---
title: "ProtectionType"
linktitle: "ProtectionType"
second_title: "Aspose.Words для Java"
description: "Тип защиты для документа в Java."
type: docs
weight: 556
url: /ru/java/com.aspose.words/protectiontype/
---

**Inheritance:**
java.lang.Object
```
public class ProtectionType
```

Тип защиты документа.

 **Examples:** 

Показывает, как отключить защиту раздела.

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
## Поля

| Поле | Описание |
| --- | --- |
| [ALLOW_ONLY_COMMENTS](#ALLOW-ONLY-COMMENTS) | Пользователь может только изменять комментарии в документе. |
| [ALLOW_ONLY_FORM_FIELDS](#ALLOW-ONLY-FORM-FIELDS) | Пользователь может только вводить данные в поля формы в документе. |
| [ALLOW_ONLY_REVISIONS](#ALLOW-ONLY-REVISIONS) | Пользователь может только добавлять метки правок в документ. |
| [NO_PROTECTION](#NO-PROTECTION) | Документ не защищён. |
| [READ_ONLY](#READ-ONLY) | Изменения в документе не разрешены. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String protectionTypeName)](#fromName-java.lang.String) |  |
| [getName(int protectionType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int protectionType)](#toString-int) |  |
### ALLOW_ONLY_COMMENTS {#ALLOW-ONLY-COMMENTS}
```
public static int ALLOW_ONLY_COMMENTS
```


Пользователь может только изменять комментарии в документе.

### ALLOW_ONLY_FORM_FIELDS {#ALLOW-ONLY-FORM-FIELDS}
```
public static int ALLOW_ONLY_FORM_FIELDS
```


Пользователь может только вводить данные в поля формы в документе.

### ALLOW_ONLY_REVISIONS {#ALLOW-ONLY-REVISIONS}
```
public static int ALLOW_ONLY_REVISIONS
```


Пользователь может только добавлять метки правок в документ.

### NO_PROTECTION {#NO-PROTECTION}
```
public static int NO_PROTECTION
```


Документ не защищён.

### READ_ONLY {#READ-ONLY}
```
public static int READ_ONLY
```


Изменения в документе не разрешены. Доступно, начиная с Microsoft Word 2003.

### length {#length}
```
public static int length
```


### fromName(String protectionTypeName) {#fromName-java.lang.String}
```
public static int fromName(String protectionTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| protectionTypeName | java.lang.String |  |

**Returns:**
int
### getName(int protectionType) {#getName-int}
```
public static String getName(int protectionType)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| protectionType | int |  |

**Returns:**
java.lang.String
