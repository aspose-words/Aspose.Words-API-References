---
title: "TextColumn"
linktitle: "TextColumn"
second_title: "Aspose.Words per Java"
description: "Rappresenta una singola colonna di testo in Java."
type: docs
weight: 670
url: /it/java/com.aspose.words/textcolumn/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class TextColumn implements Cloneable
```

Rappresenta una singola colonna di testo. [TextColumn](../../com.aspose.words/textcolumn/) è un membro della collezione [TextColumnCollection](../../com.aspose.words/textcolumncollection/). La collezione [TextColumn](../../com.aspose.words/textcolumn/) include tutte le colonne in una sezione di un documento.

Per saperne di più, visita l'articolo della documentazione [ Working with Sections ][Working with Sections].

 **Remarks:** 

[TextColumn](../../com.aspose.words/textcolumn/) objects are only used to specify columns with custom width and spacing. If you want the columns in the document to be of equal width, set TextColumns. [TextColumnCollection.getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [TextColumnCollection.setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) to  true .

Quando viene creata una nuova [TextColumn](../../com.aspose.words/textcolumn/) la sua larghezza e spaziatura sono impostate a zero.

 **Examples:** 

Mostra come creare colonne con spaziatura non uniforme.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 PageSetup pageSetup = builder.getPageSetup();

 TextColumnCollection columns = pageSetup.getTextColumns();
 columns.setEvenlySpaced(false);
 columns.setCount(2);

 // Determine the amount of room that we have available for arranging columns.
 double contentWidth = pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin();

 Assert.assertEquals(468.0d, contentWidth, 0.01d);

 // Set the first column to be narrow.
 TextColumn column = columns.get(0);
 column.setWidth(100.0);
 column.setSpaceAfter(20.0);

 // Set the second column to take the rest of the space available within the margins of the page.
 column = columns.get(1);
 column.setWidth(contentWidth - column.getWidth() - column.getSpaceAfter());

 builder.writeln("Narrow column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Wide column 2.");

 doc.save(getArtifactsDir() + "PageSetup.CustomColumnWidth.docx");
 
```


[Working with Sections]: https://docs.aspose.com/words/java/working-with-sections/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getSpaceAfter()](#getSpaceAfter) | Restituisce lo spazio tra questa colonna e la colonna successiva in punti. |
| [getWidth()](#getWidth) | Restituisce la larghezza della colonna di testo in punti. |
| [setSpaceAfter(double value)](#setSpaceAfter-double) | Imposta lo spazio tra questa colonna e la colonna successiva in punti. |
| [setWidth(double value)](#setWidth-double) | Imposta la larghezza della colonna di testo in punti. |
### getSpaceAfter() {#getSpaceAfter}
```
public double getSpaceAfter()
```


Restituisce lo spazio tra questa colonna e la colonna successiva in punti. Non richiesto per l'ultima colonna.

 **Examples:** 

Mostra come creare colonne con spaziatura non uniforme.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 PageSetup pageSetup = builder.getPageSetup();

 TextColumnCollection columns = pageSetup.getTextColumns();
 columns.setEvenlySpaced(false);
 columns.setCount(2);

 // Determine the amount of room that we have available for arranging columns.
 double contentWidth = pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin();

 Assert.assertEquals(468.0d, contentWidth, 0.01d);

 // Set the first column to be narrow.
 TextColumn column = columns.get(0);
 column.setWidth(100.0);
 column.setSpaceAfter(20.0);

 // Set the second column to take the rest of the space available within the margins of the page.
 column = columns.get(1);
 column.setWidth(contentWidth - column.getWidth() - column.getSpaceAfter());

 builder.writeln("Narrow column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Wide column 2.");

 doc.save(getArtifactsDir() + "PageSetup.CustomColumnWidth.docx");
 
```

**Returns:**
double - Lo spazio tra questa colonna e la colonna successiva in punti.
### getWidth() {#getWidth}
```
public double getWidth()
```


Restituisce la larghezza della colonna di testo in punti.

 **Examples:** 

Mostra come creare colonne con spaziatura non uniforme.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 PageSetup pageSetup = builder.getPageSetup();

 TextColumnCollection columns = pageSetup.getTextColumns();
 columns.setEvenlySpaced(false);
 columns.setCount(2);

 // Determine the amount of room that we have available for arranging columns.
 double contentWidth = pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin();

 Assert.assertEquals(468.0d, contentWidth, 0.01d);

 // Set the first column to be narrow.
 TextColumn column = columns.get(0);
 column.setWidth(100.0);
 column.setSpaceAfter(20.0);

 // Set the second column to take the rest of the space available within the margins of the page.
 column = columns.get(1);
 column.setWidth(contentWidth - column.getWidth() - column.getSpaceAfter());

 builder.writeln("Narrow column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Wide column 2.");

 doc.save(getArtifactsDir() + "PageSetup.CustomColumnWidth.docx");
 
```

**Returns:**
double - La larghezza della colonna di testo in punti.
### setSpaceAfter(double value) {#setSpaceAfter-double}
```
public void setSpaceAfter(double value)
```


Imposta lo spazio tra questa colonna e la colonna successiva in punti. Non richiesto per l'ultima colonna.

 **Examples:** 

Mostra come creare colonne con spaziatura non uniforme.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 PageSetup pageSetup = builder.getPageSetup();

 TextColumnCollection columns = pageSetup.getTextColumns();
 columns.setEvenlySpaced(false);
 columns.setCount(2);

 // Determine the amount of room that we have available for arranging columns.
 double contentWidth = pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin();

 Assert.assertEquals(468.0d, contentWidth, 0.01d);

 // Set the first column to be narrow.
 TextColumn column = columns.get(0);
 column.setWidth(100.0);
 column.setSpaceAfter(20.0);

 // Set the second column to take the rest of the space available within the margins of the page.
 column = columns.get(1);
 column.setWidth(contentWidth - column.getWidth() - column.getSpaceAfter());

 builder.writeln("Narrow column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Wide column 2.");

 doc.save(getArtifactsDir() + "PageSetup.CustomColumnWidth.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Lo spazio tra questa colonna e la colonna successiva in punti. |

### setWidth(double value) {#setWidth-double}
```
public void setWidth(double value)
```


Imposta la larghezza della colonna di testo in punti.

 **Examples:** 

Mostra come creare colonne con spaziatura non uniforme.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 PageSetup pageSetup = builder.getPageSetup();

 TextColumnCollection columns = pageSetup.getTextColumns();
 columns.setEvenlySpaced(false);
 columns.setCount(2);

 // Determine the amount of room that we have available for arranging columns.
 double contentWidth = pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin();

 Assert.assertEquals(468.0d, contentWidth, 0.01d);

 // Set the first column to be narrow.
 TextColumn column = columns.get(0);
 column.setWidth(100.0);
 column.setSpaceAfter(20.0);

 // Set the second column to take the rest of the space available within the margins of the page.
 column = columns.get(1);
 column.setWidth(contentWidth - column.getWidth() - column.getSpaceAfter());

 builder.writeln("Narrow column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Wide column 2.");

 doc.save(getArtifactsDir() + "PageSetup.CustomColumnWidth.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | La larghezza della colonna di testo in punti. |

