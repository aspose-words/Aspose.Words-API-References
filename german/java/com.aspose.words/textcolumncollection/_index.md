---
title: "TextColumnCollection"
linktitle: "TextColumnCollection"
second_title: "Aspose.Words für Java"
description: "Eine Sammlung von TextColumn‑Objekten, die alle Textspalten in einem Abschnitt eines Dokuments in Java darstellen."
type: docs
weight: 671
url: /de/java/com.aspose.words/textcolumncollection/
---

**Inheritance:**
java.lang.Object
```
public class TextColumnCollection
```

Eine Sammlung von [TextColumn](../../com.aspose.words/textcolumn/) Objekten, die alle Textspalten in einem Abschnitt eines Dokuments darstellen.

Um mehr zu erfahren, besuchen Sie den [ Working with Sections ][Working with Sections] Dokumentationsartikel.

 **Remarks:** 

Use [setCount(int)](../../com.aspose.words/textcolumncollection/\#setCount-int), um die Anzahl der Textspalten festzulegen.

Um alle Spalten gleich breit und gleichmäßig verteilt zu machen, setzen Sie [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) auf true und geben Sie den Abstand zwischen den Spalten in [getSpacing()](../../com.aspose.words/textcolumncollection/\#getSpacing) / [setSpacing(double)](../../com.aspose.words/textcolumncollection/\#setSpacing-double) an. MS Word berechnet die Spaltenbreiten automatisch.

Wenn Sie [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) auf false gesetzt haben, müssen Sie Breite und Abstand für jede Spalte einzeln festlegen. Verwenden Sie den Indexer, um einzelne [TextColumn](../../com.aspose.words/textcolumn/)‑Objekte zuzugreifen.

Wenn Sie benutzerdefinierte Spaltenbreiten verwenden, stellen Sie sicher, dass die Summe aller Spaltenbreiten und Abstände zwischen ihnen der Seitenbreite minus den linken und rechten Seitenrändern entspricht.

 **Examples:** 

Zeigt, wie man in einem Abschnitt mehrere gleichmäßig verteilte Spalten erstellt.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get(int index)](#get-int) | Gibt eine Textspalte am angegebenen Index zurück. |
| [getCount()](#getCount) | Ermittelt die Anzahl der Spalten im Abschnitt eines Dokuments. |
| [getEvenlySpaced()](#getEvenlySpaced) | True, wenn Textspalten gleich breit und gleichmäßig verteilt sind. |
| [getLineBetween()](#getLineBetween) | Wenn true, wird eine vertikale Linie zwischen den Spalten hinzugefügt. |
| [getSpacing()](#getSpacing) | Wenn Spalten gleichmäßig verteilt sind, wird der Abstand zwischen den einzelnen Spalten in Punkten ermittelt oder festgelegt. |
| [getWidth()](#getWidth) | Wenn Spalten gleichmäßig verteilt sind, wird die Breite der Spalten ermittelt. |
| [setCount(int newCount)](#setCount-int) | Ordnet den Text in die angegebene Anzahl von Textspalten ein. |
| [setEvenlySpaced(boolean value)](#setEvenlySpaced-boolean) | True, wenn Textspalten gleich breit und gleichmäßig verteilt sind. |
| [setLineBetween(boolean value)](#setLineBetween-boolean) | Wenn true, wird eine vertikale Linie zwischen den Spalten hinzugefügt. |
| [setSpacing(double value)](#setSpacing-double) | Wenn Spalten gleichmäßig verteilt sind, wird der Abstand zwischen den einzelnen Spalten in Punkten ermittelt oder festgelegt. |
### get(int index) {#get-int}
```
public TextColumn get(int index)
```


Gibt eine Textspalte am angegebenen Index zurück.

 **Examples:** 

Zeigt, wie man ungleichmäßig verteilte Spalten erstellt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int |  |

**Returns:**
[TextColumn](../../com.aspose.words/textcolumn/) - A text column at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Ermittelt die Anzahl der Spalten im Abschnitt eines Dokuments.

 **Examples:** 

Zeigt, wie man in einem Abschnitt mehrere gleichmäßig verteilte Spalten erstellt.

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
int – Die Anzahl der Spalten im Abschnitt eines Dokuments.
### getEvenlySpaced() {#getEvenlySpaced}
```
public boolean getEvenlySpaced()
```


True, wenn Textspalten gleich breit und gleichmäßig verteilt sind.

 **Examples:** 

Zeigt, wie man ungleichmäßig verteilte Spalten erstellt.

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
boolean - Der entsprechende  boolean  Wert.
### getLineBetween() {#getLineBetween}
```
public boolean getLineBetween()
```


Wenn true, wird eine vertikale Linie zwischen den Spalten hinzugefügt.

 **Examples:** 

Zeigt, wie man Spalten mit einer vertikalen Linie trennt.

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
boolean - Der entsprechende  boolean  Wert.
### getSpacing() {#getSpacing}
```
public double getSpacing()
```


Wenn Spalten gleichmäßig verteilt sind, wird der Abstand zwischen den einzelnen Spalten in Punkten ermittelt oder festgelegt.

 **Remarks:** 

Wirkt nur, wenn [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) auf true gesetzt ist.

 **Examples:** 

Zeigt, wie man in einem Abschnitt mehrere gleichmäßig verteilte Spalten erstellt.

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
double - Der entsprechende  double  Wert.
### getWidth() {#getWidth}
```
public double getWidth()
```


Wenn Spalten gleichmäßig verteilt sind, wird die Breite der Spalten ermittelt.

 **Remarks:** 

Wirkt nur, wenn [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) auf true gesetzt ist.

 **Examples:** 

Zeigt, wie man in einem Abschnitt mehrere gleichmäßig verteilte Spalten erstellt.

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
double - Der entsprechende  double  Wert.
### setCount(int newCount) {#setCount-int}
```
public void setCount(int newCount)
```


Ordnet den Text in die angegebene Anzahl von Textspalten ein.

 **Remarks:** 

Wenn [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) false ist und Sie die Anzahl der Spalten erhöhen, werden neue [TextColumn](../../com.aspose.words/textcolumn/)‑Objekte mit null Breite und Abstand erstellt. Sie müssen Breite und Abstand für die neuen Spalten festlegen.

 **Examples:** 

Zeigt, wie man in einem Abschnitt mehrere gleichmäßig verteilte Spalten erstellt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| newCount | int | Die Anzahl der Spalten, in die der Text angeordnet werden soll. |

### setEvenlySpaced(boolean value) {#setEvenlySpaced-boolean}
```
public void setEvenlySpaced(boolean value)
```


True, wenn Textspalten gleich breit und gleichmäßig verteilt sind.

 **Examples:** 

Zeigt, wie man ungleichmäßig verteilte Spalten erstellt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setLineBetween(boolean value) {#setLineBetween-boolean}
```
public void setLineBetween(boolean value)
```


Wenn true, wird eine vertikale Linie zwischen den Spalten hinzugefügt.

 **Examples:** 

Zeigt, wie man Spalten mit einer vertikalen Linie trennt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setSpacing(double value) {#setSpacing-double}
```
public void setSpacing(double value)
```


Wenn Spalten gleichmäßig verteilt sind, wird der Abstand zwischen den einzelnen Spalten in Punkten ermittelt oder festgelegt.

 **Remarks:** 

Wirkt nur, wenn [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) auf true gesetzt ist.

 **Examples:** 

Zeigt, wie man in einem Abschnitt mehrere gleichmäßig verteilte Spalten erstellt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der entsprechende  double  Wert. |

