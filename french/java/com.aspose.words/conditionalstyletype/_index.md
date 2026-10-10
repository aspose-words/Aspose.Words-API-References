---
title: "ConditionalStyleType"
linktitle: "ConditionalStyleType"
second_title: "Aspose.Words pour Java"
description: "Représente les zones de tableau possibles auxquelles un formatage conditionnel peut être défini dans un style de tableau en Java."
type: docs
weight: 125
url: /fr/java/com.aspose.words/conditionalstyletype/
---

**Inheritance:**
java.lang.Object
```
public class ConditionalStyleType
```

Représente les zones de tableau possibles auxquelles un formatage conditionnel peut être défini dans un style de tableau.

 **Examples:** 

Montre comment travailler avec certains styles de zone d'un tableau.

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
## Champs

| Champ | Description |
| --- | --- |
| [BOTTOM_LEFT_CELL](#BOTTOM-LEFT-CELL) | Spécifie le format de la cellule inférieure gauche d'un tableau. |
| [BOTTOM_RIGHT_CELL](#BOTTOM-RIGHT-CELL) | Spécifie le format de la cellule inférieure droite d'un tableau. |
| [EVEN_COLUMN_BANDING](#EVEN-COLUMN-BANDING) | Spécifie le format de la bande de colonne paire. |
| [EVEN_ROW_BANDING](#EVEN-ROW-BANDING) | Spécifie le format de la bande de ligne paire. |
| [FIRST_COLUMN](#FIRST-COLUMN) | Spécifie le formatage de la première colonne d'un tableau. |
| [FIRST_ROW](#FIRST-ROW) | Spécifie le formatage de la première ligne d'un tableau. |
| [LAST_COLUMN](#LAST-COLUMN) | Spécifie le formatage de la dernière colonne d'un tableau. |
| [LAST_ROW](#LAST-ROW) | Spécifie le formatage de la dernière ligne d'un tableau. |
| [ODD_COLUMN_BANDING](#ODD-COLUMN-BANDING) | Spécifie le formatage de la bande de colonnes impaires. |
| [ODD_ROW_BANDING](#ODD-ROW-BANDING) | Spécifie le formatage de la bande de lignes impaires. |
| [TOP_LEFT_CELL](#TOP-LEFT-CELL) | Spécifie le formatage de la cellule supérieure gauche d'un tableau. |
| [TOP_RIGHT_CELL](#TOP-RIGHT-CELL) | Spécifie le formatage de la cellule supérieure droite d'un tableau. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String conditionalStyleTypeName)](#fromName-java.lang.String) |  |
| [getName(int conditionalStyleType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int conditionalStyleType)](#toString-int) |  |
### BOTTOM_LEFT_CELL {#BOTTOM-LEFT-CELL}
```
public static int BOTTOM_LEFT_CELL
```


Spécifie le format de la cellule inférieure gauche d'un tableau.

### BOTTOM_RIGHT_CELL {#BOTTOM-RIGHT-CELL}
```
public static int BOTTOM_RIGHT_CELL
```


Spécifie le format de la cellule inférieure droite d'un tableau.

### EVEN_COLUMN_BANDING {#EVEN-COLUMN-BANDING}
```
public static int EVEN_COLUMN_BANDING
```


Spécifie le format de la bande de colonne paire.

### EVEN_ROW_BANDING {#EVEN-ROW-BANDING}
```
public static int EVEN_ROW_BANDING
```


Spécifie le format de la bande de ligne paire.

### FIRST_COLUMN {#FIRST-COLUMN}
```
public static int FIRST_COLUMN
```


Spécifie le formatage de la première colonne d'un tableau.

### FIRST_ROW {#FIRST-ROW}
```
public static int FIRST_ROW
```


Spécifie le formatage de la première ligne d'un tableau.

### LAST_COLUMN {#LAST-COLUMN}
```
public static int LAST_COLUMN
```


Spécifie le formatage de la dernière colonne d'un tableau.

### LAST_ROW {#LAST-ROW}
```
public static int LAST_ROW
```


Spécifie le formatage de la dernière ligne d'un tableau.

### ODD_COLUMN_BANDING {#ODD-COLUMN-BANDING}
```
public static int ODD_COLUMN_BANDING
```


Spécifie le formatage de la bande de colonnes impaires.

### ODD_ROW_BANDING {#ODD-ROW-BANDING}
```
public static int ODD_ROW_BANDING
```


Spécifie le formatage de la bande de lignes impaires.

### TOP_LEFT_CELL {#TOP-LEFT-CELL}
```
public static int TOP_LEFT_CELL
```


Spécifie le formatage de la cellule supérieure gauche d'un tableau.

### TOP_RIGHT_CELL {#TOP-RIGHT-CELL}
```
public static int TOP_RIGHT_CELL
```


Spécifie le formatage de la cellule supérieure droite d'un tableau.

### length {#length}
```
public static int length
```


### fromName(String conditionalStyleTypeName) {#fromName-java.lang.String}
```
public static int fromName(String conditionalStyleTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| conditionalStyleTypeName | java.lang.String |  |

**Returns:**
int
### getName(int conditionalStyleType) {#getName-int}
```
public static String getName(int conditionalStyleType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| conditionalStyleType | int |  |

**Returns:**
java.lang.String
