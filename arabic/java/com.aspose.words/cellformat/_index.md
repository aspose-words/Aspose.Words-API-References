---
title: "CellFormat"
linktitle: "CellFormat"
second_title: "Aspose.Words لـ Java"
description: "يمثل جميع تنسيقات خلية الجدول في Java."
type: docs
weight: 61
url: /ar/java/com.aspose.words/cellformat/
---

**Inheritance:**
java.lang.Object
```
public class CellFormat
```

يمثل كل التنسيقات لخلية جدول.

للتعرف على المزيد، زر مقالة الوثائق [ Working with Tables ][Working with Tables].

 **Examples:** 

يوضح كيفية إنشاء جدول بحدود مخصصة.

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

يوضح كيفية تعديل تنسيق الصفوف والخلايا في جدول.

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

يوضح كيفية تعديل تنسيق خلية الجدول.

```

 Document doc = new Document(getMyDir() + "Tables.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);
 Cell firstCell = table.getFirstRow().getFirstCell();

 // Use a cell's "CellFormat" property to set formatting that modifies the appearance of that cell.
 firstCell.getCellFormat().setWidth(30.0);
 firstCell.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 firstCell.getCellFormat().getShading().setForegroundPatternColor(Color.GREEN);

 doc.save(getArtifactsDir() + "Table.CellFormat.docx");
 
```


