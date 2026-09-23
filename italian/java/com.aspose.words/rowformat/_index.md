---
title: "RowFormat"
linktitle: "RowFormat"
second_title: "Aspose.Words per Java"
description: "Rappresenta tutta la formattazione per una riga di tabella in Java."
type: docs
weight: 590
url: /it/java/com.aspose.words/rowformat/
---

**Inheritance:**
java.lang.Object
```
public class RowFormat
```

Rappresenta tutta la formattazione per una riga di tabella.

Per saperne di più, visita l'articolo di documentazione [ Working with Tables ][Working with Tables].

 **Examples:** 

Mostra come creare una tabella con bordi personalizzati.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Mostra come modificare il formato di righe e celle in una tabella.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("City");
 builder.insertCell();
 builder.write("Country");
 builder.endRow();
 builder.insertCell();
 builder.write("London");
 builder.insertCell();
 builder.write("U.K.");
 builder.endTable();

 // Use the first row's "RowFormat" property to modify the formatting
 // of the contents of all cells in this row.
 RowFormat rowFormat = table.getFirstRow().getRowFormat();
 rowFormat.setHeight(25.0);
 rowFormat.getBorders().getByBorderType(BorderType.BOTTOM).setColor(Color.RED);

 // Use the "CellFormat" property of the first cell in the last row to modify the formatting of that cell's contents.
 CellFormat cellFormat = table.getLastRow().getFirstCell().getCellFormat();
 cellFormat.setWidth(100.0);
 cellFormat.getShading().setBackgroundPatternColor(Color.ORANGE);

 doc.save(getArtifactsDir() + "Table.RowCellFormat.docx");
 
