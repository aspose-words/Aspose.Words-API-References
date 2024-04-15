---
title: ProtectionType
linktitle: ProtectionType
second_title: Aspose.Words for Java
description: Protection type for a document in Java.
type: docs
weight: 507
url: /java/com.aspose.words/protectiontype/
---

**Inheritance:**
java.lang.Object
```
public class ProtectionType
```

Protection type for a document.

 **Examples:** 

Shows how to turn off protection for a section.

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
## Fields

| Field | Description |
| --- | --- |
| [ALLOW_ONLY_COMMENTS](#ALLOW-ONLY-COMMENTS) | User can only modify comments in the document. |
| [ALLOW_ONLY_FORM_FIELDS](#ALLOW-ONLY-FORM-FIELDS) | User can only enter data in the form fields in the document. |
| [ALLOW_ONLY_REVISIONS](#ALLOW-ONLY-REVISIONS) | User can only add revision marks to the document. |
| [NO_PROTECTION](#NO-PROTECTION) | The document is not protected. |
| [READ_ONLY](#READ-ONLY) | No changes are allowed to the document. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String protectionTypeName)](#fromName-java.lang.String) |  |
| [getName(int protectionType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int protectionType)](#toString-int) |  |
### ALLOW_ONLY_COMMENTS {#ALLOW-ONLY-COMMENTS}
```
public static int ALLOW_ONLY_COMMENTS
```


User can only modify comments in the document.

### ALLOW_ONLY_FORM_FIELDS {#ALLOW-ONLY-FORM-FIELDS}
```
public static int ALLOW_ONLY_FORM_FIELDS
```


User can only enter data in the form fields in the document.

### ALLOW_ONLY_REVISIONS {#ALLOW-ONLY-REVISIONS}
```
public static int ALLOW_ONLY_REVISIONS
```


User can only add revision marks to the document.

### NO_PROTECTION {#NO-PROTECTION}
```
public static int NO_PROTECTION
```


The document is not protected.

### READ_ONLY {#READ-ONLY}
```
public static int READ_ONLY
```


No changes are allowed to the document. Available since Microsoft Word 2003.

### length {#length}
```
public static int length
```


### fromName(String protectionTypeName) {#fromName-java.lang.String}
```
public static int fromName(String protectionTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| protectionTypeName | java.lang.String |  |

**Returns:**
int
### getName(int protectionType) {#getName-int}
```
public static String getName(int protectionType)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| protectionType | int |  |

**Returns:**
java.lang.String
