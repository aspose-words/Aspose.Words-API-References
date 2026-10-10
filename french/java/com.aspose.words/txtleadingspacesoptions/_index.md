---
title: "TxtLeadingSpacesOptions"
linktitle: "TxtLeadingSpacesOptions"
second_title: "Aspose.Words pour Java"
description: "Spécifie les options disponibles pour la gestion des espaces de tête lors de l’importation depuis le fichier LoadFormat.TEXT en Java."
type: docs
weight: 691
url: /fr/java/com.aspose.words/txtleadingspacesoptions/
---

**Inheritance:**
java.lang.Object
```
public class TxtLeadingSpacesOptions
```

Spécifie les options disponibles pour la gestion des espaces de tête lors de l’importation depuis le fichier [LoadFormat.TEXT](../../com.aspose.words/loadformat/\#TEXT).

 **Examples:** 

Montre comment supprimer les espaces blancs lors du chargement de documents texte brut.

```

 String textDoc = "      Line 1 \n" +
         "    Line 2   \n" +
         " Line 3       ";

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Preserve"
 // to preserve all whitespace characters at the start of every line.
 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.ConvertToIndent"
 // to remove all whitespace characters from the start of every line,
 // and then apply a left first line indent to the paragraph to simulate the effect of the whitespaces.
 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Trim"
 // to remove all whitespace characters from every line's start.
 loadOptions.setLeadingSpacesOptions(txtLeadingSpacesOptions);

 // Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Preserve"
 // to preserve all whitespace characters at the end of every line.
 // Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Trim" to
 // remove all whitespace characters from the end of every line.
 loadOptions.setTrailingSpacesOptions(txtTrailingSpacesOptions);

 Document doc = new Document(new ByteArrayInputStream(textDoc.getBytes()), loadOptions);
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 switch (txtLeadingSpacesOptions) {
     case TxtLeadingSpacesOptions.CONVERT_TO_INDENT:
         Assert.assertEquals(37.8d, paragraphs.get(0).getParagraphFormat().getFirstLineIndent());
         Assert.assertEquals(25.2d, paragraphs.get(1).getParagraphFormat().getFirstLineIndent());
         Assert.assertEquals(6.3d, paragraphs.get(2).getParagraphFormat().getFirstLineIndent());

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith("Line 3"));
         break;
     case TxtLeadingSpacesOptions.PRESERVE:
         Assert.assertTrue(IterableUtils.matchesAll(paragraphs, s -> s.getParagraphFormat().getFirstLineIndent() == 0.0d));

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("      Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("    Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith(" Line 3"));
         break;
     case TxtLeadingSpacesOptions.TRIM:
         Assert.assertTrue(IterableUtils.matchesAll(paragraphs, s -> s.getParagraphFormat().getFirstLineIndent() == 0.0d));

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith("Line 3"));
         break;
 }

 switch (txtTrailingSpacesOptions) {
     case TxtTrailingSpacesOptions.PRESERVE:
         Assert.assertTrue(paragraphs.get(0).getText().endsWith("Line 1 \r"));
         Assert.assertTrue(paragraphs.get(1).getText().endsWith("Line 2   \r"));
         Assert.assertTrue(paragraphs.get(2).getText().endsWith("Line 3       \f"));
         break;
     case TxtTrailingSpacesOptions.TRIM:
         Assert.assertTrue(paragraphs.get(0).getText().endsWith("Line 1\r"));
         Assert.assertTrue(paragraphs.get(1).getText().endsWith("Line 2\r"));
         Assert.assertTrue(paragraphs.get(2).getText().endsWith("Line 3\f"));
         break;
 }
 
```
## Champs

| Champ | Description |
| --- | --- |
| [CONVERT_TO_INDENT](#CONVERT-TO-INDENT) | Les espaces de tête sont supprimés et convertis en retrait gauche. |
| [PRESERVE](#PRESERVE) | Les espaces de tête sont conservés. |
| [TRIM](#TRIM) | Les espaces de tête sont tronqués |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String txtLeadingSpacesOptionsName)](#fromName-java.lang.String) |  |
| [getName(int txtLeadingSpacesOptions)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int txtLeadingSpacesOptions)](#toString-int) |  |
### CONVERT_TO_INDENT {#CONVERT-TO-INDENT}
```
public static int CONVERT_TO_INDENT
```


Les espaces de tête sont supprimés et convertis en retrait gauche.

### PRESERVE {#PRESERVE}
```
public static int PRESERVE
```


Les espaces de tête sont conservés.

### TRIM {#TRIM}
```
public static int TRIM
```


Les espaces de tête sont tronqués

### length {#length}
```
public static int length
```


### fromName(String txtLeadingSpacesOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String txtLeadingSpacesOptionsName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| txtLeadingSpacesOptionsName | java.lang.String |  |

**Returns:**
int
### getName(int txtLeadingSpacesOptions) {#getName-int}
```
public static String getName(int txtLeadingSpacesOptions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| txtLeadingSpacesOptions | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int txtLeadingSpacesOptions) {#toString-int}
```
public static String toString(int txtLeadingSpacesOptions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| txtLeadingSpacesOptions | int |  |

**Returns:**
java.lang.String
