---
title: "ConditionalStyleType"
linktitle: "ConditionalStyleType"
second_title: "Aspose.Words per Java"
description: "Rappresenta le possibili aree della tabella a cui può essere definita la formattazione condizionale in uno stile di tabella in Java."
type: docs
weight: 125
url: /it/java/com.aspose.words/conditionalstyletype/
---

**Inheritance:**
java.lang.Object
```
public class ConditionalStyleType
```

Rappresenta le possibili aree della tabella a cui può essere definita la formattazione condizionale in uno stile di tabella.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [BOTTOM_LEFT_CELL](#BOTTOM-LEFT-CELL) | Specifica la formattazione della cella in basso a sinistra di una tabella. |
| [BOTTOM_RIGHT_CELL](#BOTTOM-RIGHT-CELL) | Specifica la formattazione della cella in basso a destra di una tabella. |
| [EVEN_COLUMN_BANDING](#EVEN-COLUMN-BANDING) | Specifica la formattazione della striscia di colonna pari. |
| [EVEN_ROW_BANDING](#EVEN-ROW-BANDING) | Specifica la formattazione della striscia di riga pari. |
| [FIRST_COLUMN](#FIRST-COLUMN) | Specifica la formattazione della prima colonna di una tabella. |
| [FIRST_ROW](#FIRST-ROW) | Specifica la formattazione della prima riga di una tabella. |
| [LAST_COLUMN](#LAST-COLUMN) | Specifica la formattazione dell'ultima colonna di una tabella. |
| [LAST_ROW](#LAST-ROW) | Specifica la formattazione dell'ultima riga di una tabella. |
| [ODD_COLUMN_BANDING](#ODD-COLUMN-BANDING) | Specifica la formattazione della striscia delle colonne dispari. |
| [ODD_ROW_BANDING](#ODD-ROW-BANDING) | Specifica la formattazione della striscia delle righe dispari. |
| [TOP_LEFT_CELL](#TOP-LEFT-CELL) | Specifica la formattazione della cella in alto a sinistra di una tabella. |
| [TOP_RIGHT_CELL](#TOP-RIGHT-CELL) | Specifica la formattazione della cella in alto a destra di una tabella. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String conditionalStyleTypeName)](#fromName-java.lang.String) |  |
| [getName(int conditionalStyleType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int conditionalStyleType)](#toString-int) |  |
### BOTTOM_LEFT_CELL {#BOTTOM-LEFT-CELL}
```
public static int BOTTOM_LEFT_CELL
```


Specifica la formattazione della cella in basso a sinistra di una tabella.

### BOTTOM_RIGHT_CELL {#BOTTOM-RIGHT-CELL}
```
public static int BOTTOM_RIGHT_CELL
```


Specifica la formattazione della cella in basso a destra di una tabella.

### EVEN_COLUMN_BANDING {#EVEN-COLUMN-BANDING}
```
public static int EVEN_COLUMN_BANDING
```


Specifica la formattazione della striscia di colonna pari.

### EVEN_ROW_BANDING {#EVEN-ROW-BANDING}
```
public static int EVEN_ROW_BANDING
```


Specifica la formattazione della striscia di riga pari.

### FIRST_COLUMN {#FIRST-COLUMN}
```
public static int FIRST_COLUMN
```


Specifica la formattazione della prima colonna di una tabella.

### FIRST_ROW {#FIRST-ROW}
```
public static int FIRST_ROW
```


Specifica la formattazione della prima riga di una tabella.

### LAST_COLUMN {#LAST-COLUMN}
```
public static int LAST_COLUMN
```


Specifica la formattazione dell'ultima colonna di una tabella.

### LAST_ROW {#LAST-ROW}
```
public static int LAST_ROW
```


Specifica la formattazione dell'ultima riga di una tabella.

### ODD_COLUMN_BANDING {#ODD-COLUMN-BANDING}
```
public static int ODD_COLUMN_BANDING
```


Specifica la formattazione della striscia delle colonne dispari.

### ODD_ROW_BANDING {#ODD-ROW-BANDING}
```
public static int ODD_ROW_BANDING
```


Specifica la formattazione della striscia delle righe dispari.

### TOP_LEFT_CELL {#TOP-LEFT-CELL}
```
public static int TOP_LEFT_CELL
```


Specifica la formattazione della cella in alto a sinistra di una tabella.

### TOP_RIGHT_CELL {#TOP-RIGHT-CELL}
```
public static int TOP_RIGHT_CELL
```


Specifica la formattazione della cella in alto a destra di una tabella.

### length {#length}
```
public static int length
```


### fromName(String conditionalStyleTypeName) {#fromName-java.lang.String}
```
public static int fromName(String conditionalStyleTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| conditionalStyleTypeName | java.lang.String |  |

**Returns:**
int
### getName(int conditionalStyleType) {#getName-int}
```
public static String getName(int conditionalStyleType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| conditionalStyleType | int |  |

**Returns:**
java.lang.String
