---
title: "ProtectionType"
linktitle: "ProtectionType"
second_title: "Aspose.Words per Java"
description: "Tipo di protezione per un documento in Java."
type: docs
weight: 556
url: /it/java/com.aspose.words/protectiontype/
---

**Inheritance:**
java.lang.Object
```
public class ProtectionType
```

Tipo di protezione per un documento.

 **Examples:** 

Mostra come disattivare la protezione per una sezione.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [ALLOW_ONLY_COMMENTS](#ALLOW-ONLY-COMMENTS) | L'utente può modificare solo i commenti nel documento. |
| [ALLOW_ONLY_FORM_FIELDS](#ALLOW-ONLY-FORM-FIELDS) | L'utente può inserire dati solo nei campi modulo del documento. |
| [ALLOW_ONLY_REVISIONS](#ALLOW-ONLY-REVISIONS) | L'utente può aggiungere solo segni di revisione al documento. |
| [NO_PROTECTION](#NO-PROTECTION) | Il documento non è protetto. |
| [READ_ONLY](#READ-ONLY) | Non sono consentite modifiche al documento. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String protectionTypeName)](#fromName-java.lang.String) |  |
| [getName(int protectionType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int protectionType)](#toString-int) |  |
### ALLOW_ONLY_COMMENTS {#ALLOW-ONLY-COMMENTS}
```
public static int ALLOW_ONLY_COMMENTS
```


L'utente può modificare solo i commenti nel documento.

### ALLOW_ONLY_FORM_FIELDS {#ALLOW-ONLY-FORM-FIELDS}
```
public static int ALLOW_ONLY_FORM_FIELDS
```


L'utente può inserire dati solo nei campi modulo del documento.

### ALLOW_ONLY_REVISIONS {#ALLOW-ONLY-REVISIONS}
```
public static int ALLOW_ONLY_REVISIONS
```


L'utente può aggiungere solo segni di revisione al documento.

### NO_PROTECTION {#NO-PROTECTION}
```
public static int NO_PROTECTION
```


Il documento non è protetto.

### READ_ONLY {#READ-ONLY}
```
public static int READ_ONLY
```


Non sono consentite modifiche al documento. Disponibile a partire da Microsoft Word 2003.

### length {#length}
```
public static int length
```


### fromName(String protectionTypeName) {#fromName-java.lang.String}
```
public static int fromName(String protectionTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| protectionTypeName | java.lang.String |  |

**Returns:**
int
### getName(int protectionType) {#getName-int}
```
public static String getName(int protectionType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| protectionType | int |  |

**Returns:**
java.lang.String
