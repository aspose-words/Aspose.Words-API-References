---
title: "TextColumnCollection"
linktitle: "TextColumnCollection"
second_title: "Aspose.Words pour Java"
description: "Une collection d'objets TextColumn qui représentent toutes les colonnes de texte dans une section d'un document en Java."
type: docs
weight: 671
url: /fr/java/com.aspose.words/textcolumncollection/
---

**Inheritance:**
java.lang.Object
```
public class TextColumnCollection
```

Une collection d'objets [TextColumn](../../com.aspose.words/textcolumn/) qui représentent toutes les colonnes de texte dans une section d'un document.

Pour en savoir plus, visitez l'article de documentation [ Working with Sections ][Working with Sections].

 **Remarks:** 

Utilisez [setCount(int)](../../com.aspose.words/textcolumncollection/\#setCount-int) pour définir le nombre de colonnes de texte.

Pour que toutes les colonnes aient la même largeur et soient espacées uniformément, définissez [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) sur  true  et spécifiez la quantité d'espace entre les colonnes dans [getSpacing()](../../com.aspose.words/textcolumncollection/\#getSpacing) / [setSpacing(double)](../../com.aspose.words/textcolumncollection/\#setSpacing-double). MS Word calculera automatiquement les largeurs des colonnes.

Si vous avez [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) réglés sur  false , vous devez spécifier la largeur et l'espacement pour chaque colonne individuellement. Utilisez l'indexeur pour accéder aux objets [TextColumn](../../com.aspose.words/textcolumn/) individuels.

Lorsque vous utilisez des largeurs de colonne personnalisées, assurez‑vous que la somme de toutes les largeurs de colonne et des espacements entre elles soit égale à la largeur de la page moins les marges gauche et droite.

 **Examples:** 

Montre comment créer plusieurs colonnes espacées uniformément dans une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```


[Working with Sections]: https://docs.aspose.com/words/java/working-with-sections/
## Méthodes

| Méthode | Description |
| --- | --- |
| [get(int index)](#get-int) | Renvoie une colonne de texte à l'index spécifié. |
| [getCount()](#getCount) | Obtient le nombre de colonnes dans la section d'un document. |
| [getEvenlySpaced()](#getEvenlySpaced) | Vrai si les colonnes de texte ont une largeur égale et sont espacées uniformément. |
| [getLineBetween()](#getLineBetween) | Lorsque  true , ajoute une ligne verticale entre les colonnes. |
| [getSpacing()](#getSpacing) | Lorsque les colonnes sont espacées uniformément, obtient ou définit la quantité d'espace entre chaque colonne en points. |
| [getWidth()](#getWidth) | Lorsque les colonnes sont espacées uniformément, obtient la largeur des colonnes. |
| [setCount(int newCount)](#setCount-int) | Dispose le texte dans le nombre spécifié de colonnes de texte. |
| [setEvenlySpaced(boolean value)](#setEvenlySpaced-boolean) | Vrai si les colonnes de texte ont une largeur égale et sont espacées uniformément. |
| [setLineBetween(boolean value)](#setLineBetween-boolean) | Lorsque  true , ajoute une ligne verticale entre les colonnes. |
| [setSpacing(double value)](#setSpacing-double) | Lorsque les colonnes sont espacées uniformément, obtient ou définit la quantité d'espace entre chaque colonne en points. |
### get(int index) {#get-int}
```
public TextColumn get(int index)
```


Renvoie une colonne de texte à l'index spécifié.

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
| index | int |  |

**Returns:**
[TextColumn](../../com.aspose.words/textcolumn/) - A text column at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Obtient le nombre de colonnes dans la section d'un document.

 **Examples:** 

Montre comment créer plusieurs colonnes espacées uniformément dans une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Returns:**
int - Le nombre de colonnes dans la section d'un document.
### getEvenlySpaced() {#getEvenlySpaced}
```
public boolean getEvenlySpaced()
```


Vrai si les colonnes de texte ont une largeur égale et sont espacées uniformément.

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
boolean - La valeur  boolean  correspondante.
### getLineBetween() {#getLineBetween}
```
public boolean getLineBetween()
```


Lorsque  true , ajoute une ligne verticale entre les colonnes.

 **Examples:** 

Montre comment séparer les colonnes avec une ligne verticale.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Configure the current section's PageSetup object to divide the text into several columns.
 // Set the "LineBetween" property to "true" to put a dividing line between columns.
 // Set the "LineBetween" property to "false" to leave the space between columns blank.
 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setLineBetween(lineBetween);
 columns.setCount(3);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 3.");

 doc.save(getArtifactsDir() + "PageSetup.VerticalLineBetweenColumns.docx");
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getSpacing() {#getSpacing}
```
public double getSpacing()
```


Lorsque les colonnes sont espacées uniformément, obtient ou définit la quantité d'espace entre chaque colonne en points.

 **Remarks:** 

N'a d'effet que lorsque [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) est réglé sur  true .

 **Examples:** 

Montre comment créer plusieurs colonnes espacées uniformément dans une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Returns:**
double - La valeur  double  correspondante.
### getWidth() {#getWidth}
```
public double getWidth()
```


Lorsque les colonnes sont espacées uniformément, obtient la largeur des colonnes.

 **Remarks:** 

N'a d'effet que lorsque [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) est réglé sur  true .

 **Examples:** 

Montre comment créer plusieurs colonnes espacées uniformément dans une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Returns:**
double - La valeur  double  correspondante.
### setCount(int newCount) {#setCount-int}
```
public void setCount(int newCount)
```


Dispose le texte dans le nombre spécifié de colonnes de texte.

 **Remarks:** 

Lorsque [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) est  false  et que vous augmentez le nombre de colonnes, de nouveaux objets [TextColumn](../../com.aspose.words/textcolumn/) sont créés avec une largeur et un espacement nuls. Vous devez définir la largeur et l'espacement pour les nouvelles colonnes.

 **Examples:** 

Montre comment créer plusieurs colonnes espacées uniformément dans une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| newCount | int | Le nombre de colonnes dans lesquelles le texte doit être disposé. |

### setEvenlySpaced(boolean value) {#setEvenlySpaced-boolean}
```
public void setEvenlySpaced(boolean value)
```


Vrai si les colonnes de texte ont une largeur égale et sont espacées uniformément.

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
| valeur | boolean | La valeur  boolean  correspondante. |

### setLineBetween(boolean value) {#setLineBetween-boolean}
```
public void setLineBetween(boolean value)
```


Lorsque  true , ajoute une ligne verticale entre les colonnes.

 **Examples:** 

Montre comment séparer les colonnes avec une ligne verticale.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Configure the current section's PageSetup object to divide the text into several columns.
 // Set the "LineBetween" property to "true" to put a dividing line between columns.
 // Set the "LineBetween" property to "false" to leave the space between columns blank.
 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setLineBetween(lineBetween);
 columns.setCount(3);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 3.");

 doc.save(getArtifactsDir() + "PageSetup.VerticalLineBetweenColumns.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setSpacing(double value) {#setSpacing-double}
```
public void setSpacing(double value)
```


Lorsque les colonnes sont espacées uniformément, obtient ou définit la quantité d'espace entre chaque colonne en points.

 **Remarks:** 

N'a d'effet que lorsque [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) est réglé sur  true .

 **Examples:** 

Montre comment créer plusieurs colonnes espacées uniformément dans une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La valeur  double  correspondante. |

