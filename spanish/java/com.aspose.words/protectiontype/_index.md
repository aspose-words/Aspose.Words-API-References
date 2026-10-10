---
title: "ProtectionType"
linktitle: "ProtectionType"
second_title: "Aspose.Words para Java"
description: "Tipo de protección para un documento en Java."
type: docs
weight: 556
url: /es/java/com.aspose.words/protectiontype/
---

**Inheritance:**
java.lang.Object
```
public class ProtectionType
```

Tipo de protección para un documento.

 **Examples:** 

Muestra cómo desactivar la protección para una sección.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [ALLOW_ONLY_COMMENTS](#ALLOW-ONLY-COMMENTS) | El usuario solo puede modificar los comentarios en el documento. |
| [ALLOW_ONLY_FORM_FIELDS](#ALLOW-ONLY-FORM-FIELDS) | El usuario solo puede ingresar datos en los campos de formulario del documento. |
| [ALLOW_ONLY_REVISIONS](#ALLOW-ONLY-REVISIONS) | El usuario solo puede agregar marcas de revisión al documento. |
| [NO_PROTECTION](#NO-PROTECTION) | El documento no está protegido. |
| [READ_ONLY](#READ-ONLY) | No se permiten cambios en el documento. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String protectionTypeName)](#fromName-java.lang.String) |  |
| [getName(int protectionType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int protectionType)](#toString-int) |  |
### ALLOW_ONLY_COMMENTS {#ALLOW-ONLY-COMMENTS}
```
public static int ALLOW_ONLY_COMMENTS
```


El usuario solo puede modificar los comentarios en el documento.

### ALLOW_ONLY_FORM_FIELDS {#ALLOW-ONLY-FORM-FIELDS}
```
public static int ALLOW_ONLY_FORM_FIELDS
```


El usuario solo puede ingresar datos en los campos de formulario del documento.

### ALLOW_ONLY_REVISIONS {#ALLOW-ONLY-REVISIONS}
```
public static int ALLOW_ONLY_REVISIONS
```


El usuario solo puede agregar marcas de revisión al documento.

### NO_PROTECTION {#NO-PROTECTION}
```
public static int NO_PROTECTION
```


El documento no está protegido.

### READ_ONLY {#READ-ONLY}
```
public static int READ_ONLY
```


No se permiten cambios en el documento. Disponible desde Microsoft Word 2003.

### length {#length}
```
public static int length
```


### fromName(String protectionTypeName) {#fromName-java.lang.String}
```
public static int fromName(String protectionTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| protectionTypeName | java.lang.String |  |

**Returns:**
int
### getName(int protectionType) {#getName-int}
```
public static String getName(int protectionType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| protectionType | int |  |

**Returns:**
java.lang.String
