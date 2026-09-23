---
title: "ConditionalStyleType"
linktitle: "ConditionalStyleType"
second_title: "Aspose.Words для Java"
description: "Представляет возможные области таблицы, к которым может быть применено условное форматирование в стиле таблицы в Java."
type: docs
weight: 125
url: /ru/java/com.aspose.words/conditionalstyletype/
---

**Inheritance:**
java.lang.Object
```
public class ConditionalStyleType
```

Представляет возможные области таблицы, к которым может быть определено условное форматирование в стиле таблицы.

 **Examples:** 

Показывает, как работать с определёнными стилями областей таблицы.

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
## Поля

| Поле | Описание |
| --- | --- |
| [BOTTOM_LEFT_CELL](#BOTTOM-LEFT-CELL) | Указывает форматирование ячейки в нижнем левом углу таблицы. |
| [BOTTOM_RIGHT_CELL](#BOTTOM-RIGHT-CELL) | Указывает форматирование ячейки в нижнем правом углу таблицы. |
| [EVEN_COLUMN_BANDING](#EVEN-COLUMN-BANDING) | Указывает форматирование полосы чётных колонок. |
| [EVEN_ROW_BANDING](#EVEN-ROW-BANDING) | Указывает форматирование полосы чётных строк. |
| [FIRST_COLUMN](#FIRST-COLUMN) | Указывает форматирование первого столбца таблицы. |
| [FIRST_ROW](#FIRST-ROW) | Указывает форматирование первой строки таблицы. |
| [LAST_COLUMN](#LAST-COLUMN) | Указывает форматирование последнего столбца таблицы. |
| [LAST_ROW](#LAST-ROW) | Указывает форматирование последней строки таблицы. |
| [ODD_COLUMN_BANDING](#ODD-COLUMN-BANDING) | Указывает форматирование полосы нечетных столбцов. |
| [ODD_ROW_BANDING](#ODD-ROW-BANDING) | Указывает форматирование полосы нечетных строк. |
| [TOP_LEFT_CELL](#TOP-LEFT-CELL) | Указывает форматирование верхней левой ячейки таблицы. |
| [TOP_RIGHT_CELL](#TOP-RIGHT-CELL) | Указывает форматирование верхней правой ячейки таблицы. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String conditionalStyleTypeName)](#fromName-java.lang.String) |  |
| [getName(int conditionalStyleType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int conditionalStyleType)](#toString-int) |  |
### BOTTOM_LEFT_CELL {#BOTTOM-LEFT-CELL}
```
public static int BOTTOM_LEFT_CELL
```


Указывает форматирование ячейки в нижнем левом углу таблицы.

### BOTTOM_RIGHT_CELL {#BOTTOM-RIGHT-CELL}
```
public static int BOTTOM_RIGHT_CELL
```


Указывает форматирование ячейки в нижнем правом углу таблицы.

### EVEN_COLUMN_BANDING {#EVEN-COLUMN-BANDING}
```
public static int EVEN_COLUMN_BANDING
```


Указывает форматирование полосы чётных колонок.

### EVEN_ROW_BANDING {#EVEN-ROW-BANDING}
```
public static int EVEN_ROW_BANDING
```


Указывает форматирование полосы чётных строк.

### FIRST_COLUMN {#FIRST-COLUMN}
```
public static int FIRST_COLUMN
```


Указывает форматирование первого столбца таблицы.

### FIRST_ROW {#FIRST-ROW}
```
public static int FIRST_ROW
```


Указывает форматирование первой строки таблицы.

### LAST_COLUMN {#LAST-COLUMN}
```
public static int LAST_COLUMN
```


Указывает форматирование последнего столбца таблицы.

### LAST_ROW {#LAST-ROW}
```
public static int LAST_ROW
```


Указывает форматирование последней строки таблицы.

### ODD_COLUMN_BANDING {#ODD-COLUMN-BANDING}
```
public static int ODD_COLUMN_BANDING
```


Указывает форматирование полосы нечетных столбцов.

### ODD_ROW_BANDING {#ODD-ROW-BANDING}
```
public static int ODD_ROW_BANDING
```


Указывает форматирование полосы нечетных строк.

### TOP_LEFT_CELL {#TOP-LEFT-CELL}
```
public static int TOP_LEFT_CELL
```


Указывает форматирование верхней левой ячейки таблицы.

### TOP_RIGHT_CELL {#TOP-RIGHT-CELL}
```
public static int TOP_RIGHT_CELL
```


Указывает форматирование верхней правой ячейки таблицы.

### length {#length}
```
public static int length
```


### fromName(String conditionalStyleTypeName) {#fromName-java.lang.String}
```
public static int fromName(String conditionalStyleTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| conditionalStyleTypeName | java.lang.String |  |

**Returns:**
int
### getName(int conditionalStyleType) {#getName-int}
```
public static String getName(int conditionalStyleType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| conditionalStyleType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int conditionalStyleType) {#toString-int}
```
public static String toString(int conditionalStyleType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| conditionalStyleType | int |  |

**Returns:**
java.lang.String
