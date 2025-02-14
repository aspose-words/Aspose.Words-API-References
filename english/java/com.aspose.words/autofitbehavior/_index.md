---
title: AutoFitBehavior
linktitle: AutoFitBehavior
second_title: Aspose.Words for Java
description: Determines how Aspose.Words resizes the table when you invoke the MAspose.Words.Tables.Table.AutoFitAspose.Words.Tables.AutoFitBehavior method in Java.
type: docs
weight: 21
url: /java/com.aspose.words/autofitbehavior/
---

**Inheritance:**
java.lang.Object
```
public class AutoFitBehavior
```

Determines how Aspose.Words resizes the table when you invoke the **M:Aspose.Words.Tables.Table.AutoFit(Aspose.Words.Tables.AutoFitBehavior)** method.

 **Examples:** 

Shows how to build a new table while applying a style.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // We must insert at least one row before setting any table formatting.
 builder.insertCell();

 // Set the table style used based on the style identifier.
 // Note that not all table styles are available when saving to .doc format.
 table.setStyleIdentifier(StyleIdentifier.MEDIUM_SHADING_1_ACCENT_1);

 // Partially apply the style to features of the table based on predicates, then build the table.
 table.setStyleOptions(TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS | TableStyleOptions.FIRST_ROW);
 table.autoFit(AutoFitBehavior.AUTO_FIT_TO_CONTENTS);

 builder.writeln("Item");
 builder.getCellFormat().setRightPadding(40.0);
 builder.insertCell();
 builder.writeln("Quantity (kg)");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Apples");
 builder.insertCell();
 builder.writeln("20");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Bananas");
 builder.insertCell();
 builder.writeln("40");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Carrots");
 builder.insertCell();
 builder.writeln("50");
 builder.endRow();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTableWithStyle.docx");
 
```

Shows how to build a formatted 2x2 table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [AUTO_FIT_TO_CONTENTS](#AUTO-FIT-TO-CONTENTS) | Aspose.Words enables the AutoFit option, removes the preferred width from the table and all cells and then updates the table layout. |
| [AUTO_FIT_TO_WINDOW](#AUTO-FIT-TO-WINDOW) | When you use this value, Aspose.Words enables the AutoFit option, sets the preferred width for the table to 100%, removes preferred widths from all cells and then updates the table layout. |
| [FIXED_COLUMN_WIDTHS](#FIXED-COLUMN-WIDTHS) | Aspose.Words disables the AutoFit option and removes the preferred with from the table. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String autoFitBehaviorName)](#fromName-java.lang.String) |  |
| [getName(int autoFitBehavior)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int autoFitBehavior)](#toString-int) |  |
### AUTO_FIT_TO_CONTENTS {#AUTO-FIT-TO-CONTENTS}
```
public static int AUTO_FIT_TO_CONTENTS
```


Aspose.Words enables the AutoFit option, removes the preferred width from the table and all cells and then updates the table layout.

In the resulting table, cell widths are updated to fit the table contents. Most likely, the table will shrink.

### AUTO_FIT_TO_WINDOW {#AUTO-FIT-TO-WINDOW}
```
public static int AUTO_FIT_TO_WINDOW
```


When you use this value, Aspose.Words enables the AutoFit option, sets the preferred width for the table to 100%, removes preferred widths from all cells and then updates the table layout.

As a result, the table occupies all available width and the cell widths are updated to fit table contents.

### FIXED_COLUMN_WIDTHS {#FIXED-COLUMN-WIDTHS}
```
public static int FIXED_COLUMN_WIDTHS
```


Aspose.Words disables the AutoFit option and removes the preferred with from the table.

The widths of the cells remain as they are specified by their [CellFormat.getWidth()](../../com.aspose.words/cellformat/\#getWidth) / [CellFormat.setWidth(double)](../../com.aspose.words/cellformat/\#setWidth-double) properties.

### length {#length}
```
public static int length
```


### fromName(String autoFitBehaviorName) {#fromName-java.lang.String}
```
public static int fromName(String autoFitBehaviorName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| autoFitBehaviorName | java.lang.String |  |

**Returns:**
int
### getName(int autoFitBehavior) {#getName-int}
```
public static String getName(int autoFitBehavior)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| autoFitBehavior | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int autoFitBehavior) {#toString-int}
```
public static String toString(int autoFitBehavior)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| autoFitBehavior | int |  |

**Returns:**
java.lang.String
