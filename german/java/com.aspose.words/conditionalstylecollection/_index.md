---
title: "ConditionalStyleCollection"
linktitle: "ConditionalStyleCollection"
second_title: "Aspose.Words für Java"
description: "Stellt eine Sammlung von ConditionalStyle-Objekten in Java dar."
type: docs
weight: 124
url: /de/java/com.aspose.words/conditionalstylecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ConditionalStyleCollection implements Iterable
```

Stellt eine Sammlung von [ConditionalStyle](../../com.aspose.words/conditionalstyle/) Objekten dar.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Working with Tables ][Working with Tables].

 **Remarks:** 

Es ist nicht möglich, Elemente zu dieser Sammlung hinzuzufügen oder zu entfernen. Sie enthält einen permanenten Satz von Elementen: ein Element für jeden Wert des Aufzählungstyps [ConditionalStyleType](../../com.aspose.words/conditionalstyletype/).

 **Examples:** 

Zeigt, wie man mit bestimmten Bereichsstilen einer Tabelle arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endRow();
 builder.insertCell();
 builder.write("Cell 3");
 builder.insertCell();
 builder.write("Cell 4");
 builder.endTable();

 // Create a custom table style.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");

 // Conditional styles are formatting changes that affect only some of the table's cells
 // based on a predicate, such as the cells being in the last row.
 // Below are three ways of accessing a table style's conditional styles from the "ConditionalStyles" collection.
 // 1 -  By style type:
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.FIRST_ROW).getShading().setBackgroundPatternColor(Color.BLUE);

 // 2 -  By index:
 tableStyle.getConditionalStyles().get(0).getBorders().setColor(Color.BLACK);
 tableStyle.getConditionalStyles().get(0).getBorders().setLineStyle(LineStyle.DOT_DASH);
 Assert.assertEquals(ConditionalStyleType.FIRST_ROW, tableStyle.getConditionalStyles().get(0).getType());

 // 3 -  As a property:
 tableStyle.getConditionalStyles().getFirstRow().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 // Apply padding and text formatting to conditional styles.
 tableStyle.getConditionalStyles().getLastRow().setBottomPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setLeftPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setRightPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setTopPadding(10.0);
 tableStyle.getConditionalStyles().getLastColumn().getFont().setBold(true);

 // List all possible style conditions.
 Iterator enumerator = tableStyle.getConditionalStyles().iterator();
 while (enumerator.hasNext()) {
     ConditionalStyle currentStyle = enumerator.next();
     if (currentStyle != null) System.out.println(currentStyle.getType());
 }

 // Apply the custom style, which contains all conditional styles, to the table.
 table.setStyle(tableStyle);

 // Our style applies some conditional styles by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // We will need to enable all other styles ourselves via the "StyleOptions" property.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.LAST_ROW | TableStyleOptions.LAST_COLUMN);

 doc.save(getArtifactsDir() + "Table.ConditionalStyles.docx");
 
```


