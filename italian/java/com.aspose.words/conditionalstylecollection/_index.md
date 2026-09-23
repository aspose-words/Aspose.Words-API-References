---
title: "ConditionalStyleCollection"
linktitle: "ConditionalStyleCollection"
second_title: "Aspose.Words per Java"
description: "Rappresenta una raccolta di oggetti ConditionalStyle in Java."
type: docs
weight: 124
url: /it/java/com.aspose.words/conditionalstylecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ConditionalStyleCollection implements Iterable
```

Rappresenta una raccolta di oggetti [ConditionalStyle](../../com.aspose.words/conditionalstyle/).

Per saperne di più, visita l'articolo di documentazione [ Working with Tables ][Working with Tables].

 **Remarks:** 

Non è possibile aggiungere o rimuovere elementi da questa raccolta. Contiene un set permanente di elementi: un elemento per ogni valore del tipo di enumerazione [ConditionalStyleType](../../com.aspose.words/conditionalstyletype/).

 **Examples:** 

Mostra come lavorare con alcuni stili di area di una tabella.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Cancella tutti gli stili condizionali dello stile tabella. |
| [get(int index)](#get-int) | Recupera un oggetto [ConditionalStyle](../../com.aspose.words/conditionalstyle/) per indice. |
| [getBottomLeftCell()](#getBottomLeftCell) | Ottiene lo stile della cella in basso a sinistra. |
| [getBottomRightCell()](#getBottomRightCell) | Ottiene lo stile della cella in basso a destra. |
| [getByConditionalStyleType(int conditionalStyleType)](#getByConditionalStyleType-int) |  |
| [getCount()](#getCount) | Ottiene il numero di stili condizionali nella raccolta. |
| [getEvenColumnBanding()](#getEvenColumnBanding) | Ottiene lo stile di bande delle colonne pari. |
| [getEvenRowBanding()](#getEvenRowBanding) | Ottiene lo stile di bande delle righe pari. |
| [getFirstColumn()](#getFirstColumn) | Ottiene lo stile della prima colonna. |
| [getFirstRow()](#getFirstRow) | Ottiene lo stile della prima riga. |
| [getLastColumn()](#getLastColumn) | Ottiene lo stile dell'ultima colonna. |
| [getLastRow()](#getLastRow) | Ottiene lo stile dell'ultima riga. |
| [getOddColumnBanding()](#getOddColumnBanding) | Ottiene lo stile di bande delle colonne dispari. |
| [getOddRowBanding()](#getOddRowBanding) | Ottiene lo stile di bande delle righe dispari. |
| [getTopLeftCell()](#getTopLeftCell) | Ottiene lo stile della cella in alto a sinistra. |
| [getTopRightCell()](#getTopRightCell) | Ottiene lo stile della cella in alto a destra. |
| [iterator()](#iterator) | Restituisce un oggetto enumeratore che può essere usato per iterare tutti gli stili condizionali nella raccolta. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Cancella tutti gli stili condizionali dello stile tabella.

 **Examples:** 

Mostra come ripristinare gli stili di tabella condizionali.

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


Recupera un oggetto [ConditionalStyle](../../com.aspose.words/conditionalstyle/) per indice.

 **Examples:** 

Mostra come lavorare con alcuni stili di area di una tabella.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | Indice basato su zero dello stile condizionale da recuperare. |

**Returns:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle/) - The corresponding [ConditionalStyle](../../com.aspose.words/conditionalstyle/) value.
### getBottomLeftCell() {#getBottomLeftCell}
```
public ConditionalStyle getBottomLeftCell()
```


Ottiene lo stile della cella in basso a sinistra.

 **Examples:** 

Mostra come lavorare con alcuni stili di area di una tabella.

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


Ottiene lo stile della cella in basso a destra.

 **Examples:** 

Mostra come lavorare con alcuni stili di area di una tabella.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| conditionalStyleType | int |  |

**Returns:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle/)
### getCount() {#getCount}
```
public int getCount()
```


Ottiene il numero di stili condizionali nella raccolta.

 **Examples:** 

Mostra come lavorare con alcuni stili di area di una tabella.

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
int - Il numero di stili condizionali nella raccolta.
### getEvenColumnBanding() {#getEvenColumnBanding}
```
public ConditionalStyle getEvenColumnBanding()
```


Ottiene lo stile di bande delle colonne pari.

 **Examples:** 

Mostra come lavorare con alcuni stili di area di una tabella.

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


Ottiene lo stile di bande delle righe pari.

 **Examples:** 

Mostra come lavorare con alcuni stili di area di una tabella.

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


Ottiene lo stile della prima colonna.

 **Examples:** 

Mostra come lavorare con alcuni stili di area di una tabella.

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


Ottiene lo stile della prima riga.

 **Examples:** 

Mostra come lavorare con alcuni stili di area di una tabella.

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


Ottiene lo stile dell'ultima colonna.

 **Examples:** 

Mostra come lavorare con alcuni stili di area di una tabella.

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


Ottiene lo stile dell'ultima riga.

 **Examples:** 

Mostra come lavorare con alcuni stili di area di una tabella.

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


Ottiene lo stile di bande delle colonne dispari.

 **Examples:** 

Mostra come lavorare con alcuni stili di area di una tabella.

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


Ottiene lo stile di bande delle righe dispari.

 **Examples:** 

Mostra come lavorare con alcuni stili di area di una tabella.

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


Ottiene lo stile della cella in alto a sinistra.

 **Examples:** 

Mostra come lavorare con alcuni stili di area di una tabella.

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


Ottiene lo stile della cella in alto a destra.

 **Examples:** 

Mostra come lavorare con alcuni stili di area di una tabella.

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


Restituisce un oggetto enumeratore che può essere usato per iterare tutti gli stili condizionali nella raccolta.

 **Examples:** 

Mostra come lavorare con alcuni stili di area di una tabella.

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