```

Mostra come modificare la formattazione di una riga di tabella.

```

 Document doc = new Document(getMyDir() + "Tables.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Use the first row's "RowFormat" property to set formatting that modifies that entire row's appearance.
 Row firstRow = table.getFirstRow();
 firstRow.getRowFormat().getBorders().setLineStyle(LineStyle.NONE);
 firstRow.getRowFormat().setHeightRule(HeightRule.AUTO);
 firstRow.getRowFormat().setAllowBreakAcrossPages(true);

 doc.save(getArtifactsDir() + "Table.RowFormat.docx");
 
```


[Working with Tables]: https://docs.aspose.com/words/java/working-with-tables/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Ripristina la formattazione predefinita della riga. |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [getAllowBreakAcrossPages()](#getAllowBreakAcrossPages) | Vero se il testo in una riga di tabella può essere diviso tra interruzioni di pagina. |
| [getBorders()](#getBorders) | Ottiene la raccolta dei bordi predefiniti delle celle per la riga. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getHeadingFormat()](#getHeadingFormat) | Vero se la riga viene ripetuta come intestazione della tabella su ogni pagina quando la tabella si estende su più di una pagina. |
| [getHeight()](#getHeight) | Ottiene l'altezza della riga della tabella in punti. |
| [getHeightRule()](#getHeightRule) | Ottiene la regola per determinare l'altezza della riga della tabella. |
| [setAllowBreakAcrossPages(boolean value)](#setAllowBreakAcrossPages-boolean) | Vero se il testo in una riga di tabella può essere diviso tra interruzioni di pagina. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setHeadingFormat(boolean value)](#setHeadingFormat-boolean) | Vero se la riga viene ripetuta come intestazione della tabella su ogni pagina quando la tabella si estende su più di una pagina. |
| [setHeight(double value)](#setHeight-double) | Imposta l'altezza della riga della tabella in punti. |
| [setHeightRule(int value)](#setHeightRule-int) | Imposta la regola per determinare l'altezza della riga della tabella. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Ripristina la formattazione predefinita della riga.

 **Examples:** 

Mostra come creare una tabella con bordi personalizzati.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int}
```
public Object fetchInheritedBorderAttr(int key)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getAllowBreakAcrossPages() {#getAllowBreakAcrossPages}
```
public boolean getAllowBreakAcrossPages()
```


Vero se il testo in una riga di tabella può essere diviso tra interruzioni di pagina.

 **Examples:** 

Mostra come disabilitare la divisione delle righe tra pagine per ogni riga in una tabella.

```

 Document doc = new Document(getMyDir() + "Table spanning two pages.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Set the "AllowBreakAcrossPages" property to "false" to keep the row
 // in one piece if a table spans two pages, which break up along that row.
 // If the row is too big to fit in one page, Microsoft Word will push it down to the next page.
 // Set the "AllowBreakAcrossPages" property to "true" to allow the row to break up across two pages.
 for (Row row : table.getRows())
     row.getRowFormat().setAllowBreakAcrossPages(allowBreakAcrossPages);

 doc.save(getArtifactsDir() + "Table.AllowBreakAcrossPages.docx");
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


Ottiene la raccolta dei bordi predefiniti delle celle per la riga.

 **Examples:** 

Mostra come creare una tabella con bordi personalizzati.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

**Returns:**
[BorderCollection](../../com.aspose.words/bordercollection/) - The collection of default cell borders for the row.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getHeadingFormat() {#getHeadingFormat}
```
public boolean getHeadingFormat()
```


Vero se la riga viene ripetuta come intestazione della tabella su ogni pagina quando la tabella si estende su più di una pagina.

 **Examples:** 

Mostra come creare una tabella con righe che si ripetono su ogni pagina.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();

 // Any rows inserted while the "HeadingFormat" flag is set to "true"
 // will show up at the top of the table on every page that it spans.
 builder.getRowFormat().setHeadingFormat(true);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.getCellFormat().setWidth(100.0);
 builder.insertCell();
 builder.write("Heading row 1");
 builder.endRow();
 builder.insertCell();
 builder.write("Heading row 2");
 builder.endRow();

 builder.getCellFormat().setWidth(50.0);
 builder.getParagraphFormat().clearFormatting();
 builder.getRowFormat().setHeadingFormat(false);

 // Add enough rows for the table to span two pages.
 for (int i = 0; i < 50; i++) {
     builder.insertCell();
     builder.write(MessageFormat.format("Row {0}, column 1.", table.getRows().toArray().length));
     builder.insertCell();
     builder.write(MessageFormat.format("Row {0}, column 2.", table.getRows().toArray().length));
     builder.endRow();
 }

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTableSetHeadingRow.docx");
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getHeight() {#getHeight}
```
public double getHeight()
```


Ottiene l'altezza della riga della tabella in punti.

 **Examples:** 

Mostra come creare una tabella formattata usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 table.setLeftIndent(20.0);

 // Set some formatting options for text and table appearance.
 builder.getRowFormat().setHeight(40.0);
 builder.getRowFormat().setHeightRule(HeightRule.AT_LEAST);
 builder.getCellFormat().getShading().setBackgroundPatternColor(new Color((198), (217), (241)));

 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.getFont().setSize(16.0);
 builder.getFont().setName("Arial");
 builder.getFont().setBold(true);

 // Configuring the formatting options in a document builder will apply them
 // to the current cell/row its cursor is in,
 // as well as any new cells and rows created using that builder.
 builder.write("Header Row,\n Cell 1");
 builder.insertCell();
 builder.write("Header Row,\n Cell 2");
 builder.insertCell();
 builder.write("Header Row,\n Cell 3");
 builder.endRow();

 // Reconfigure the builder's formatting objects for new rows and cells that we are about to make.
 // The builder will not apply these to the first row already created so that it will stand out as a header row.
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.WHITE);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getRowFormat().setHeight(30.0);
 builder.getRowFormat().setHeightRule(HeightRule.AUTO);
 builder.insertCell();
 builder.getFont().setSize(12.0);
 builder.getFont().setBold(false);

 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");
 builder.insertCell();
 builder.write("Row 1, Cell 3.");
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.insertCell();
 builder.write("Row 2, Cell 3.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateFormattedTable.docx");
 
```

Mostra come formattare le righe con un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Start a second row, and then configure its height. The builder will apply these settings to
 // its current row, as well as any new rows it creates afterwards.
 builder.endRow();

 RowFormat rowFormat = builder.getRowFormat();
 rowFormat.setHeight(100.0);
 rowFormat.setHeightRule(HeightRule.EXACTLY);

 builder.insertCell();
 builder.write("Row 2, cell 1.");
 builder.endTable();

 // The first row was unaffected by the padding reconfiguration and still holds the default values.
 Assert.assertEquals(0.0d, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());

 Assert.assertEquals(100.0d, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());

 doc.save(getArtifactsDir() + "DocumentBuilder.SetRowFormatting.docx");
 
```

**Returns:**
double - L'altezza della riga della tabella in punti.
### getHeightRule() {#getHeightRule}
```
public int getHeightRule()
```


Ottiene la regola per determinare l'altezza della riga della tabella.

 **Examples:** 

Mostra come creare una tabella formattata usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 table.setLeftIndent(20.0);

 // Set some formatting options for text and table appearance.
 builder.getRowFormat().setHeight(40.0);
 builder.getRowFormat().setHeightRule(HeightRule.AT_LEAST);
 builder.getCellFormat().getShading().setBackgroundPatternColor(new Color((198), (217), (241)));

 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.getFont().setSize(16.0);
 builder.getFont().setName("Arial");
 builder.getFont().setBold(true);

 // Configuring the formatting options in a document builder will apply them
 // to the current cell/row its cursor is in,
 // as well as any new cells and rows created using that builder.
 builder.write("Header Row,\n Cell 1");
 builder.insertCell();
 builder.write("Header Row,\n Cell 2");
 builder.insertCell();
 builder.write("Header Row,\n Cell 3");
 builder.endRow();

 // Reconfigure the builder's formatting objects for new rows and cells that we are about to make.
 // The builder will not apply these to the first row already created so that it will stand out as a header row.
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.WHITE);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getRowFormat().setHeight(30.0);
 builder.getRowFormat().setHeightRule(HeightRule.AUTO);
 builder.insertCell();
 builder.getFont().setSize(12.0);
 builder.getFont().setBold(false);

 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");
 builder.insertCell();
 builder.write("Row 1, Cell 3.");
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.insertCell();
 builder.write("Row 2, Cell 3.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateFormattedTable.docx");
 
```

Mostra come formattare le righe con un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Start a second row, and then configure its height. The builder will apply these settings to
 // its current row, as well as any new rows it creates afterwards.
 builder.endRow();

 RowFormat rowFormat = builder.getRowFormat();
 rowFormat.setHeight(100.0);
 rowFormat.setHeightRule(HeightRule.EXACTLY);

 builder.insertCell();
 builder.write("Row 2, cell 1.");
 builder.endTable();

 // The first row was unaffected by the padding reconfiguration and still holds the default values.
 Assert.assertEquals(0.0d, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());

 Assert.assertEquals(100.0d, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());

 doc.save(getArtifactsDir() + "DocumentBuilder.SetRowFormatting.docx");
 
```

**Returns:**
int - La regola per determinare l'altezza della riga della tabella. Il valore restituito è uno dei costanti [HeightRule](../../com.aspose.words/heightrule/) .
### setAllowBreakAcrossPages(boolean value) {#setAllowBreakAcrossPages-boolean}
```
public void setAllowBreakAcrossPages(boolean value)
```


Vero se il testo in una riga di tabella può essere diviso tra interruzioni di pagina.

 **Examples:** 

Mostra come disabilitare la divisione delle righe tra pagine per ogni riga in una tabella.

```

 Document doc = new Document(getMyDir() + "Table spanning two pages.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Set the "AllowBreakAcrossPages" property to "false" to keep the row
 // in one piece if a table spans two pages, which break up along that row.
 // If the row is too big to fit in one page, Microsoft Word will push it down to the next page.
 // Set the "AllowBreakAcrossPages" property to "true" to allow the row to break up across two pages.
 for (Row row : table.getRows())
     row.getRowFormat().setAllowBreakAcrossPages(allowBreakAcrossPages);

 doc.save(getArtifactsDir() + "Table.AllowBreakAcrossPages.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| key | int |  |
| valore | java.lang.Object |  |

### setHeadingFormat(boolean value) {#setHeadingFormat-boolean}
```
public void setHeadingFormat(boolean value)
```


Vero se la riga viene ripetuta come intestazione della tabella su ogni pagina quando la tabella si estende su più di una pagina.

 **Examples:** 

Mostra come creare una tabella con righe che si ripetono su ogni pagina.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();

 // Any rows inserted while the "HeadingFormat" flag is set to "true"
 // will show up at the top of the table on every page that it spans.
 builder.getRowFormat().setHeadingFormat(true);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.getCellFormat().setWidth(100.0);
 builder.insertCell();
 builder.write("Heading row 1");
 builder.endRow();
 builder.insertCell();
 builder.write("Heading row 2");
 builder.endRow();

 builder.getCellFormat().setWidth(50.0);
 builder.getParagraphFormat().clearFormatting();
 builder.getRowFormat().setHeadingFormat(false);

 // Add enough rows for the table to span two pages.
 for (int i = 0; i < 50; i++) {
     builder.insertCell();
     builder.write(MessageFormat.format("Row {0}, column 1.", table.getRows().toArray().length));
     builder.insertCell();
     builder.write(MessageFormat.format("Row {0}, column 2.", table.getRows().toArray().length));
     builder.endRow();
 }

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTableSetHeadingRow.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setHeight(double value) {#setHeight-double}
```
public void setHeight(double value)
```


Imposta l'altezza della riga della tabella in punti.

 **Examples:** 

Mostra come creare una tabella formattata usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 table.setLeftIndent(20.0);

 // Set some formatting options for text and table appearance.
 builder.getRowFormat().setHeight(40.0);
 builder.getRowFormat().setHeightRule(HeightRule.AT_LEAST);
 builder.getCellFormat().getShading().setBackgroundPatternColor(new Color((198), (217), (241)));

 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.getFont().setSize(16.0);
 builder.getFont().setName("Arial");
 builder.getFont().setBold(true);

 // Configuring the formatting options in a document builder will apply them
 // to the current cell/row its cursor is in,
 // as well as any new cells and rows created using that builder.
 builder.write("Header Row,\n Cell 1");
 builder.insertCell();
 builder.write("Header Row,\n Cell 2");
 builder.insertCell();
 builder.write("Header Row,\n Cell 3");
 builder.endRow();

 // Reconfigure the builder's formatting objects for new rows and cells that we are about to make.
 // The builder will not apply these to the first row already created so that it will stand out as a header row.
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.WHITE);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getRowFormat().setHeight(30.0);
 builder.getRowFormat().setHeightRule(HeightRule.AUTO);
 builder.insertCell();
 builder.getFont().setSize(12.0);
 builder.getFont().setBold(false);

 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");
 builder.insertCell();
 builder.write("Row 1, Cell 3.");
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.insertCell();
 builder.write("Row 2, Cell 3.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateFormattedTable.docx");
 
```

Mostra come formattare le righe con un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Start a second row, and then configure its height. The builder will apply these settings to
 // its current row, as well as any new rows it creates afterwards.
 builder.endRow();

 RowFormat rowFormat = builder.getRowFormat();
 rowFormat.setHeight(100.0);
 rowFormat.setHeightRule(HeightRule.EXACTLY);

 builder.insertCell();
 builder.write("Row 2, cell 1.");
 builder.endTable();

 // The first row was unaffected by the padding reconfiguration and still holds the default values.
 Assert.assertEquals(0.0d, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());

 Assert.assertEquals(100.0d, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());

 doc.save(getArtifactsDir() + "DocumentBuilder.SetRowFormatting.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | L'altezza della riga della tabella in punti. |

### setHeightRule(int value) {#setHeightRule-int}
```
public void setHeightRule(int value)
```


Imposta la regola per determinare l'altezza della riga della tabella.

 **Examples:** 

Mostra come creare una tabella formattata usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 table.setLeftIndent(20.0);

 // Set some formatting options for text and table appearance.
 builder.getRowFormat().setHeight(40.0);
 builder.getRowFormat().setHeightRule(HeightRule.AT_LEAST);
 builder.getCellFormat().getShading().setBackgroundPatternColor(new Color((198), (217), (241)));

 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.getFont().setSize(16.0);
 builder.getFont().setName("Arial");
 builder.getFont().setBold(true);

 // Configuring the formatting options in a document builder will apply them
 // to the current cell/row its cursor is in,
 // as well as any new cells and rows created using that builder.
 builder.write("Header Row,\n Cell 1");
 builder.insertCell();
 builder.write("Header Row,\n Cell 2");
 builder.insertCell();
 builder.write("Header Row,\n Cell 3");
 builder.endRow();

 // Reconfigure the builder's formatting objects for new rows and cells that we are about to make.
 // The builder will not apply these to the first row already created so that it will stand out as a header row.
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.WHITE);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getRowFormat().setHeight(30.0);
 builder.getRowFormat().setHeightRule(HeightRule.AUTO);
 builder.insertCell();
 builder.getFont().setSize(12.0);
 builder.getFont().setBold(false);

 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");
 builder.insertCell();
 builder.write("Row 1, Cell 3.");
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.insertCell();
 builder.write("Row 2, Cell 3.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateFormattedTable.docx");
 
```

Mostra come formattare le righe con un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Start a second row, and then configure its height. The builder will apply these settings to
 // its current row, as well as any new rows it creates afterwards.
 builder.endRow();

 RowFormat rowFormat = builder.getRowFormat();
 rowFormat.setHeight(100.0);
 rowFormat.setHeightRule(HeightRule.EXACTLY);

 builder.insertCell();
 builder.write("Row 2, cell 1.");
 builder.endTable();

 // The first row was unaffected by the padding reconfiguration and still holds the default values.
 Assert.assertEquals(0.0d, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());

 Assert.assertEquals(100.0d, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());

 doc.save(getArtifactsDir() + "DocumentBuilder.SetRowFormatting.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | La regola per determinare l'altezza della riga della tabella. Il valore deve essere uno dei costanti [HeightRule](../../com.aspose.words/heightrule/) . |

