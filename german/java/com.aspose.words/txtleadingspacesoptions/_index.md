---
title: "TxtLeadingSpacesOptions"
linktitle: "TxtLeadingSpacesOptions"
second_title: "Aspose.Words für Java"
description: "Gibt die verfügbaren Optionen für die Behandlung von führenden Leerzeichen beim Import aus einer LoadFormat.TEXT-Datei in Java an."
type: docs
weight: 691
url: /de/java/com.aspose.words/txtleadingspacesoptions/
---

**Inheritance:**
java.lang.Object
```
public class TxtLeadingSpacesOptions
```

Gibt die verfügbaren Optionen für die Behandlung von führenden Leerzeichen beim Import aus der Datei [LoadFormat.TEXT](../../com.aspose.words/loadformat/\#TEXT) an.

 **Examples:** 

Zeigt, wie Leerzeichen beim Laden von Nur-Text-Dokumenten getrimmt werden.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CONVERT_TO_INDENT](#CONVERT-TO-INDENT) | Führende Leerzeichen werden entfernt und in einen linken Einzug umgewandelt. |
| [PRESERVE](#PRESERVE) | Führende Leerzeichen werden beibehalten. |
| [TRIM](#TRIM) | Führende Leerzeichen werden gekürzt |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String txtLeadingSpacesOptionsName)](#fromName-java.lang.String) |  |
| [getName(int txtLeadingSpacesOptions)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int txtLeadingSpacesOptions)](#toString-int) |  |
### CONVERT_TO_INDENT {#CONVERT-TO-INDENT}
```
public static int CONVERT_TO_INDENT
```


Führende Leerzeichen werden entfernt und in einen linken Einzug umgewandelt.

### PRESERVE {#PRESERVE}
```
public static int PRESERVE
```


Führende Leerzeichen werden beibehalten.

### TRIM {#TRIM}
```
public static int TRIM
```


Führende Leerzeichen werden gekürzt

### length {#length}
```
public static int length
```


### fromName(String txtLeadingSpacesOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String txtLeadingSpacesOptionsName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| txtLeadingSpacesOptionsName | java.lang.String |  |

**Returns:**
int
### getName(int txtLeadingSpacesOptions) {#getName-int}
```
public static String getName(int txtLeadingSpacesOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| txtLeadingSpacesOptions | int |  |

**Returns:**
java.lang.String
