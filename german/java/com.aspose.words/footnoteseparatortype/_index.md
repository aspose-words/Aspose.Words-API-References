---
title: "FootnoteSeparatorType"
linktitle: "FootnoteSeparatorType"
second_title: "Aspose.Words für Java"
description: "Gibt den Typ des Fußnoten-/Endnoten‑Trennzeichens in Java an."
type: docs
weight: 345
url: /de/java/com.aspose.words/footnoteseparatortype/
---

**Inheritance:**
java.lang.Object
```
public class FootnoteSeparatorType
```

Gibt den Typ des Fußnoten-/Endnoten-Trennzeichens an.

 **Examples:** 

Zeigt, wie das Endnoten‑Trennzeichen entfernt wird.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");

 FootnoteSeparator endnoteSeparator = doc.getFootnoteSeparators().getByFootnoteSeparatorType(FootnoteSeparatorType.ENDNOTE_SEPARATOR);
 // Remove endnote separator.
 endnoteSeparator.getFirstParagraph().getFirstChild().remove();
 
```

Zeigt, wie das Format des Fußnotentrennzeichens verwaltet wird.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");

 FootnoteSeparator footnoteSeparator = doc.getFootnoteSeparators().getByFootnoteSeparatorType(FootnoteSeparatorType.FOOTNOTE_SEPARATOR);
 // Align footnote separator.
 footnoteSeparator.getFirstParagraph().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [ENDNOTE_CONTINUATION_NOTICE](#ENDNOTE-CONTINUATION-NOTICE) | Wird unter dem Endnotentext auf einer Seite gedruckt, wenn der Endnotentext auf einer folgenden Seite fortgesetzt werden muss. |
| [ENDNOTE_CONTINUATION_SEPARATOR](#ENDNOTE-CONTINUATION-SEPARATOR) | Wird über dem Endnotentext auf einer Seite gedruckt, wenn der Text von einer vorherigen Seite fortgesetzt werden muss. |
| [ENDNOTE_SEPARATOR](#ENDNOTE-SEPARATOR) | Trennzeichen zwischen Haupttext und Endnotentext. |
| [FOOTNOTE_CONTINUATION_NOTICE](#FOOTNOTE-CONTINUATION-NOTICE) | Wird unter dem Fußnotentext auf einer Seite gedruckt, wenn der Fußnotentext auf einer folgenden Seite fortgesetzt werden muss. |
| [FOOTNOTE_CONTINUATION_SEPARATOR](#FOOTNOTE-CONTINUATION-SEPARATOR) | Wird über dem Fußnotentext auf einer Seite gedruckt, wenn der Text von einer vorherigen Seite fortgesetzt werden muss. |
| [FOOTNOTE_SEPARATOR](#FOOTNOTE-SEPARATOR) | Trennzeichen zwischen Haupttext und Fußnotentext. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String footnoteSeparatorTypeName)](#fromName-java.lang.String) |  |
| [getName(int footnoteSeparatorType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int footnoteSeparatorType)](#toString-int) |  |
### ENDNOTE_CONTINUATION_NOTICE {#ENDNOTE-CONTINUATION-NOTICE}
```
public static int ENDNOTE_CONTINUATION_NOTICE
```


Wird unter dem Endnotentext auf einer Seite gedruckt, wenn der Endnotentext auf einer folgenden Seite fortgesetzt werden muss.

### ENDNOTE_CONTINUATION_SEPARATOR {#ENDNOTE-CONTINUATION-SEPARATOR}
```
public static int ENDNOTE_CONTINUATION_SEPARATOR
```


Wird über dem Endnotentext auf einer Seite gedruckt, wenn der Text von einer vorherigen Seite fortgesetzt werden muss.

### ENDNOTE_SEPARATOR {#ENDNOTE-SEPARATOR}
```
public static int ENDNOTE_SEPARATOR
```


Trennzeichen zwischen Haupttext und Endnotentext.

### FOOTNOTE_CONTINUATION_NOTICE {#FOOTNOTE-CONTINUATION-NOTICE}
```
public static int FOOTNOTE_CONTINUATION_NOTICE
```


Wird unter dem Fußnotentext auf einer Seite gedruckt, wenn der Fußnotentext auf einer folgenden Seite fortgesetzt werden muss.

### FOOTNOTE_CONTINUATION_SEPARATOR {#FOOTNOTE-CONTINUATION-SEPARATOR}
```
public static int FOOTNOTE_CONTINUATION_SEPARATOR
```


Wird über dem Fußnotentext auf einer Seite gedruckt, wenn der Text von einer vorherigen Seite fortgesetzt werden muss.

### FOOTNOTE_SEPARATOR {#FOOTNOTE-SEPARATOR}
```
public static int FOOTNOTE_SEPARATOR
```


Trennzeichen zwischen Haupttext und Fußnotentext.

### length {#length}
```
public static int length
```


### fromName(String footnoteSeparatorTypeName) {#fromName-java.lang.String}
```
public static int fromName(String footnoteSeparatorTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| footnoteSeparatorTypeName | java.lang.String |  |

**Returns:**
int
### getName(int footnoteSeparatorType) {#getName-int}
```
public static String getName(int footnoteSeparatorType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| footnoteSeparatorType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int footnoteSeparatorType) {#toString-int}
```
public static String toString(int footnoteSeparatorType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| footnoteSeparatorType | int |  |

**Returns:**
java.lang.String
