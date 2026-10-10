---
title: "MultiplePagesType"
linktitle: "MultiplePagesType"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se imprime el documento en Java."
type: docs
weight: 473
url: /es/java/com.aspose.words/multiplepagestype/
---

**Inheritance:**
java.lang.Object
```
public class MultiplePagesType
```

Especifica cómo se imprime el documento.

 **Examples:** 

Muestra cómo configurar un documento que puede imprimirse como un pliegue de libro.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [BOOK_FOLD_PRINTING](#BOOK-FOLD-PRINTING) | Especifica si se debe imprimir el documento como un pliegue de libro. |
| [BOOK_FOLD_PRINTING_REVERSE](#BOOK-FOLD-PRINTING-REVERSE) | Especifica si se debe imprimir el documento como un pliegue de libro inverso. |
| [DEFAULT](#DEFAULT) | El valor predeterminado es [NORMAL](../../com.aspose.words/multiplepagestype/\#NORMAL) |
| [MIRROR_MARGINS](#MIRROR-MARGINS) | Intercambia los márgenes izquierdo y derecho en páginas enfrentadas. |
| [NORMAL](#NORMAL) | Impresión normal, sin páginas múltiples especificadas. |
| [TWO_PAGES_PER_SHEET](#TWO-PAGES-PER-SHEET) | Imprime dos páginas por hoja. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String multiplePagesTypeName)](#fromName-java.lang.String) |  |
| [getName(int multiplePagesType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int multiplePagesType)](#toString-int) |  |
### BOOK_FOLD_PRINTING {#BOOK-FOLD-PRINTING}
```
public static int BOOK_FOLD_PRINTING
```


Especifica si se debe imprimir el documento como un pliegue de libro.

### BOOK_FOLD_PRINTING_REVERSE {#BOOK-FOLD-PRINTING-REVERSE}
```
public static int BOOK_FOLD_PRINTING_REVERSE
```


Especifica si se debe imprimir el documento como un pliegue de libro inverso.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


El valor predeterminado es [NORMAL](../../com.aspose.words/multiplepagestype/\#NORMAL)

### MIRROR_MARGINS {#MIRROR-MARGINS}
```
public static int MIRROR_MARGINS
```


Intercambia los márgenes izquierdo y derecho en páginas enfrentadas.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Impresión normal, sin páginas múltiples especificadas.

### TWO_PAGES_PER_SHEET {#TWO-PAGES-PER-SHEET}
```
public static int TWO_PAGES_PER_SHEET
```


Imprime dos páginas por hoja.

### length {#length}
```
public static int length
```


### fromName(String multiplePagesTypeName) {#fromName-java.lang.String}
```
public static int fromName(String multiplePagesTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| multiplePagesTypeName | java.lang.String |  |

**Returns:**
int
### getName(int multiplePagesType) {#getName-int}
```
public static String getName(int multiplePagesType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| multiplePagesType | int |  |

**Returns:**
java.lang.String
