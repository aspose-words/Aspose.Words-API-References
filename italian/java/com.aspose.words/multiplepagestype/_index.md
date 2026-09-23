---
title: "MultiplePagesType"
linktitle: "MultiplePagesType"
second_title: "Aspose.Words per Java"
description: "Specifica come il documento viene stampato in Java."
type: docs
weight: 473
url: /it/java/com.aspose.words/multiplepagestype/
---

**Inheritance:**
java.lang.Object
```
public class MultiplePagesType
```

Specifica come il documento viene stampato.

 **Examples:** 

Mostra come configurare un documento che può essere stampato come piega a libro.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [BOOK_FOLD_PRINTING](#BOOK-FOLD-PRINTING) | Specifica se stampare il documento come piega a libro. |
| [BOOK_FOLD_PRINTING_REVERSE](#BOOK-FOLD-PRINTING-REVERSE) | Specifica se stampare il documento come piega a libro inversa. |
| [DEFAULT](#DEFAULT) | Il valore predefinito è [NORMAL](../../com.aspose.words/multiplepagestype/\#NORMAL) |
| [MIRROR_MARGINS](#MIRROR-MARGINS) | Scambia i margini sinistro e destro nelle pagine affiancate. |
| [NORMAL](#NORMAL) | Stampa normale, nessuna pagina multipla specificata. |
| [TWO_PAGES_PER_SHEET](#TWO-PAGES-PER-SHEET) | Stampa due pagine per foglio. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String multiplePagesTypeName)](#fromName-java.lang.String) |  |
| [getName(int multiplePagesType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int multiplePagesType)](#toString-int) |  |
### BOOK_FOLD_PRINTING {#BOOK-FOLD-PRINTING}
```
public static int BOOK_FOLD_PRINTING
```


Specifica se stampare il documento come piega a libro.

### BOOK_FOLD_PRINTING_REVERSE {#BOOK-FOLD-PRINTING-REVERSE}
```
public static int BOOK_FOLD_PRINTING_REVERSE
```


Specifica se stampare il documento come piega a libro inversa.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Il valore predefinito è [NORMAL](../../com.aspose.words/multiplepagestype/\#NORMAL)

### MIRROR_MARGINS {#MIRROR-MARGINS}
```
public static int MIRROR_MARGINS
```


Scambia i margini sinistro e destro nelle pagine affiancate.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Stampa normale, nessuna pagina multipla specificata.

### TWO_PAGES_PER_SHEET {#TWO-PAGES-PER-SHEET}
```
public static int TWO_PAGES_PER_SHEET
```


Stampa due pagine per foglio.

### length {#length}
```
public static int length
```


### fromName(String multiplePagesTypeName) {#fromName-java.lang.String}
```
public static int fromName(String multiplePagesTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| multiplePagesTypeName | java.lang.String |  |

**Returns:**
int
### getName(int multiplePagesType) {#getName-int}
```
public static String getName(int multiplePagesType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| multiplePagesType | int |  |

**Returns:**
java.lang.String