[Working with Tables]: https://docs.aspose.com/words/java/working-with-tables/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [clearFormatting()](#clearFormatting) | يعيد تعيين تنسيق الخلية إلى الافتراضي. |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int) |  |
| [getBorders()](#getBorders) | يحصل على مجموعة حدود الخلية. |
| [getBottomPadding()](#getBottomPadding) | يحصل على مقدار المسافة (بالنقاط) لإضافتها أسفل محتويات الخلية. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getFitText()](#getFitText) | إذا كان  true , يضبط النص داخل الخلية، مضغًا كل فقرة إلى عرض الخلية. |
| [getHideMark()](#getHideMark) | يحصل على رؤية علامة الخلية. |
| [getHorizontalMerge()](#getHorizontalMerge) | يحدد كيفية دمج الخلية أفقياً مع خلايا أخرى في الصف. |
| [getLeftPadding()](#getLeftPadding) | يحصل على مقدار المسافة (بالنقاط) لإضافتها إلى يسار محتوى الخلية. |
| [getOrientation()](#getOrientation) | يحصل على اتجاه النص في خلية الجدول. |
| [getPreferredWidth()](#getPreferredWidth) | يحصل على العرض المفضل للخلية. |
| [getRightPadding()](#getRightPadding) | يحصل على مقدار المسافة (بالنقاط) لإضافتها إلى يمين محتوى الخلية. |
| [getShading()](#getShading) | يرجع كائن [Shading](../../com.aspose.words/shading/) الذي يشير إلى تنسيق التظليل للخلية. |
| [getTopPadding()](#getTopPadding) | يحصل على مقدار المسافة (بالنقاط) لإضافتها فوق محتوى الخلية. |
| [getVerticalAlignment()](#getVerticalAlignment) | يحصل على المحاذاة العمودية للنص في الخلية. |
| [getVerticalMerge()](#getVerticalMerge) | يحدد كيفية دمج الخلية مع خلايا أخرى عمودياً. |
| [getWidth()](#getWidth) | يحصل على عرض الخلية بالنقاط. |
| [getWrapText()](#getWrapText) | إذا كان true ، قم بلف النص للخلية. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setBottomPadding(double value)](#setBottomPadding-double) | يضبط مقدار المسافة (بالنقاط) لإضافتها أسفل محتوى الخلية. |
| [setFitText(boolean value)](#setFitText-boolean) | إذا كان  true , يضبط النص داخل الخلية، مضغًا كل فقرة إلى عرض الخلية. |
| [setHideMark(boolean value)](#setHideMark-boolean) | يضبط رؤية علامة الخلية. |
| [setHorizontalMerge(int value)](#setHorizontalMerge-int) | يحدد كيفية دمج الخلية أفقياً مع خلايا أخرى في الصف. |
| [setLeftPadding(double value)](#setLeftPadding-double) | يضبط مقدار المسافة (بالنقاط) لإضافتها إلى يسار محتوى الخلية. |
| [setOrientation(int value)](#setOrientation-int) | يضبط اتجاه النص في خلية الجدول. |
| [setPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding)](#setPaddings-double-double-double-double) | يضبط مقدار المسافة (بالنقاط) لإضافتها إلى اليسار/الأعلى/اليمين/الأسفل من محتوى الخلية. |
| [setPreferredWidth(PreferredWidth value)](#setPreferredWidth-com.aspose.words.PreferredWidth) | يضبط العرض المفضل للخلية. |
| [setRightPadding(double value)](#setRightPadding-double) | يضبط مقدار المسافة (بالنقاط) لإضافتها إلى يمين محتوى الخلية. |
| [setTopPadding(double value)](#setTopPadding-double) | يضبط مقدار المسافة (بالنقاط) لإضافتها فوق محتوى الخلية. |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int) | يضبط المحاذاة العمودية للنص في الخلية. |
| [setVerticalMerge(int value)](#setVerticalMerge-int) | يحدد كيفية دمج الخلية مع خلايا أخرى عمودياً. |
| [setWidth(double value)](#setWidth-double) | يحصل على عرض الخلية بالنقاط. |
| [setWrapText(boolean value)](#setWrapText-boolean) | إذا كان true ، قم بلف النص للخلية. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


يعيد الضبط إلى تنسيق الخلية الافتراضي. لا يغيّر عرض الخلية.

 **Examples:** 

يوضح كيفية دمج الصفوف من جدولين في جدول واحد.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // Below are two ways of getting a table from a document.
 // 1 -  From the "Tables" collection of a Body node:
 Table firstTable = doc.getFirstSection().getBody().getTables().get(0);

 // 2 -  Using the "GetChild" method:
 Table secondTable = (Table) doc.getChild(NodeType.TABLE, 1, true);

 // Append all rows from the current table to the next.
 while (secondTable.hasChildNodes())
     firstTable.getRows().add(secondTable.getFirstRow());

 // Remove the empty table container.
 secondTable.remove();

 doc.save(getArtifactsDir() + "Table.CombineTables.docx");
 
```

### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int}
```
public Object fetchInheritedBorderAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int}
```
public Object fetchInheritedShadingAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


يحصل على مجموعة حدود الخلية.

 **Examples:** 

يوضح كيفية دمج الصفوف من جدولين في جدول واحد.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // Below are two ways of getting a table from a document.
 // 1 -  From the "Tables" collection of a Body node:
 Table firstTable = doc.getFirstSection().getBody().getTables().get(0);

 // 2 -  Using the "GetChild" method:
 Table secondTable = (Table) doc.getChild(NodeType.TABLE, 1, true);

 // Append all rows from the current table to the next.
 while (secondTable.hasChildNodes())
     firstTable.getRows().add(secondTable.getFirstRow());

 // Remove the empty table container.
 secondTable.remove();

 doc.save(getArtifactsDir() + "Table.CombineTables.docx");
 
```

**Returns:**
[BorderCollection](../../com.aspose.words/bordercollection/) - Collection of borders of the cell.
### getBottomPadding() {#getBottomPadding}
```
public double getBottomPadding()
```


يحصل على مقدار المسافة (بالنقاط) لإضافتها أسفل محتويات الخلية.

 **Examples:** 

يعرض كيفية تنسيق الخلايا باستخدام منشئ المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Returns:**
double - مقدار المسافة (بالنقاط) لإضافتها أسفل محتوى الخلية.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getFitText() {#getFitText}
```
public boolean getFitText()
```


إذا كان  true , يضبط النص داخل الخلية، مضغًا كل فقرة إلى عرض الخلية.

 **Examples:** 

يوضح كيفية إنشاء جدول بحدود مخصصة.

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
boolean - القيمة المنطقية المقابلة.
### getHideMark() {#getHideMark}
```
public boolean getHideMark()
```


يحصل على رؤية علامة الخلية.

 **Remarks:** 

يحدد أن محتوى خلية الجدول يُعرض بدون ارتفاع إذا كانت جميع الخلايا في الصف فارغة؛ ومع ذلك، تكون للخلية ارتفاع مرئي إذا كان لديها حدود خلايا غير صفرية أو هوامش خلايا أو تباعد خلايا.

**Returns:**
boolean - رؤية علامة الخلية.
### getHorizontalMerge() {#getHorizontalMerge}
```
public int getHorizontalMerge()
```


يحدد كيفية دمج الخلية أفقياً مع خلايا أخرى في الصف.

 **Examples:** 

يعرض كيفية دمج خلايا الجدول أفقياً.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a cell into the first column of the first row.
 // This cell will be the first in a range of horizontally merged cells.
 builder.insertCell();
 builder.getCellFormat().setHorizontalMerge(CellMerge.FIRST);
 builder.write("Text in merged cells.");

 // Insert a cell into the second column of the first row. Instead of adding text contents,
 // we will merge this cell with the first cell that we added directly to the left.
 builder.insertCell();
 builder.getCellFormat().setHorizontalMerge(CellMerge.PREVIOUS);
 builder.endRow();

 // Insert two more unmerged cells to the second row.
 builder.getCellFormat().setHorizontalMerge(CellMerge.NONE);
 builder.insertCell();
 builder.write("Text in unmerged cell.");
 builder.insertCell();
 builder.write("Text in unmerged cell.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "CellFormat.HorizontalMerge.docx");
 
```

يطبع نوع الدمج الأفقي والعمودي للخلية.

```

 public void checkCellsMerged() throws Exception {
     Document doc = new Document(getMyDir() + "Table with merged cells.docx");
     Table table = doc.getFirstSection().getBody().getTables().get(0);

     for (Row row : table.getRows()) {
         for (Cell cell : row.getCells()) {
             System.out.println(printCellMergeType(cell));
         }
     }
 }

 public String printCellMergeType(Cell cell) {
     boolean isHorizontallyMerged = cell.getCellFormat().getHorizontalMerge() != CellMerge.NONE;
     boolean isVerticallyMerged = cell.getCellFormat().getVerticalMerge() != CellMerge.NONE;
     String cellLocation =
             MessageFormat.format("R{0}, C{1}", cell.getParentRow().getParentTable().indexOf(cell.getParentRow()) + 1, cell.getParentRow().indexOf(cell) + 1);

     if (isHorizontallyMerged && isVerticallyMerged)
         return MessageFormat.format("The cell at {0} is both horizontally and vertically merged", cellLocation);
     if (isHorizontallyMerged)
         return MessageFormat.format("The cell at {0} is horizontally merged.", cellLocation);

     return isVerticallyMerged ? MessageFormat.format("The cell at {0} is vertically merged", cellLocation) : MessageFormat.format("The cell at {0} is not merged", cellLocation);
 }
 
```

**Returns:**
int - القيمة int المقابلة. القيمة المرجعة هي واحدة من ثوابت [CellMerge](../../com.aspose.words/cellmerge/).
### getLeftPadding() {#getLeftPadding}
```
public double getLeftPadding()
```


يحصل على مقدار المسافة (بالنقاط) لإضافتها إلى يسار محتوى الخلية.

 **Examples:** 

يعرض كيفية تنسيق الخلايا باستخدام منشئ المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Returns:**
double - مقدار المسافة (بالنقاط) لإضافتها إلى يسار محتوى الخلية.
### getOrientation() {#getOrientation}
```
public int getOrientation()
```


يحصل على اتجاه النص في خلية الجدول.

 **Examples:** 

يوضح كيفية إنشاء جدول بحدود مخصصة.

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

يعرض كيفية إنشاء جدول 2x2 منسق.

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

**Returns:**
int - اتجاه النص في خلية الجدول. القيمة المرجعة هي واحدة من ثوابت [TextOrientation](../../com.aspose.words/textorientation/).
### getPreferredWidth() {#getPreferredWidth}
```
public PreferredWidth getPreferredWidth()
```


يحصل على العرض المفضل للخلية.

 **Remarks:** 

العرض المفضل (إلى جانب خيار الضبط التلقائي للجدول) يحدد كيفية حساب العرض الفعلي للخلية بواسطة خوارزمية تخطيط الجدول. يمكن تنفيذ تخطيط الجدول بواسطة Aspose.Words عند حفظ المستند أو بواسطة Microsoft Word عند عرض المستند.

يمكن تحديد العرض المفضل بالنقاط أو بالنسبة المئوية. يمكن أيضاً تحديد العرض المفضل كـ \"auto\"، مما يعني عدم تحديد عرض مفضل.

القيمة الافتراضية هي [PreferredWidth.AUTO](../../com.aspose.words/preferredwidth/\#AUTO).

 **Examples:** 

يوضح كيفية ضبط عرض مفضل لخلايا الجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

**Returns:**
[PreferredWidth](../../com.aspose.words/preferredwidth/) - The preferred width of the cell.
### getRightPadding() {#getRightPadding}
```
public double getRightPadding()
```


يحصل على مقدار المسافة (بالنقاط) لإضافتها إلى يمين محتوى الخلية.

 **Examples:** 

يعرض كيفية تنسيق الخلايا باستخدام منشئ المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Returns:**
double - مقدار المسافة (بالنقاط) لإضافتها إلى يمين محتوى الخلية.
### getShading() {#getShading}
```
public Shading getShading()
```


يرجع كائن [Shading](../../com.aspose.words/shading/) الذي يشير إلى تنسيق التظليل للخلية.

 **Examples:** 

يوضح كيفية إنشاء جدول بحدود مخصصة.

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

يوضح كيفية تعديل تنسيق الصفوف والخلايا في جدول.

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

**Returns:**
[Shading](../../com.aspose.words/shading/) - A [Shading](../../com.aspose.words/shading/) object that refers to the shading formatting for the cell.
### getTopPadding() {#getTopPadding}
```
public double getTopPadding()
```


يحصل على مقدار المسافة (بالنقاط) لإضافتها فوق محتوى الخلية.

 **Examples:** 

يعرض كيفية تنسيق الخلايا باستخدام منشئ المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Returns:**
double - مقدار المسافة (بالنقاط) لإضافتها فوق محتوى الخلية.
### getVerticalAlignment() {#getVerticalAlignment}
```
public int getVerticalAlignment()
```


يحصل على المحاذاة العمودية للنص في الخلية.

 **Examples:** 

يوضح كيفية إنشاء جدول بحدود مخصصة.

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
int - المحاذاة العمودية للنص في الخلية. القيمة المرجعة هي واحدة من ثوابت [CellVerticalAlignment](../../com.aspose.words/cellverticalalignment/).
### getVerticalMerge() {#getVerticalMerge}
```
public int getVerticalMerge()
```


يحدد كيفية دمج الخلية مع خلايا أخرى عمودياً.

 **Remarks:** 

يمكن دمج الخلايا عمودياً فقط إذا كانت حدودها اليسرى واليمنى متطابقة.

عند دمج الخلايا عمودياً، يتم دمج مناطق العرض للخلايا المدمجة. تُستخدم المنطقة المدمجة لعرض محتوى الخلية المدمجة الأولى ويجب أن تكون جميع الخلايا المدمجة عمودياً الأخرى فارغة.

 **Examples:** 

يعرض كيفية دمج خلايا الجدول عموديًا.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a cell into the first column of the first row.
 // This cell will be the first in a range of vertically merged cells.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.FIRST);
 builder.write("Text in merged cells.");

 // Insert a cell into the second column of the first row, then end the row.
 // Also, configure the builder to disable vertical merging in created cells.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.NONE);
 builder.write("Text in unmerged cell.");
 builder.endRow();

 // Insert a cell into the first column of the second row.
 // Instead of adding text contents, we will merge this cell with the first cell that we added directly above.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.PREVIOUS);

 // Insert another independent cell in the second column of the second row.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.NONE);
 builder.write("Text in unmerged cell.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "CellFormat.VerticalMerge.docx");
 
```

يطبع نوع الدمج الأفقي والعمودي للخلية.

```

 public void checkCellsMerged() throws Exception {
     Document doc = new Document(getMyDir() + "Table with merged cells.docx");
     Table table = doc.getFirstSection().getBody().getTables().get(0);

     for (Row row : table.getRows()) {
         for (Cell cell : row.getCells()) {
             System.out.println(printCellMergeType(cell));
         }
     }
 }

 public String printCellMergeType(Cell cell) {
     boolean isHorizontallyMerged = cell.getCellFormat().getHorizontalMerge() != CellMerge.NONE;
     boolean isVerticallyMerged = cell.getCellFormat().getVerticalMerge() != CellMerge.NONE;
     String cellLocation =
             MessageFormat.format("R{0}, C{1}", cell.getParentRow().getParentTable().indexOf(cell.getParentRow()) + 1, cell.getParentRow().indexOf(cell) + 1);

     if (isHorizontallyMerged && isVerticallyMerged)
         return MessageFormat.format("The cell at {0} is both horizontally and vertically merged", cellLocation);
     if (isHorizontallyMerged)
         return MessageFormat.format("The cell at {0} is horizontally merged.", cellLocation);

     return isVerticallyMerged ? MessageFormat.format("The cell at {0} is vertically merged", cellLocation) : MessageFormat.format("The cell at {0} is not merged", cellLocation);
 }
 
```

**Returns:**
int - القيمة int المقابلة. القيمة المرجعة هي واحدة من ثوابت [CellMerge](../../com.aspose.words/cellmerge/).
### getWidth() {#getWidth}
```
public double getWidth()
```


يحصل على عرض الخلية بالنقاط.

 **Remarks:** 

يتم حساب العرض بواسطة Aspose.Words عند تحميل المستند وحفظه. حالياً، لا يتم دعم كل تركيبة من خصائص الجدول والخلية والمستند. قد لا تكون القيمة المرجعة دقيقة لبعض المستندات. قد لا تتطابق تماماً مع عرض الخلية كما يحسبه MS Word عند فتح المستند في MS Word.

لا يُنصح بتعيين هذه الخاصية. لا يوجد ضمان بأن الخلية ستحصل فعلياً على العرض المحدد. قد يتم تعديل العرض لاستيعاب محتوى الخلية في تخطيط جدول تلقائي الضبط. قد تكون خلايا الصفوف الأخرى لديها إعدادات عرض متضاربة. قد يتم تغيير حجم الجدول ليتناسب مع الحاوية أو لتلبية إعدادات عرض الجدول. فكر في استخدام [getPreferredWidth()](../../com.aspose.words/cellformat/\#getPreferredWidth) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat/\#setPreferredWidth-com.aspose.words.PreferredWidth) لتعيين عرض الخلية. تعيين هذه الخاصية يضبط [getPreferredWidth()](../../com.aspose.words/cellformat/\#getPreferredWidth) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat/\#setPreferredWidth-com.aspose.words.PreferredWidth) ضمنياً منذ الإصدار 15.8.

 **Examples:** 

يوضح كيفية إنشاء جدول بحدود مخصصة.

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

يعرض كيفية تنسيق الخلايا باستخدام منشئ المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Returns:**
double - عرض الخلية بالنقاط.
### getWrapText() {#getWrapText}
```
public boolean getWrapText()
```


إذا كان true ، قم بلف النص للخلية.

 **Examples:** 

يوضح كيفية إنشاء جدول بحدود مخصصة.

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
boolean - القيمة المنطقية المقابلة.
### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |
| قيمة | java.lang.Object |  |

### setBottomPadding(double value) {#setBottomPadding-double}
```
public void setBottomPadding(double value)
```


يضبط مقدار المسافة (بالنقاط) لإضافتها أسفل محتوى الخلية.

 **Examples:** 

يعرض كيفية تنسيق الخلايا باستخدام منشئ المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | مقدار المسافة (بالنقاط) لإضافتها أسفل محتوى الخلية. |

### setFitText(boolean value) {#setFitText-boolean}
```
public void setFitText(boolean value)
```


إذا كان  true , يضبط النص داخل الخلية، مضغًا كل فقرة إلى عرض الخلية.

 **Examples:** 

يوضح كيفية إنشاء جدول بحدود مخصصة.

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setHideMark(boolean value) {#setHideMark-boolean}
```
public void setHideMark(boolean value)
```


يضبط رؤية علامة الخلية.

 **Remarks:** 

يحدد أن محتوى خلية الجدول يُعرض بدون ارتفاع إذا كانت جميع الخلايا في الصف فارغة؛ ومع ذلك، تكون للخلية ارتفاع مرئي إذا كان لديها حدود خلايا غير صفرية أو هوامش خلايا أو تباعد خلايا.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | إظهار علامة الخلية. |

### setHorizontalMerge(int value) {#setHorizontalMerge-int}
```
public void setHorizontalMerge(int value)
```


يحدد كيفية دمج الخلية أفقياً مع خلايا أخرى في الصف.

 **Examples:** 

يعرض كيفية دمج خلايا الجدول أفقياً.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a cell into the first column of the first row.
 // This cell will be the first in a range of horizontally merged cells.
 builder.insertCell();
 builder.getCellFormat().setHorizontalMerge(CellMerge.FIRST);
 builder.write("Text in merged cells.");

 // Insert a cell into the second column of the first row. Instead of adding text contents,
 // we will merge this cell with the first cell that we added directly to the left.
 builder.insertCell();
 builder.getCellFormat().setHorizontalMerge(CellMerge.PREVIOUS);
 builder.endRow();

 // Insert two more unmerged cells to the second row.
 builder.getCellFormat().setHorizontalMerge(CellMerge.NONE);
 builder.insertCell();
 builder.write("Text in unmerged cell.");
 builder.insertCell();
 builder.write("Text in unmerged cell.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "CellFormat.HorizontalMerge.docx");
 
```

يطبع نوع الدمج الأفقي والعمودي للخلية.

```

 public void checkCellsMerged() throws Exception {
     Document doc = new Document(getMyDir() + "Table with merged cells.docx");
     Table table = doc.getFirstSection().getBody().getTables().get(0);

     for (Row row : table.getRows()) {
         for (Cell cell : row.getCells()) {
             System.out.println(printCellMergeType(cell));
         }
     }
 }

 public String printCellMergeType(Cell cell) {
     boolean isHorizontallyMerged = cell.getCellFormat().getHorizontalMerge() != CellMerge.NONE;
     boolean isVerticallyMerged = cell.getCellFormat().getVerticalMerge() != CellMerge.NONE;
     String cellLocation =
             MessageFormat.format("R{0}, C{1}", cell.getParentRow().getParentTable().indexOf(cell.getParentRow()) + 1, cell.getParentRow().indexOf(cell) + 1);

     if (isHorizontallyMerged && isVerticallyMerged)
         return MessageFormat.format("The cell at {0} is both horizontally and vertically merged", cellLocation);
     if (isHorizontallyMerged)
         return MessageFormat.format("The cell at {0} is horizontally merged.", cellLocation);

     return isVerticallyMerged ? MessageFormat.format("The cell at {0} is vertically merged", cellLocation) : MessageFormat.format("The cell at {0} is not merged", cellLocation);
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة int المقابلة. يجب أن تكون القيمة واحدة من ثوابت [CellMerge](../../com.aspose.words/cellmerge/). |

### setLeftPadding(double value) {#setLeftPadding-double}
```
public void setLeftPadding(double value)
```


يضبط مقدار المسافة (بالنقاط) لإضافتها إلى يسار محتوى الخلية.

 **Examples:** 

يعرض كيفية تنسيق الخلايا باستخدام منشئ المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | مقدار المسافة (بالنقاط) لإضافتها إلى يسار محتوى الخلية. |

### setOrientation(int value) {#setOrientation-int}
```
public void setOrientation(int value)
```


يضبط اتجاه النص في خلية الجدول.

 **Examples:** 

يوضح كيفية إنشاء جدول بحدود مخصصة.

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

يعرض كيفية إنشاء جدول 2x2 منسق.

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | اتجاه النص في خلية الجدول. يجب أن تكون القيمة واحدة من ثوابت [TextOrientation](../../com.aspose.words/textorientation/). |

### setPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding) {#setPaddings-double-double-double-double}
```
public void setPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding)
```


يضبط مقدار المسافة (بالنقاط) لإضافتها إلى اليسار/الأعلى/اليمين/الأسفل من محتوى الخلية.

 **Examples:** 

يعرض كيفية إضافة مسافات إلى محتوى الخلية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set a padding distance (in points) between the border and the text contents
 // of each table cell we create with the document builder.
 builder.getCellFormat().setPaddings(5.0, 10.0, 40.0, 50.0);

 // Create a table with one cell whose contents will have whitespace padding.
 builder.startTable();
 builder.insertCell();
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
         "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 doc.save(getArtifactsDir() + "CellFormat.Padding.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| leftPadding | double |  |
| topPadding | double |  |
| rightPadding | double |  |
| bottomPadding | double |  |

### setPreferredWidth(PreferredWidth value) {#setPreferredWidth-com.aspose.words.PreferredWidth}
```
public void setPreferredWidth(PreferredWidth value)
```


يضبط العرض المفضل للخلية.

 **Remarks:** 

العرض المفضل (إلى جانب خيار الضبط التلقائي للجدول) يحدد كيفية حساب العرض الفعلي للخلية بواسطة خوارزمية تخطيط الجدول. يمكن تنفيذ تخطيط الجدول بواسطة Aspose.Words عند حفظ المستند أو بواسطة Microsoft Word عند عرض المستند.

يمكن تحديد العرض المفضل بالنقاط أو بالنسبة المئوية. يمكن أيضاً تحديد العرض المفضل كـ \"auto\"، مما يعني عدم تحديد عرض مفضل.

القيمة الافتراضية هي [PreferredWidth.AUTO](../../com.aspose.words/preferredwidth/\#AUTO).

 **Examples:** 

يوضح كيفية ضبط عرض مفضل لخلايا الجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [PreferredWidth](../../com.aspose.words/preferredwidth/) | العرض المفضل للخلية. |

### setRightPadding(double value) {#setRightPadding-double}
```
public void setRightPadding(double value)
```


يضبط مقدار المسافة (بالنقاط) لإضافتها إلى يمين محتوى الخلية.

 **Examples:** 

يعرض كيفية تنسيق الخلايا باستخدام منشئ المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | كمية المسافة (بالنقاط) لإضافتها إلى يمين محتويات الخلية. |

### setTopPadding(double value) {#setTopPadding-double}
```
public void setTopPadding(double value)
```


يضبط مقدار المسافة (بالنقاط) لإضافتها فوق محتوى الخلية.

 **Examples:** 

يعرض كيفية تنسيق الخلايا باستخدام منشئ المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | كمية المسافة (بالنقاط) لإضافتها فوق محتويات الخلية. |

### setVerticalAlignment(int value) {#setVerticalAlignment-int}
```
public void setVerticalAlignment(int value)
```


يضبط المحاذاة العمودية للنص في الخلية.

 **Examples:** 

يوضح كيفية إنشاء جدول بحدود مخصصة.

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | المحاذاة العمودية للنص في الخلية. يجب أن تكون القيمة واحدة من ثوابت [CellVerticalAlignment](../../com.aspose.words/cellverticalalignment/). |

### setVerticalMerge(int value) {#setVerticalMerge-int}
```
public void setVerticalMerge(int value)
```


يحدد كيفية دمج الخلية مع خلايا أخرى عمودياً.

 **Remarks:** 

يمكن دمج الخلايا عمودياً فقط إذا كانت حدودها اليسرى واليمنى متطابقة.

عند دمج الخلايا عمودياً، يتم دمج مناطق العرض للخلايا المدمجة. تُستخدم المنطقة المدمجة لعرض محتوى الخلية المدمجة الأولى ويجب أن تكون جميع الخلايا المدمجة عمودياً الأخرى فارغة.

 **Examples:** 

يعرض كيفية دمج خلايا الجدول عموديًا.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a cell into the first column of the first row.
 // This cell will be the first in a range of vertically merged cells.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.FIRST);
 builder.write("Text in merged cells.");

 // Insert a cell into the second column of the first row, then end the row.
 // Also, configure the builder to disable vertical merging in created cells.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.NONE);
 builder.write("Text in unmerged cell.");
 builder.endRow();

 // Insert a cell into the first column of the second row.
 // Instead of adding text contents, we will merge this cell with the first cell that we added directly above.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.PREVIOUS);

 // Insert another independent cell in the second column of the second row.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.NONE);
 builder.write("Text in unmerged cell.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "CellFormat.VerticalMerge.docx");
 
```

يطبع نوع الدمج الأفقي والعمودي للخلية.

```

 public void checkCellsMerged() throws Exception {
     Document doc = new Document(getMyDir() + "Table with merged cells.docx");
     Table table = doc.getFirstSection().getBody().getTables().get(0);

     for (Row row : table.getRows()) {
         for (Cell cell : row.getCells()) {
             System.out.println(printCellMergeType(cell));
         }
     }
 }

 public String printCellMergeType(Cell cell) {
     boolean isHorizontallyMerged = cell.getCellFormat().getHorizontalMerge() != CellMerge.NONE;
     boolean isVerticallyMerged = cell.getCellFormat().getVerticalMerge() != CellMerge.NONE;
     String cellLocation =
             MessageFormat.format("R{0}, C{1}", cell.getParentRow().getParentTable().indexOf(cell.getParentRow()) + 1, cell.getParentRow().indexOf(cell) + 1);

     if (isHorizontallyMerged && isVerticallyMerged)
         return MessageFormat.format("The cell at {0} is both horizontally and vertically merged", cellLocation);
     if (isHorizontallyMerged)
         return MessageFormat.format("The cell at {0} is horizontally merged.", cellLocation);

     return isVerticallyMerged ? MessageFormat.format("The cell at {0} is vertically merged", cellLocation) : MessageFormat.format("The cell at {0} is not merged", cellLocation);
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة int المقابلة. يجب أن تكون القيمة واحدة من ثوابت [CellMerge](../../com.aspose.words/cellmerge/). |

### setWidth(double value) {#setWidth-double}
```
public void setWidth(double value)
```


يحصل على عرض الخلية بالنقاط.

 **Remarks:** 

يتم حساب العرض بواسطة Aspose.Words عند تحميل المستند وحفظه. حالياً، لا يتم دعم كل تركيبة من خصائص الجدول والخلية والمستند. قد لا تكون القيمة المرجعة دقيقة لبعض المستندات. قد لا تتطابق تماماً مع عرض الخلية كما يحسبه MS Word عند فتح المستند في MS Word.

لا يُنصح بتعيين هذه الخاصية. لا يوجد ضمان بأن الخلية ستحصل فعلياً على العرض المحدد. قد يتم تعديل العرض لاستيعاب محتوى الخلية في تخطيط جدول تلقائي الضبط. قد تكون خلايا الصفوف الأخرى لديها إعدادات عرض متضاربة. قد يتم تغيير حجم الجدول ليتناسب مع الحاوية أو لتلبية إعدادات عرض الجدول. فكر في استخدام [getPreferredWidth()](../../com.aspose.words/cellformat/\#getPreferredWidth) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat/\#setPreferredWidth-com.aspose.words.PreferredWidth) لتعيين عرض الخلية. تعيين هذه الخاصية يضبط [getPreferredWidth()](../../com.aspose.words/cellformat/\#getPreferredWidth) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat/\#setPreferredWidth-com.aspose.words.PreferredWidth) ضمنياً منذ الإصدار 15.8.

 **Examples:** 

يوضح كيفية إنشاء جدول بحدود مخصصة.

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

يعرض كيفية تنسيق الخلايا باستخدام منشئ المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | عرض الخلية بالنقاط. |

### setWrapText(boolean value) {#setWrapText-boolean}
```
public void setWrapText(boolean value)
```


إذا كان true ، قم بلف النص للخلية.

 **Examples:** 

يوضح كيفية إنشاء جدول بحدود مخصصة.

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