[Working with Tables]: https://docs.aspose.com/words/java/working-with-tables/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Löscht alle bedingten Formatierungen des Tabellenstils. |
| [get(int index)](#get-int) | Ruft ein [ConditionalStyle](../../com.aspose.words/conditionalstyle/) Objekt anhand des Index ab. |
| [getBottomLeftCell()](#getBottomLeftCell) | Liefert den Stil der unteren linken Zelle. |
| [getBottomRightCell()](#getBottomRightCell) | Liefert den Stil der unteren rechten Zelle. |
| [getByConditionalStyleType(int conditionalStyleType)](#getByConditionalStyleType-int) |  |
| [getCount()](#getCount) | Liefert die Anzahl der bedingten Stile in der Sammlung. |
| [getEvenColumnBanding()](#getEvenColumnBanding) | Liefert den Stil für gerade Spaltenbänder. |
| [getEvenRowBanding()](#getEvenRowBanding) | Liefert den Stil für gerade Zeilenbänder. |
| [getFirstColumn()](#getFirstColumn) | Liefert den Stil der ersten Spalte. |
| [getFirstRow()](#getFirstRow) | Liefert den Stil der ersten Zeile. |
| [getLastColumn()](#getLastColumn) | Liefert den Stil der letzten Spalte. |
| [getLastRow()](#getLastRow) | Liefert den Stil der letzten Zeile. |
| [getOddColumnBanding()](#getOddColumnBanding) | Liefert den Stil für ungerade Spaltenbänder. |
| [getOddRowBanding()](#getOddRowBanding) | Liefert den Stil für ungerade Zeilenbänder. |
| [getTopLeftCell()](#getTopLeftCell) | Liefert den Stil der oberen linken Zelle. |
| [getTopRightCell()](#getTopRightCell) | Liefert den Stil der oberen rechten Zelle. |
| [iterator()](#iterator) | Gibt ein Enumerator-Objekt zurück, das verwendet werden kann, um über alle bedingten Stile in der Sammlung zu iterieren. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Löscht alle bedingten Formatierungen des Tabellenstils.

 **Examples:** 

Zeigt, wie bedingte Tabellenstile zurückgesetzt werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("First row");
 builder.endRow();
 builder.insertCell();
 builder.write("Last row");
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 table.setStyle(tableStyle);

 // Set the table style to color the borders of the first row of the table in red.
 tableStyle.getConditionalStyles().getFirstRow().getBorders().setColor(Color.RED);

 // Set the table style to color the borders of the last row of the table in blue.
 tableStyle.getConditionalStyles().getLastRow().getBorders().setColor(Color.BLUE);

 // Below are two ways of using the "ClearFormatting" method to clear the conditional styles.
 // 1 -  Clear the conditional styles for a specific part of a table:
 tableStyle.getConditionalStyles().get(0).clearFormatting();

 Assert.assertEquals(0, tableStyle.getConditionalStyles().getFirstRow().getBorders().getColor().getRGB());

 // 2 -  Clear the conditional styles for the entire table:
 tableStyle.getConditionalStyles().clearFormatting();

 Assert.assertEquals(tableStyle.getConditionalStyles().getLastRow().getBorders().getColor().getRGB(), 0);
 
```

### get(int index) {#get-int}
```
public ConditionalStyle get(int index)
```


Ruft ein [ConditionalStyle](../../com.aspose.words/conditionalstyle/) Objekt anhand des Index ab.

 **Examples:** 

Zeigt, wie man mit bestimmten Bereichsstilen einer Tabelle arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endRow();
 builder.insertCell();
 builder.write("Cell 3");
 builder.insertCell();
 builder.write("Cell 4");
 builder.endTable();

 // Create a custom table style.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");

 // Conditional styles are formatting changes that affect only some of the table's cells
 // based on a predicate, such as the cells being in the last row.
 // Below are three ways of accessing a table style's conditional styles from the "ConditionalStyles" collection.
 // 1 -  By style type:
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.FIRST_ROW).getShading().setBackgroundPatternColor(Color.BLUE);

 // 2 -  By index:
 tableStyle.getConditionalStyles().get(0).getBorders().setColor(Color.BLACK);
 tableStyle.getConditionalStyles().get(0).getBorders().setLineStyle(LineStyle.DOT_DASH);
 Assert.assertEquals(ConditionalStyleType.FIRST_ROW, tableStyle.getConditionalStyles().get(0).getType());

 // 3 -  As a property:
 tableStyle.getConditionalStyles().getFirstRow().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 // Apply padding and text formatting to conditional styles.
 tableStyle.getConditionalStyles().getLastRow().setBottomPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setLeftPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setRightPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setTopPadding(10.0);
 tableStyle.getConditionalStyles().getLastColumn().getFont().setBold(true);

 // List all possible style conditions.
 Iterator enumerator = tableStyle.getConditionalStyles().iterator();
 while (enumerator.hasNext()) {
     ConditionalStyle currentStyle = enumerator.next();
     if (currentStyle != null) System.out.println(currentStyle.getType());
 }

 // Apply the custom style, which contains all conditional styles, to the table.
 table.setStyle(tableStyle);

 // Our style applies some conditional styles by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // We will need to enable all other styles ourselves via the "StyleOptions" property.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.LAST_ROW | TableStyleOptions.LAST_COLUMN);

 doc.save(getArtifactsDir() + "Table.ConditionalStyles.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Nullbasierter Index des abzurufenden bedingten Stils. |

**Returns:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle/) - The corresponding [ConditionalStyle](../../com.aspose.words/conditionalstyle/) value.
### getBottomLeftCell() {#getBottomLeftCell}
```
public ConditionalStyle getBottomLeftCell()
```


Liefert den Stil der unteren linken Zelle.

 **Examples:** 

Zeigt, wie man mit bestimmten Bereichsstilen einer Tabelle arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endRow();
 builder.insertCell();
 builder.write("Cell 3");
 builder.insertCell();
 builder.write("Cell 4");
 builder.endTable();

 // Create a custom table style.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");

 // Conditional styles are formatting changes that affect only some of the table's cells
 // based on a predicate, such as the cells being in the last row.
 // Below are three ways of accessing a table style's conditional styles from the "ConditionalStyles" collection.
 // 1 -  By style type:
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.FIRST_ROW).getShading().setBackgroundPatternColor(Color.BLUE);

 // 2 -  By index:
 tableStyle.getConditionalStyles().get(0).getBorders().setColor(Color.BLACK);
 tableStyle.getConditionalStyles().get(0).getBorders().setLineStyle(LineStyle.DOT_DASH);
 Assert.assertEquals(ConditionalStyleType.FIRST_ROW, tableStyle.getConditionalStyles().get(0).getType());

 // 3 -  As a property:
 tableStyle.getConditionalStyles().getFirstRow().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 // Apply padding and text formatting to conditional styles.
 tableStyle.getConditionalStyles().getLastRow().setBottomPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setLeftPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setRightPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setTopPadding(10.0);
 tableStyle.getConditionalStyles().getLastColumn().getFont().setBold(true);

 // List all possible style conditions.
 Iterator enumerator = tableStyle.getConditionalStyles().iterator();
 while (enumerator.hasNext()) {
     ConditionalStyle currentStyle = enumerator.next();
     if (currentStyle != null) System.out.println(currentStyle.getType());
 }

 // Apply the custom style, which contains all conditional styles, to the table.
 table.setStyle(tableStyle);

 // Our style applies some conditional styles by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // We will need to enable all other styles ourselves via the "StyleOptions" property.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.LAST_ROW | TableStyleOptions.LAST_COLUMN);

 doc.save(getArtifactsDir() + "Table.ConditionalStyles.docx");
 
```

**Returns:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle/) - The bottom left cell style.
### getBottomRightCell() {#getBottomRightCell}
```
public ConditionalStyle getBottomRightCell()
```


Liefert den Stil der unteren rechten Zelle.

 **Examples:** 

Zeigt, wie man mit bestimmten Bereichsstilen einer Tabelle arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endRow();
 builder.insertCell();
 builder.write("Cell 3");
 builder.insertCell();
 builder.write("Cell 4");
 builder.endTable();

 // Create a custom table style.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");

 // Conditional styles are formatting changes that affect only some of the table's cells
 // based on a predicate, such as the cells being in the last row.
 // Below are three ways of accessing a table style's conditional styles from the "ConditionalStyles" collection.
 // 1 -  By style type:
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.FIRST_ROW).getShading().setBackgroundPatternColor(Color.BLUE);

 // 2 -  By index:
 tableStyle.getConditionalStyles().get(0).getBorders().setColor(Color.BLACK);
 tableStyle.getConditionalStyles().get(0).getBorders().setLineStyle(LineStyle.DOT_DASH);
 Assert.assertEquals(ConditionalStyleType.FIRST_ROW, tableStyle.getConditionalStyles().get(0).getType());

 // 3 -  As a property:
 tableStyle.getConditionalStyles().getFirstRow().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 // Apply padding and text formatting to conditional styles.
 tableStyle.getConditionalStyles().getLastRow().setBottomPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setLeftPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setRightPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setTopPadding(10.0);
 tableStyle.getConditionalStyles().getLastColumn().getFont().setBold(true);

 // List all possible style conditions.
 Iterator enumerator = tableStyle.getConditionalStyles().iterator();
 while (enumerator.hasNext()) {
     ConditionalStyle currentStyle = enumerator.next();
     if (currentStyle != null) System.out.println(currentStyle.getType());
 }

 // Apply the custom style, which contains all conditional styles, to the table.
 table.setStyle(tableStyle);

 // Our style applies some conditional styles by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // We will need to enable all other styles ourselves via the "StyleOptions" property.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.LAST_ROW | TableStyleOptions.LAST_COLUMN);

 doc.save(getArtifactsDir() + "Table.ConditionalStyles.docx");
 
```

**Returns:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle/) - The bottom right cell style.
### getByConditionalStyleType(int conditionalStyleType) {#getByConditionalStyleType-int}
```
public ConditionalStyle getByConditionalStyleType(int conditionalStyleType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| conditionalStyleType | int |  |

**Returns:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle/)
### getCount() {#getCount}
```
public int getCount()
```


Liefert die Anzahl der bedingten Stile in der Sammlung.

 **Examples:** 

Zeigt, wie man mit bestimmten Bereichsstilen einer Tabelle arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endRow();
 builder.insertCell();
 builder.write("Cell 3");
 builder.insertCell();
 builder.write("Cell 4");
 builder.endTable();

 // Create a custom table style.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");

 // Conditional styles are formatting changes that affect only some of the table's cells
 // based on a predicate, such as the cells being in the last row.
 // Below are three ways of accessing a table style's conditional styles from the "ConditionalStyles" collection.
 // 1 -  By style type:
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.FIRST_ROW).getShading().setBackgroundPatternColor(Color.BLUE);

 // 2 -  By index:
 tableStyle.getConditionalStyles().get(0).getBorders().setColor(Color.BLACK);
 tableStyle.getConditionalStyles().get(0).getBorders().setLineStyle(LineStyle.DOT_DASH);
 Assert.assertEquals(ConditionalStyleType.FIRST_ROW, tableStyle.getConditionalStyles().get(0).getType());

 // 3 -  As a property:
 tableStyle.getConditionalStyles().getFirstRow().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 // Apply padding and text formatting to conditional styles.
 tableStyle.getConditionalStyles().getLastRow().setBottomPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setLeftPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setRightPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setTopPadding(10.0);
 tableStyle.getConditionalStyles().getLastColumn().getFont().setBold(true);

 // List all possible style conditions.
 Iterator enumerator = tableStyle.getConditionalStyles().iterator();
 while (enumerator.hasNext()) {
     ConditionalStyle currentStyle = enumerator.next();
     if (currentStyle != null) System.out.println(currentStyle.getType());
 }

 // Apply the custom style, which contains all conditional styles, to the table.
 table.setStyle(tableStyle);

 // Our style applies some conditional styles by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // We will need to enable all other styles ourselves via the "StyleOptions" property.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.LAST_ROW | TableStyleOptions.LAST_COLUMN);

 doc.save(getArtifactsDir() + "Table.ConditionalStyles.docx");
 
```

**Returns:**
int - Die Anzahl der bedingten Stile in der Sammlung.
### getEvenColumnBanding() {#getEvenColumnBanding}
```
public ConditionalStyle getEvenColumnBanding()
```


Liefert den Stil für gerade Spaltenbänder.

 **Examples:** 

Zeigt, wie man mit bestimmten Bereichsstilen einer Tabelle arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endRow();
 builder.insertCell();
 builder.write("Cell 3");
 builder.insertCell();
 builder.write("Cell 4");
 builder.endTable();

 // Create a custom table style.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");

 // Conditional styles are formatting changes that affect only some of the table's cells
 // based on a predicate, such as the cells being in the last row.
 // Below are three ways of accessing a table style's conditional styles from the "ConditionalStyles" collection.
 // 1 -  By style type:
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.FIRST_ROW).getShading().setBackgroundPatternColor(Color.BLUE);

 // 2 -  By index:
 tableStyle.getConditionalStyles().get(0).getBorders().setColor(Color.BLACK);
 tableStyle.getConditionalStyles().get(0).getBorders().setLineStyle(LineStyle.DOT_DASH);
 Assert.assertEquals(ConditionalStyleType.FIRST_ROW, tableStyle.getConditionalStyles().get(0).getType());

 // 3 -  As a property:
 tableStyle.getConditionalStyles().getFirstRow().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 // Apply padding and text formatting to conditional styles.
 tableStyle.getConditionalStyles().getLastRow().setBottomPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setLeftPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setRightPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setTopPadding(10.0);
 tableStyle.getConditionalStyles().getLastColumn().getFont().setBold(true);

 // List all possible style conditions.
 Iterator enumerator = tableStyle.getConditionalStyles().iterator();
 while (enumerator.hasNext()) {
     ConditionalStyle currentStyle = enumerator.next();
     if (currentStyle != null) System.out.println(currentStyle.getType());
 }

 // Apply the custom style, which contains all conditional styles, to the table.
 table.setStyle(tableStyle);

 // Our style applies some conditional styles by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // We will need to enable all other styles ourselves via the "StyleOptions" property.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.LAST_ROW | TableStyleOptions.LAST_COLUMN);

 doc.save(getArtifactsDir() + "Table.ConditionalStyles.docx");
 
```

**Returns:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle/) - The even column banding style.
### getEvenRowBanding() {#getEvenRowBanding}
```
public ConditionalStyle getEvenRowBanding()
```


Liefert den Stil für gerade Zeilenbänder.

 **Examples:** 

Zeigt, wie man mit bestimmten Bereichsstilen einer Tabelle arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endRow();
 builder.insertCell();
 builder.write("Cell 3");
 builder.insertCell();
 builder.write("Cell 4");
 builder.endTable();

 // Create a custom table style.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");

 // Conditional styles are formatting changes that affect only some of the table's cells
 // based on a predicate, such as the cells being in the last row.
 // Below are three ways of accessing a table style's conditional styles from the "ConditionalStyles" collection.
 // 1 -  By style type:
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.FIRST_ROW).getShading().setBackgroundPatternColor(Color.BLUE);

 // 2 -  By index:
 tableStyle.getConditionalStyles().get(0).getBorders().setColor(Color.BLACK);
 tableStyle.getConditionalStyles().get(0).getBorders().setLineStyle(LineStyle.DOT_DASH);
 Assert.assertEquals(ConditionalStyleType.FIRST_ROW, tableStyle.getConditionalStyles().get(0).getType());

 // 3 -  As a property:
 tableStyle.getConditionalStyles().getFirstRow().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 // Apply padding and text formatting to conditional styles.
 tableStyle.getConditionalStyles().getLastRow().setBottomPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setLeftPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setRightPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setTopPadding(10.0);
 tableStyle.getConditionalStyles().getLastColumn().getFont().setBold(true);

 // List all possible style conditions.
 Iterator enumerator = tableStyle.getConditionalStyles().iterator();
 while (enumerator.hasNext()) {
     ConditionalStyle currentStyle = enumerator.next();
     if (currentStyle != null) System.out.println(currentStyle.getType());
 }

 // Apply the custom style, which contains all conditional styles, to the table.
 table.setStyle(tableStyle);

 // Our style applies some conditional styles by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // We will need to enable all other styles ourselves via the "StyleOptions" property.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.LAST_ROW | TableStyleOptions.LAST_COLUMN);

 doc.save(getArtifactsDir() + "Table.ConditionalStyles.docx");
 
```

**Returns:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle/) - The even row banding style.
### getFirstColumn() {#getFirstColumn}
```
public ConditionalStyle getFirstColumn()
```


Liefert den Stil der ersten Spalte.

 **Examples:** 

Zeigt, wie man mit bestimmten Bereichsstilen einer Tabelle arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endRow();
 builder.insertCell();
 builder.write("Cell 3");
 builder.insertCell();
 builder.write("Cell 4");
 builder.endTable();

 // Create a custom table style.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");

 // Conditional styles are formatting changes that affect only some of the table's cells
 // based on a predicate, such as the cells being in the last row.
 // Below are three ways of accessing a table style's conditional styles from the "ConditionalStyles" collection.
 // 1 -  By style type:
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.FIRST_ROW).getShading().setBackgroundPatternColor(Color.BLUE);

 // 2 -  By index:
 tableStyle.getConditionalStyles().get(0).getBorders().setColor(Color.BLACK);
 tableStyle.getConditionalStyles().get(0).getBorders().setLineStyle(LineStyle.DOT_DASH);
 Assert.assertEquals(ConditionalStyleType.FIRST_ROW, tableStyle.getConditionalStyles().get(0).getType());

 // 3 -  As a property:
 tableStyle.getConditionalStyles().getFirstRow().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 // Apply padding and text formatting to conditional styles.
 tableStyle.getConditionalStyles().getLastRow().setBottomPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setLeftPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setRightPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setTopPadding(10.0);
 tableStyle.getConditionalStyles().getLastColumn().getFont().setBold(true);

 // List all possible style conditions.
 Iterator enumerator = tableStyle.getConditionalStyles().iterator();
 while (enumerator.hasNext()) {
     ConditionalStyle currentStyle = enumerator.next();
     if (currentStyle != null) System.out.println(currentStyle.getType());
 }

 // Apply the custom style, which contains all conditional styles, to the table.
 table.setStyle(tableStyle);

 // Our style applies some conditional styles by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // We will need to enable all other styles ourselves via the "StyleOptions" property.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.LAST_ROW | TableStyleOptions.LAST_COLUMN);

 doc.save(getArtifactsDir() + "Table.ConditionalStyles.docx");
 
```

**Returns:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle/) - The first column style.
### getFirstRow() {#getFirstRow}
```
public ConditionalStyle getFirstRow()
```


Liefert den Stil der ersten Zeile.

 **Examples:** 

Zeigt, wie man mit bestimmten Bereichsstilen einer Tabelle arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endRow();
 builder.insertCell();
 builder.write("Cell 3");
 builder.insertCell();
 builder.write("Cell 4");
 builder.endTable();

 // Create a custom table style.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");

 // Conditional styles are formatting changes that affect only some of the table's cells
 // based on a predicate, such as the cells being in the last row.
 // Below are three ways of accessing a table style's conditional styles from the "ConditionalStyles" collection.
 // 1 -  By style type:
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.FIRST_ROW).getShading().setBackgroundPatternColor(Color.BLUE);

 // 2 -  By index:
 tableStyle.getConditionalStyles().get(0).getBorders().setColor(Color.BLACK);
 tableStyle.getConditionalStyles().get(0).getBorders().setLineStyle(LineStyle.DOT_DASH);
 Assert.assertEquals(ConditionalStyleType.FIRST_ROW, tableStyle.getConditionalStyles().get(0).getType());

 // 3 -  As a property:
 tableStyle.getConditionalStyles().getFirstRow().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 // Apply padding and text formatting to conditional styles.
 tableStyle.getConditionalStyles().getLastRow().setBottomPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setLeftPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setRightPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setTopPadding(10.0);
 tableStyle.getConditionalStyles().getLastColumn().getFont().setBold(true);

 // List all possible style conditions.
 Iterator enumerator = tableStyle.getConditionalStyles().iterator();
 while (enumerator.hasNext()) {
     ConditionalStyle currentStyle = enumerator.next();
     if (currentStyle != null) System.out.println(currentStyle.getType());
 }

 // Apply the custom style, which contains all conditional styles, to the table.
 table.setStyle(tableStyle);

 // Our style applies some conditional styles by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // We will need to enable all other styles ourselves via the "StyleOptions" property.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.LAST_ROW | TableStyleOptions.LAST_COLUMN);

 doc.save(getArtifactsDir() + "Table.ConditionalStyles.docx");
 
```

**Returns:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle/) - The first row style.
### getLastColumn() {#getLastColumn}
```
public ConditionalStyle getLastColumn()
```


Liefert den Stil der letzten Spalte.

 **Examples:** 

Zeigt, wie man mit bestimmten Bereichsstilen einer Tabelle arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endRow();
 builder.insertCell();
 builder.write("Cell 3");
 builder.insertCell();
 builder.write("Cell 4");
 builder.endTable();

 // Create a custom table style.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");

 // Conditional styles are formatting changes that affect only some of the table's cells
 // based on a predicate, such as the cells being in the last row.
 // Below are three ways of accessing a table style's conditional styles from the "ConditionalStyles" collection.
 // 1 -  By style type:
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.FIRST_ROW).getShading().setBackgroundPatternColor(Color.BLUE);

 // 2 -  By index:
 tableStyle.getConditionalStyles().get(0).getBorders().setColor(Color.BLACK);
 tableStyle.getConditionalStyles().get(0).getBorders().setLineStyle(LineStyle.DOT_DASH);
 Assert.assertEquals(ConditionalStyleType.FIRST_ROW, tableStyle.getConditionalStyles().get(0).getType());

 // 3 -  As a property:
 tableStyle.getConditionalStyles().getFirstRow().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 // Apply padding and text formatting to conditional styles.
 tableStyle.getConditionalStyles().getLastRow().setBottomPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setLeftPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setRightPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setTopPadding(10.0);
 tableStyle.getConditionalStyles().getLastColumn().getFont().setBold(true);

 // List all possible style conditions.
 Iterator enumerator = tableStyle.getConditionalStyles().iterator();
 while (enumerator.hasNext()) {
     ConditionalStyle currentStyle = enumerator.next();
     if (currentStyle != null) System.out.println(currentStyle.getType());
 }

 // Apply the custom style, which contains all conditional styles, to the table.
 table.setStyle(tableStyle);

 // Our style applies some conditional styles by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // We will need to enable all other styles ourselves via the "StyleOptions" property.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.LAST_ROW | TableStyleOptions.LAST_COLUMN);

 doc.save(getArtifactsDir() + "Table.ConditionalStyles.docx");
 
```

**Returns:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle/) - The last column style.
### getLastRow() {#getLastRow}
```
public ConditionalStyle getLastRow()
```


Liefert den Stil der letzten Zeile.

 **Examples:** 

Zeigt, wie man mit bestimmten Bereichsstilen einer Tabelle arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endRow();
 builder.insertCell();
 builder.write("Cell 3");
 builder.insertCell();
 builder.write("Cell 4");
 builder.endTable();

 // Create a custom table style.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");

 // Conditional styles are formatting changes that affect only some of the table's cells
 // based on a predicate, such as the cells being in the last row.
 // Below are three ways of accessing a table style's conditional styles from the "ConditionalStyles" collection.
 // 1 -  By style type:
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.FIRST_ROW).getShading().setBackgroundPatternColor(Color.BLUE);

 // 2 -  By index:
 tableStyle.getConditionalStyles().get(0).getBorders().setColor(Color.BLACK);
 tableStyle.getConditionalStyles().get(0).getBorders().setLineStyle(LineStyle.DOT_DASH);
 Assert.assertEquals(ConditionalStyleType.FIRST_ROW, tableStyle.getConditionalStyles().get(0).getType());

 // 3 -  As a property:
 tableStyle.getConditionalStyles().getFirstRow().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 // Apply padding and text formatting to conditional styles.
 tableStyle.getConditionalStyles().getLastRow().setBottomPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setLeftPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setRightPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setTopPadding(10.0);
 tableStyle.getConditionalStyles().getLastColumn().getFont().setBold(true);

 // List all possible style conditions.
 Iterator enumerator = tableStyle.getConditionalStyles().iterator();
 while (enumerator.hasNext()) {
     ConditionalStyle currentStyle = enumerator.next();
     if (currentStyle != null) System.out.println(currentStyle.getType());
 }

 // Apply the custom style, which contains all conditional styles, to the table.
 table.setStyle(tableStyle);

 // Our style applies some conditional styles by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // We will need to enable all other styles ourselves via the "StyleOptions" property.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.LAST_ROW | TableStyleOptions.LAST_COLUMN);

 doc.save(getArtifactsDir() + "Table.ConditionalStyles.docx");
 
```

**Returns:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle/) - The last row style.
### getOddColumnBanding() {#getOddColumnBanding}
```
public ConditionalStyle getOddColumnBanding()
```


Liefert den Stil für ungerade Spaltenbänder.

 **Examples:** 

Zeigt, wie man mit bestimmten Bereichsstilen einer Tabelle arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endRow();
 builder.insertCell();
 builder.write("Cell 3");
 builder.insertCell();
 builder.write("Cell 4");
 builder.endTable();

 // Create a custom table style.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");

 // Conditional styles are formatting changes that affect only some of the table's cells
 // based on a predicate, such as the cells being in the last row.
 // Below are three ways of accessing a table style's conditional styles from the "ConditionalStyles" collection.
 // 1 -  By style type:
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.FIRST_ROW).getShading().setBackgroundPatternColor(Color.BLUE);

 // 2 -  By index:
 tableStyle.getConditionalStyles().get(0).getBorders().setColor(Color.BLACK);
 tableStyle.getConditionalStyles().get(0).getBorders().setLineStyle(LineStyle.DOT_DASH);
 Assert.assertEquals(ConditionalStyleType.FIRST_ROW, tableStyle.getConditionalStyles().get(0).getType());

 // 3 -  As a property:
 tableStyle.getConditionalStyles().getFirstRow().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 // Apply padding and text formatting to conditional styles.
 tableStyle.getConditionalStyles().getLastRow().setBottomPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setLeftPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setRightPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setTopPadding(10.0);
 tableStyle.getConditionalStyles().getLastColumn().getFont().setBold(true);

 // List all possible style conditions.
 Iterator enumerator = tableStyle.getConditionalStyles().iterator();
 while (enumerator.hasNext()) {
     ConditionalStyle currentStyle = enumerator.next();
     if (currentStyle != null) System.out.println(currentStyle.getType());
 }

 // Apply the custom style, which contains all conditional styles, to the table.
 table.setStyle(tableStyle);

 // Our style applies some conditional styles by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // We will need to enable all other styles ourselves via the "StyleOptions" property.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.LAST_ROW | TableStyleOptions.LAST_COLUMN);

 doc.save(getArtifactsDir() + "Table.ConditionalStyles.docx");
 
```

**Returns:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle/) - The odd column banding style.
### getOddRowBanding() {#getOddRowBanding}
```
public ConditionalStyle getOddRowBanding()
```


Liefert den Stil für ungerade Zeilenbänder.

 **Examples:** 

Zeigt, wie man mit bestimmten Bereichsstilen einer Tabelle arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endRow();
 builder.insertCell();
 builder.write("Cell 3");
 builder.insertCell();
 builder.write("Cell 4");
 builder.endTable();

 // Create a custom table style.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");

 // Conditional styles are formatting changes that affect only some of the table's cells
 // based on a predicate, such as the cells being in the last row.
 // Below are three ways of accessing a table style's conditional styles from the "ConditionalStyles" collection.
 // 1 -  By style type:
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.FIRST_ROW).getShading().setBackgroundPatternColor(Color.BLUE);

 // 2 -  By index:
 tableStyle.getConditionalStyles().get(0).getBorders().setColor(Color.BLACK);
 tableStyle.getConditionalStyles().get(0).getBorders().setLineStyle(LineStyle.DOT_DASH);
 Assert.assertEquals(ConditionalStyleType.FIRST_ROW, tableStyle.getConditionalStyles().get(0).getType());

 // 3 -  As a property:
 tableStyle.getConditionalStyles().getFirstRow().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 // Apply padding and text formatting to conditional styles.
 tableStyle.getConditionalStyles().getLastRow().setBottomPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setLeftPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setRightPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setTopPadding(10.0);
 tableStyle.getConditionalStyles().getLastColumn().getFont().setBold(true);

 // List all possible style conditions.
 Iterator enumerator = tableStyle.getConditionalStyles().iterator();
 while (enumerator.hasNext()) {
     ConditionalStyle currentStyle = enumerator.next();
     if (currentStyle != null) System.out.println(currentStyle.getType());
 }

 // Apply the custom style, which contains all conditional styles, to the table.
 table.setStyle(tableStyle);

 // Our style applies some conditional styles by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // We will need to enable all other styles ourselves via the "StyleOptions" property.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.LAST_ROW | TableStyleOptions.LAST_COLUMN);

 doc.save(getArtifactsDir() + "Table.ConditionalStyles.docx");
 
```

**Returns:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle/) - The odd row banding style.
### getTopLeftCell() {#getTopLeftCell}
```
public ConditionalStyle getTopLeftCell()
```


Liefert den Stil der oberen linken Zelle.

 **Examples:** 

Zeigt, wie man mit bestimmten Bereichsstilen einer Tabelle arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endRow();
 builder.insertCell();
 builder.write("Cell 3");
 builder.insertCell();
 builder.write("Cell 4");
 builder.endTable();

 // Create a custom table style.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");

 // Conditional styles are formatting changes that affect only some of the table's cells
 // based on a predicate, such as the cells being in the last row.
 // Below are three ways of accessing a table style's conditional styles from the "ConditionalStyles" collection.
 // 1 -  By style type:
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.FIRST_ROW).getShading().setBackgroundPatternColor(Color.BLUE);

 // 2 -  By index:
 tableStyle.getConditionalStyles().get(0).getBorders().setColor(Color.BLACK);
 tableStyle.getConditionalStyles().get(0).getBorders().setLineStyle(LineStyle.DOT_DASH);
 Assert.assertEquals(ConditionalStyleType.FIRST_ROW, tableStyle.getConditionalStyles().get(0).getType());

 // 3 -  As a property:
 tableStyle.getConditionalStyles().getFirstRow().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 // Apply padding and text formatting to conditional styles.
 tableStyle.getConditionalStyles().getLastRow().setBottomPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setLeftPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setRightPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setTopPadding(10.0);
 tableStyle.getConditionalStyles().getLastColumn().getFont().setBold(true);

 // List all possible style conditions.
 Iterator enumerator = tableStyle.getConditionalStyles().iterator();
 while (enumerator.hasNext()) {
     ConditionalStyle currentStyle = enumerator.next();
     if (currentStyle != null) System.out.println(currentStyle.getType());
 }

 // Apply the custom style, which contains all conditional styles, to the table.
 table.setStyle(tableStyle);

 // Our style applies some conditional styles by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // We will need to enable all other styles ourselves via the "StyleOptions" property.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.LAST_ROW | TableStyleOptions.LAST_COLUMN);

 doc.save(getArtifactsDir() + "Table.ConditionalStyles.docx");
 
```

**Returns:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle/) - The top left cell style.
### getTopRightCell() {#getTopRightCell}
```
public ConditionalStyle getTopRightCell()
```


Liefert den Stil der oberen rechten Zelle.

 **Examples:** 

Zeigt, wie man mit bestimmten Bereichsstilen einer Tabelle arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endRow();
 builder.insertCell();
 builder.write("Cell 3");
 builder.insertCell();
 builder.write("Cell 4");
 builder.endTable();

 // Create a custom table style.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");

 // Conditional styles are formatting changes that affect only some of the table's cells
 // based on a predicate, such as the cells being in the last row.
 // Below are three ways of accessing a table style's conditional styles from the "ConditionalStyles" collection.
 // 1 -  By style type:
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.FIRST_ROW).getShading().setBackgroundPatternColor(Color.BLUE);

 // 2 -  By index:
 tableStyle.getConditionalStyles().get(0).getBorders().setColor(Color.BLACK);
 tableStyle.getConditionalStyles().get(0).getBorders().setLineStyle(LineStyle.DOT_DASH);
 Assert.assertEquals(ConditionalStyleType.FIRST_ROW, tableStyle.getConditionalStyles().get(0).getType());

 // 3 -  As a property:
 tableStyle.getConditionalStyles().getFirstRow().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 // Apply padding and text formatting to conditional styles.
 tableStyle.getConditionalStyles().getLastRow().setBottomPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setLeftPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setRightPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setTopPadding(10.0);
 tableStyle.getConditionalStyles().getLastColumn().getFont().setBold(true);

 // List all possible style conditions.
 Iterator enumerator = tableStyle.getConditionalStyles().iterator();
 while (enumerator.hasNext()) {
     ConditionalStyle currentStyle = enumerator.next();
     if (currentStyle != null) System.out.println(currentStyle.getType());
 }

 // Apply the custom style, which contains all conditional styles, to the table.
 table.setStyle(tableStyle);

 // Our style applies some conditional styles by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // We will need to enable all other styles ourselves via the "StyleOptions" property.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.LAST_ROW | TableStyleOptions.LAST_COLUMN);

 doc.save(getArtifactsDir() + "Table.ConditionalStyles.docx");
 
```

**Returns:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle/) - The top right cell style.
### iterator() {#iterator}
```
public Iterator iterator()
```


Gibt ein Enumerator-Objekt zurück, das verwendet werden kann, um über alle bedingten Stile in der Sammlung zu iterieren.

 **Examples:** 

Zeigt, wie man mit bestimmten Bereichsstilen einer Tabelle arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endRow();
 builder.insertCell();
 builder.write("Cell 3");
 builder.insertCell();
 builder.write("Cell 4");
 builder.endTable();

 // Create a custom table style.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");

 // Conditional styles are formatting changes that affect only some of the table's cells
 // based on a predicate, such as the cells being in the last row.
 // Below are three ways of accessing a table style's conditional styles from the "ConditionalStyles" collection.
 // 1 -  By style type:
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.FIRST_ROW).getShading().setBackgroundPatternColor(Color.BLUE);

 // 2 -  By index:
 tableStyle.getConditionalStyles().get(0).getBorders().setColor(Color.BLACK);
 tableStyle.getConditionalStyles().get(0).getBorders().setLineStyle(LineStyle.DOT_DASH);
 Assert.assertEquals(ConditionalStyleType.FIRST_ROW, tableStyle.getConditionalStyles().get(0).getType());

 // 3 -  As a property:
 tableStyle.getConditionalStyles().getFirstRow().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 // Apply padding and text formatting to conditional styles.
 tableStyle.getConditionalStyles().getLastRow().setBottomPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setLeftPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setRightPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setTopPadding(10.0);
 tableStyle.getConditionalStyles().getLastColumn().getFont().setBold(true);

 // List all possible style conditions.
 Iterator enumerator = tableStyle.getConditionalStyles().iterator();
 while (enumerator.hasNext()) {
     ConditionalStyle currentStyle = enumerator.next();
     if (currentStyle != null) System.out.println(currentStyle.getType());
 }

 // Apply the custom style, which contains all conditional styles, to the table.
 table.setStyle(tableStyle);

 // Our style applies some conditional styles by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // We will need to enable all other styles ourselves via the "StyleOptions" property.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.LAST_ROW | TableStyleOptions.LAST_COLUMN);

 doc.save(getArtifactsDir() + "Table.ConditionalStyles.docx");
 
```

**Returns:**
java.util.Iterator
