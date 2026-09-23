---
title: "TextColumn"
linktitle: "TextColumn"
second_title: "Aspose.Words pour Java"
description: "Représente une seule colonne de texte en Java."
type: docs
weight: 670
url: /fr/java/com.aspose.words/textcolumn/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class TextColumn implements Cloneable
```

Représente une seule colonne de texte. [TextColumn](../../com.aspose.words/textcolumn/) est un membre de la collection [TextColumnCollection](../../com.aspose.words/textcolumncollection/). La collection [TextColumn](../../com.aspose.words/textcolumn/) comprend toutes les colonnes d’une section d’un document.

Pour en savoir plus, visitez l'article de documentation [ Working with Sections ][Working with Sections].

 **Remarks:** 

[TextColumn](../../com.aspose.words/textcolumn/) objects are only used to specify columns with custom width and spacing. If you want the columns in the document to be of equal width, set TextColumns. [TextColumnCollection.getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [TextColumnCollection.setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) to  true .

Lorsqu’une nouvelle [TextColumn](../../com.aspose.words/textcolumn/) est créée, sa largeur et son espacement sont réglés à zéro.

 **Examples:** 

Montre comment créer des colonnes espacées de manière inégale.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [getSpaceAfter()](#getSpaceAfter) | Obtient l’espace entre cette colonne et la colonne suivante en points. |
| [getWidth()](#getWidth) | Obtient la largeur de la colonne de texte en points. |
| [setSpaceAfter(double value)](#setSpaceAfter-double) | Définit l’espace entre cette colonne et la colonne suivante en points. |
| [setWidth(double value)](#setWidth-double) | Définit la largeur de la colonne de texte en points. |
### getSpaceAfter() {#getSpaceAfter}
```
public double getSpaceAfter()
```


Obtient l’espace entre cette colonne et la colonne suivante en points. Non requis pour la dernière colonne.

 **Examples:** 

Montre comment créer des colonnes espacées de manière inégale.

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
double - L'espace entre cette colonne et la colonne suivante en points.
### getWidth() {#getWidth}
```
public double getWidth()
```


Obtient la largeur de la colonne de texte en points.

 **Examples:** 

Montre comment créer des colonnes espacées de manière inégale.

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
double - La largeur de la colonne de texte en points.
### setSpaceAfter(double value) {#setSpaceAfter-double}
```
public void setSpaceAfter(double value)
```


Définit l'espace entre cette colonne et la colonne suivante en points. Non requis pour la dernière colonne.

 **Examples:** 

Montre comment créer des colonnes espacées de manière inégale.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | L'espace entre cette colonne et la colonne suivante en points. |

### setWidth(double value) {#setWidth-double}
```
public void setWidth(double value)
```


Définit la largeur de la colonne de texte en points.

 **Examples:** 

Montre comment créer des colonnes espacées de manière inégale.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La largeur de la colonne de texte en points. |

