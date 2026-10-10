---
title: "ConditionalStyleType"
linktitle: "ConditionalStyleType"
second_title: "Aspose.Words für Java"
description: "Stellt mögliche Tabellenbereiche dar, für die bedingte Formatierung in einem Tabellenstil in Java definiert werden kann."
type: docs
weight: 125
url: /de/java/com.aspose.words/conditionalstyletype/
---

**Inheritance:**
java.lang.Object
```
public class ConditionalStyleType
```

Stellt mögliche Tabellenbereiche dar, für die bedingte Formatierung in einem Tabellenstil definiert werden kann.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [BOTTOM_LEFT_CELL](#BOTTOM-LEFT-CELL) | Gibt die Formatierung der unteren linken Zelle einer Tabelle an. |
| [BOTTOM_RIGHT_CELL](#BOTTOM-RIGHT-CELL) | Gibt die Formatierung der unteren rechten Zelle einer Tabelle an. |
| [EVEN_COLUMN_BANDING](#EVEN-COLUMN-BANDING) | Gibt die Formatierung des geraden Spaltenstreifens an. |
| [EVEN_ROW_BANDING](#EVEN-ROW-BANDING) | Gibt die Formatierung des geraden Zeilenstreifens an. |
| [FIRST_COLUMN](#FIRST-COLUMN) | Gibt die Formatierung der ersten Spalte einer Tabelle an. |
| [FIRST_ROW](#FIRST-ROW) | Gibt die Formatierung der ersten Zeile einer Tabelle an. |
| [LAST_COLUMN](#LAST-COLUMN) | Gibt die Formatierung der letzten Spalte einer Tabelle an. |
| [LAST_ROW](#LAST-ROW) | Gibt die Formatierung der letzten Zeile einer Tabelle an. |
| [ODD_COLUMN_BANDING](#ODD-COLUMN-BANDING) | Gibt die Formatierung des ungeraden Spaltenstreifens an. |
| [ODD_ROW_BANDING](#ODD-ROW-BANDING) | Gibt die Formatierung des ungeraden Zeilenstreifens an. |
| [TOP_LEFT_CELL](#TOP-LEFT-CELL) | Gibt die Formatierung der oberen linken Zelle einer Tabelle an. |
| [TOP_RIGHT_CELL](#TOP-RIGHT-CELL) | Gibt die Formatierung der oberen rechten Zelle einer Tabelle an. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String conditionalStyleTypeName)](#fromName-java.lang.String) |  |
| [getName(int conditionalStyleType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int conditionalStyleType)](#toString-int) |  |
### BOTTOM_LEFT_CELL {#BOTTOM-LEFT-CELL}
```
public static int BOTTOM_LEFT_CELL
```


Gibt die Formatierung der unteren linken Zelle einer Tabelle an.

### BOTTOM_RIGHT_CELL {#BOTTOM-RIGHT-CELL}
```
public static int BOTTOM_RIGHT_CELL
```


Gibt die Formatierung der unteren rechten Zelle einer Tabelle an.

### EVEN_COLUMN_BANDING {#EVEN-COLUMN-BANDING}
```
public static int EVEN_COLUMN_BANDING
```


Gibt die Formatierung des geraden Spaltenstreifens an.

### EVEN_ROW_BANDING {#EVEN-ROW-BANDING}
```
public static int EVEN_ROW_BANDING
```


Gibt die Formatierung des geraden Zeilenstreifens an.

### FIRST_COLUMN {#FIRST-COLUMN}
```
public static int FIRST_COLUMN
```


Gibt die Formatierung der ersten Spalte einer Tabelle an.

### FIRST_ROW {#FIRST-ROW}
```
public static int FIRST_ROW
```


Gibt die Formatierung der ersten Zeile einer Tabelle an.

### LAST_COLUMN {#LAST-COLUMN}
```
public static int LAST_COLUMN
```


Gibt die Formatierung der letzten Spalte einer Tabelle an.

### LAST_ROW {#LAST-ROW}
```
public static int LAST_ROW
```


Gibt die Formatierung der letzten Zeile einer Tabelle an.

### ODD_COLUMN_BANDING {#ODD-COLUMN-BANDING}
```
public static int ODD_COLUMN_BANDING
```


Gibt die Formatierung des ungeraden Spaltenstreifens an.

### ODD_ROW_BANDING {#ODD-ROW-BANDING}
```
public static int ODD_ROW_BANDING
```


Gibt die Formatierung des ungeraden Zeilenstreifens an.

### TOP_LEFT_CELL {#TOP-LEFT-CELL}
```
public static int TOP_LEFT_CELL
```


Gibt die Formatierung der oberen linken Zelle einer Tabelle an.

### TOP_RIGHT_CELL {#TOP-RIGHT-CELL}
```
public static int TOP_RIGHT_CELL
```


Gibt die Formatierung der oberen rechten Zelle einer Tabelle an.

### length {#length}
```
public static int length
```


### fromName(String conditionalStyleTypeName) {#fromName-java.lang.String}
```
public static int fromName(String conditionalStyleTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| conditionalStyleTypeName | java.lang.String |  |

**Returns:**
int
### getName(int conditionalStyleType) {#getName-int}
```
public static String getName(int conditionalStyleType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| conditionalStyleType | int |  |

**Returns:**
java.lang.String
