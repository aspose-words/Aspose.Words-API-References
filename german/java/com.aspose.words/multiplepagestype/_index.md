---
title: "MultiplePagesType"
linktitle: "MultiplePagesType"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie das Dokument in Java gedruckt wird."
type: docs
weight: 473
url: /de/java/com.aspose.words/multiplepagestype/
---

**Inheritance:**
java.lang.Object
```
public class MultiplePagesType
```

Gibt an, wie das Dokument gedruckt wird.

 **Examples:** 

Zeigt, wie man ein Dokument konfiguriert, das als Buchfalz gedruckt werden kann.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [BOOK_FOLD_PRINTING](#BOOK-FOLD-PRINTING) | Gibt an, ob das Dokument als Buchfalz gedruckt werden soll. |
| [BOOK_FOLD_PRINTING_REVERSE](#BOOK-FOLD-PRINTING-REVERSE) | Gibt an, ob das Dokument als umgekehrter Buchfalz gedruckt werden soll. |
| [DEFAULT](#DEFAULT) | Standardwert ist [NORMAL](../../com.aspose.words/multiplepagestype/\#NORMAL) |
| [MIRROR_MARGINS](#MIRROR-MARGINS) | Vertauscht linke und rechte Ränder auf gegenüberliegenden Seiten. |
| [NORMAL](#NORMAL) | Normaler Druck, keine Mehrseitendrucke angegeben. |
| [TWO_PAGES_PER_SHEET](#TWO-PAGES-PER-SHEET) | Druckt zwei Seiten pro Blatt. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String multiplePagesTypeName)](#fromName-java.lang.String) |  |
| [getName(int multiplePagesType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int multiplePagesType)](#toString-int) |  |
### BOOK_FOLD_PRINTING {#BOOK-FOLD-PRINTING}
```
public static int BOOK_FOLD_PRINTING
```


Gibt an, ob das Dokument als Buchfalz gedruckt werden soll.

### BOOK_FOLD_PRINTING_REVERSE {#BOOK-FOLD-PRINTING-REVERSE}
```
public static int BOOK_FOLD_PRINTING_REVERSE
```


Gibt an, ob das Dokument als umgekehrter Buchfalz gedruckt werden soll.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Standardwert ist [NORMAL](../../com.aspose.words/multiplepagestype/\#NORMAL)

### MIRROR_MARGINS {#MIRROR-MARGINS}
```
public static int MIRROR_MARGINS
```


Vertauscht linke und rechte Ränder auf gegenüberliegenden Seiten.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Normaler Druck, keine Mehrseitendrucke angegeben.

### TWO_PAGES_PER_SHEET {#TWO-PAGES-PER-SHEET}
```
public static int TWO_PAGES_PER_SHEET
```


Druckt zwei Seiten pro Blatt.

### length {#length}
```
public static int length
```


### fromName(String multiplePagesTypeName) {#fromName-java.lang.String}
```
public static int fromName(String multiplePagesTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| multiplePagesTypeName | java.lang.String |  |

**Returns:**
int
### getName(int multiplePagesType) {#getName-int}
```
public static String getName(int multiplePagesType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| multiplePagesType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int multiplePagesType) {#toString-int}
```
public static String toString(int multiplePagesType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| multiplePagesType | int |  |

**Returns:**
java.lang.String
