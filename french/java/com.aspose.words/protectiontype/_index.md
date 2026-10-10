---
title: "ProtectionType"
linktitle: "ProtectionType"
second_title: "Aspose.Words pour Java"
description: "Type de protection pour un document en Java."
type: docs
weight: 556
url: /fr/java/com.aspose.words/protectiontype/
---

**Inheritance:**
java.lang.Object
```
public class ProtectionType
```

Type de protection d'un document.

 **Examples:** 

Montre comment désactiver la protection d'une section.

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
## Champs

| Champ | Description |
| --- | --- |
| [ALLOW_ONLY_COMMENTS](#ALLOW-ONLY-COMMENTS) | L'utilisateur ne peut modifier que les commentaires dans le document. |
| [ALLOW_ONLY_FORM_FIELDS](#ALLOW-ONLY-FORM-FIELDS) | L'utilisateur ne peut saisir que des données dans les champs de formulaire du document. |
| [ALLOW_ONLY_REVISIONS](#ALLOW-ONLY-REVISIONS) | L'utilisateur ne peut ajouter que des marques de révision au document. |
| [NO_PROTECTION](#NO-PROTECTION) | Le document n'est pas protégé. |
| [READ_ONLY](#READ-ONLY) | Aucune modification n'est autorisée sur le document. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String protectionTypeName)](#fromName-java.lang.String) |  |
| [getName(int protectionType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int protectionType)](#toString-int) |  |
### ALLOW_ONLY_COMMENTS {#ALLOW-ONLY-COMMENTS}
```
public static int ALLOW_ONLY_COMMENTS
```


L'utilisateur ne peut modifier que les commentaires dans le document.

### ALLOW_ONLY_FORM_FIELDS {#ALLOW-ONLY-FORM-FIELDS}
```
public static int ALLOW_ONLY_FORM_FIELDS
```


L'utilisateur ne peut saisir que des données dans les champs de formulaire du document.

### ALLOW_ONLY_REVISIONS {#ALLOW-ONLY-REVISIONS}
```
public static int ALLOW_ONLY_REVISIONS
```


L'utilisateur ne peut ajouter que des marques de révision au document.

### NO_PROTECTION {#NO-PROTECTION}
```
public static int NO_PROTECTION
```


Le document n'est pas protégé.

### READ_ONLY {#READ-ONLY}
```
public static int READ_ONLY
```


Aucune modification n'est autorisée sur le document. Disponible depuis Microsoft Word 2003.

### length {#length}
```
public static int length
```


### fromName(String protectionTypeName) {#fromName-java.lang.String}
```
public static int fromName(String protectionTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| protectionTypeName | java.lang.String |  |

**Returns:**
int
### getName(int protectionType) {#getName-int}
```
public static String getName(int protectionType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| protectionType | int |  |

**Returns:**
java.lang.String
