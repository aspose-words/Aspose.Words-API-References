---
title: "TextColumnCollection"
linktitle: "TextColumnCollection"
second_title: "Aspose.Words per Java"
description: "Una collezione di oggetti TextColumn che rappresentano tutte le colonne di testo in una sezione di un documento in Java."
type: docs
weight: 671
url: /it/java/com.aspose.words/textcolumncollection/
---

**Inheritance:**
java.lang.Object
```
public class TextColumnCollection
```

Una collezione di oggetti [TextColumn](../../com.aspose.words/textcolumn/) che rappresentano tutte le colonne di testo in una sezione di un documento.

Per saperne di più, visita l'articolo della documentazione [ Working with Sections ][Working with Sections].

 **Remarks:** 

Usa [setCount(int)](../../com.aspose.words/textcolumncollection/\#setCount-int) per impostare il numero di colonne di testo.

Per rendere tutte le colonne della stessa larghezza e spaziarle uniformemente, imposta [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) su  true  e specifica la quantità di spazio tra le colonne in [getSpacing()](../../com.aspose.words/textcolumncollection/\#getSpacing) / [setSpacing(double)](../../com.aspose.words/textcolumncollection/\#setSpacing-double). MS Word calcolerà automaticamente le larghezze delle colonne.

Se hai [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) impostato su  false , devi specificare larghezza e spaziatura per ogni colonna individualmente. Usa l'indicizzatore per accedere ai singoli oggetti [TextColumn](../../com.aspose.words/textcolumn/).

Quando si usano larghezze di colonna personalizzate, assicurati che la somma di tutte le larghezze delle colonne e degli spazi tra di esse sia uguale alla larghezza della pagina meno i margini sinistro e destro.

 **Examples:** 

Mostra come creare più colonne equamente distanziate in una sezione.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get(int index)](#get-int) | Restituisce una colonna di testo all'indice specificato. |
| [getCount()](#getCount) | Restituisce il numero di colonne nella sezione di un documento. |
| [getEvenlySpaced()](#getEvenlySpaced) | True se le colonne di testo hanno larghezza uguale e sono equamente distanziate. |
| [getLineBetween()](#getLineBetween) | Quando  true , aggiunge una linea verticale tra le colonne. |
| [getSpacing()](#getSpacing) | Quando le colonne sono equamente distanziate, ottiene o imposta la quantità di spazio tra ciascuna colonna in punti. |
| [getWidth()](#getWidth) | Quando le colonne sono equamente distanziate, ottiene la larghezza delle colonne. |
| [setCount(int newCount)](#setCount-int) | Dispone il testo nel numero specificato di colonne di testo. |
| [setEvenlySpaced(boolean value)](#setEvenlySpaced-boolean) | True se le colonne di testo hanno larghezza uguale e sono equamente distanziate. |
| [setLineBetween(boolean value)](#setLineBetween-boolean) | Quando  true , aggiunge una linea verticale tra le colonne. |
| [setSpacing(double value)](#setSpacing-double) | Quando le colonne sono equamente distanziate, ottiene o imposta la quantità di spazio tra ciascuna colonna in punti. |
### get(int index) {#get-int}
```
public TextColumn get(int index)
```


Restituisce una colonna di testo all'indice specificato.

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
| indice | int |  |

**Returns:**
[TextColumn](../../com.aspose.words/textcolumn/) - A text column at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Restituisce il numero di colonne nella sezione di un documento.

 **Examples:** 

Mostra come creare più colonne equamente distanziate in una sezione.

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
int - Il numero di colonne nella sezione di un documento.
### getEvenlySpaced() {#getEvenlySpaced}
```
public boolean getEvenlySpaced()
```


True se le colonne di testo hanno larghezza uguale e sono equamente distanziate.

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
boolean - Il valore booleano corrispondente.
### getLineBetween() {#getLineBetween}
```
public boolean getLineBetween()
```


Quando  true , aggiunge una linea verticale tra le colonne.

 **Examples:** 

Mostra come separare le colonne con una linea verticale.

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
boolean - Il valore booleano corrispondente.
### getSpacing() {#getSpacing}
```
public double getSpacing()
```


Quando le colonne sono equamente distanziate, ottiene o imposta la quantità di spazio tra ciascuna colonna in punti.

 **Remarks:** 

Ha effetto solo quando [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) è impostato su  true .

 **Examples:** 

Mostra come creare più colonne equamente distanziate in una sezione.

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
double - Il valore double corrispondente.
### getWidth() {#getWidth}
```
public double getWidth()
```


Quando le colonne sono equamente distanziate, ottiene la larghezza delle colonne.

 **Remarks:** 

Ha effetto solo quando [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) è impostato su  true .

 **Examples:** 

Mostra come creare più colonne equamente distanziate in una sezione.

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
double - Il valore double corrispondente.
### setCount(int newCount) {#setCount-int}
```
public void setCount(int newCount)
```


Dispone il testo nel numero specificato di colonne di testo.

 **Remarks:** 

Quando [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) è  false  e aumenti il numero di colonne, vengono creati nuovi oggetti [TextColumn](../../com.aspose.words/textcolumn/) con larghezza e spaziatura zero. È necessario impostare larghezza e spaziatura per le nuove colonne.

 **Examples:** 

Mostra come creare più colonne equamente distanziate in una sezione.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| newCount | int | Il numero di colonne in cui il testo deve essere disposto. |

### setEvenlySpaced(boolean value) {#setEvenlySpaced-boolean}
```
public void setEvenlySpaced(boolean value)
```


True se le colonne di testo hanno larghezza uguale e sono equamente distanziate.

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
| valore | boolean | Il valore booleano corrispondente. |

### setLineBetween(boolean value) {#setLineBetween-boolean}
```
public void setLineBetween(boolean value)
```


Quando  true , aggiunge una linea verticale tra le colonne.

 **Examples:** 

Mostra come separare le colonne con una linea verticale.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setSpacing(double value) {#setSpacing-double}
```
public void setSpacing(double value)
```


Quando le colonne sono equamente distanziate, ottiene o imposta la quantità di spazio tra ciascuna colonna in punti.

 **Remarks:** 

Ha effetto solo quando [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) è impostato su  true .

 **Examples:** 

Mostra come creare più colonne equamente distanziate in una sezione.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Il valore double corrispondente. |

