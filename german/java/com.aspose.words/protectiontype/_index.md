---
title: "ProtectionType"
linktitle: "ProtectionType"
second_title: "Aspose.Words für Java"
description: "Schutztyp für ein Dokument in Java."
type: docs
weight: 556
url: /de/java/com.aspose.words/protectiontype/
---

**Inheritance:**
java.lang.Object
```
public class ProtectionType
```

Schutztyp für ein Dokument.

 **Examples:** 

Zeigt, wie der Schutz für einen Abschnitt deaktiviert wird.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [ALLOW_ONLY_COMMENTS](#ALLOW-ONLY-COMMENTS) | Benutzer kann im Dokument nur Kommentare ändern. |
| [ALLOW_ONLY_FORM_FIELDS](#ALLOW-ONLY-FORM-FIELDS) | Benutzer kann im Dokument nur Daten in Formularfelder eingeben. |
| [ALLOW_ONLY_REVISIONS](#ALLOW-ONLY-REVISIONS) | Benutzer kann im Dokument nur Revisionsmarken hinzufügen. |
| [NO_PROTECTION](#NO-PROTECTION) | Das Dokument ist nicht geschützt. |
| [READ_ONLY](#READ-ONLY) | Keine Änderungen am Dokument sind erlaubt. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String protectionTypeName)](#fromName-java.lang.String) |  |
| [getName(int protectionType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int protectionType)](#toString-int) |  |
### ALLOW_ONLY_COMMENTS {#ALLOW-ONLY-COMMENTS}
```
public static int ALLOW_ONLY_COMMENTS
```


Benutzer kann im Dokument nur Kommentare ändern.

### ALLOW_ONLY_FORM_FIELDS {#ALLOW-ONLY-FORM-FIELDS}
```
public static int ALLOW_ONLY_FORM_FIELDS
```


Benutzer kann im Dokument nur Daten in Formularfelder eingeben.

### ALLOW_ONLY_REVISIONS {#ALLOW-ONLY-REVISIONS}
```
public static int ALLOW_ONLY_REVISIONS
```


Benutzer kann im Dokument nur Revisionsmarken hinzufügen.

### NO_PROTECTION {#NO-PROTECTION}
```
public static int NO_PROTECTION
```


Das Dokument ist nicht geschützt.

### READ_ONLY {#READ-ONLY}
```
public static int READ_ONLY
```


Keine Änderungen am Dokument sind erlaubt. Verfügbar seit Microsoft Word 2003.

### length {#length}
```
public static int length
```


### fromName(String protectionTypeName) {#fromName-java.lang.String}
```
public static int fromName(String protectionTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| protectionTypeName | java.lang.String |  |

**Returns:**
int
### getName(int protectionType) {#getName-int}
```
public static String getName(int protectionType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| protectionType | int |  |

**Returns:**
java.lang.String
