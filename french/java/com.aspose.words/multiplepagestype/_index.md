---
title: "MultiplePagesType"
linktitle: "MultiplePagesType"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment le document est imprimé en Java."
type: docs
weight: 473
url: /fr/java/com.aspose.words/multiplepagestype/
---

**Inheritance:**
java.lang.Object
```
public class MultiplePagesType
```

Spécifie comment le document est imprimé.

 **Examples:** 

Montre comment configurer un document qui peut être imprimé en pliage de livre.

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
## Champs

| Champ | Description |
| --- | --- |
| [BOOK_FOLD_PRINTING](#BOOK-FOLD-PRINTING) | Spécifie si le document doit être imprimé en pliage de livre. |
| [BOOK_FOLD_PRINTING_REVERSE](#BOOK-FOLD-PRINTING-REVERSE) | Spécifie si le document doit être imprimé en pliage de livre inversé. |
| [DEFAULT](#DEFAULT) | La valeur par défaut est [NORMAL](../../com.aspose.words/multiplepagestype/\#NORMAL) |
| [MIRROR_MARGINS](#MIRROR-MARGINS) | Échange les marges gauche et droite sur les pages en vis-à-vis. |
| [NORMAL](#NORMAL) | Impression normale, aucune page multiple spécifiée. |
| [TWO_PAGES_PER_SHEET](#TWO-PAGES-PER-SHEET) | Imprime deux pages par feuille. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String multiplePagesTypeName)](#fromName-java.lang.String) |  |
| [getName(int multiplePagesType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int multiplePagesType)](#toString-int) |  |
### BOOK_FOLD_PRINTING {#BOOK-FOLD-PRINTING}
```
public static int BOOK_FOLD_PRINTING
```


Spécifie si le document doit être imprimé en pliage de livre.

### BOOK_FOLD_PRINTING_REVERSE {#BOOK-FOLD-PRINTING-REVERSE}
```
public static int BOOK_FOLD_PRINTING_REVERSE
```


Spécifie si le document doit être imprimé en pliage de livre inversé.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


La valeur par défaut est [NORMAL](../../com.aspose.words/multiplepagestype/\#NORMAL)

### MIRROR_MARGINS {#MIRROR-MARGINS}
```
public static int MIRROR_MARGINS
```


Échange les marges gauche et droite sur les pages en vis-à-vis.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Impression normale, aucune page multiple spécifiée.

### TWO_PAGES_PER_SHEET {#TWO-PAGES-PER-SHEET}
```
public static int TWO_PAGES_PER_SHEET
```


Imprime deux pages par feuille.

### length {#length}
```
public static int length
```


### fromName(String multiplePagesTypeName) {#fromName-java.lang.String}
```
public static int fromName(String multiplePagesTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| multiplePagesTypeName | java.lang.String |  |

**Returns:**
int
### getName(int multiplePagesType) {#getName-int}
```
public static String getName(int multiplePagesType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| multiplePagesType | int |  |

**Returns:**
java.lang.String
