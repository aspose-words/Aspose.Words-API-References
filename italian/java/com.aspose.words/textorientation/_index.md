---
title: "TextOrientation"
linktitle: "TextOrientation"
second_title: "Aspose.Words per Java"
description: "Specifica l'orientamento del testo su una pagina in una cella di tabella o in un frame di testo in Java."
type: docs
weight: 675
url: /it/java/com.aspose.words/textorientation/
---

**Inheritance:**
java.lang.Object
```
public class TextOrientation
```

Specifica l'orientamento del testo su una pagina, in una cella di tabella o in un riquadro di testo.

 **Examples:** 

Mostra come creare una tabella formattata 2x2.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [DOWNWARD](#DOWNWARD) | Il testo è ruotato di 90 gradi verso destra per apparire dall'alto verso il basso (tb-rl). |
| [HORIZONTAL](#HORIZONTAL) | Il testo è disposto orizzontalmente (lr-tb). |
| [HORIZONTAL_ROTATED_FAR_EAST](#HORIZONTAL-ROTATED-FAR-EAST) | Il testo è disposto orizzontalmente, ma i caratteri dell'Estremo Oriente sono ruotati di 90 gradi verso sinistra (lr-tb-v). |
| [UPWARD](#UPWARD) | Il testo è ruotato di 90 gradi verso sinistra per apparire dal basso verso l'alto (bt-lr). |
| [VERTICAL_FAR_EAST](#VERTICAL-FAR-EAST) | I caratteri dell'Estremo Oriente appaiono verticali, gli altri testi sono ruotati di 90 gradi verso destra per apparire dall'alto verso il basso (tb-rl-v). |
| [VERTICAL_ROTATED_FAR_EAST](#VERTICAL-ROTATED-FAR-EAST) | I caratteri dell'Estremo Oriente appaiono verticali, gli altri testi sono ruotati di 90 gradi verso destra per apparire dall'alto verso il basso verticalmente, poi da sinistra a destra orizzontalmente (tb-lr-v). |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String textOrientationName)](#fromName-java.lang.String) |  |
| [getName(int textOrientation)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textOrientation)](#toString-int) |  |
### DOWNWARD {#DOWNWARD}
```
public static int DOWNWARD
```


Il testo è ruotato di 90 gradi verso destra per apparire dall'alto verso il basso (tb-rl).

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Il testo è disposto orizzontalmente (lr-tb).

### HORIZONTAL_ROTATED_FAR_EAST {#HORIZONTAL-ROTATED-FAR-EAST}
```
public static int HORIZONTAL_ROTATED_FAR_EAST
```


Il testo è disposto orizzontalmente, ma i caratteri dell'Estremo Oriente sono ruotati di 90 gradi verso sinistra (lr-tb-v).

### UPWARD {#UPWARD}
```
public static int UPWARD
```


Il testo è ruotato di 90 gradi verso sinistra per apparire dal basso verso l'alto (bt-lr).

### VERTICAL_FAR_EAST {#VERTICAL-FAR-EAST}
```
public static int VERTICAL_FAR_EAST
```


I caratteri dell'Estremo Oriente appaiono verticali, gli altri testi sono ruotati di 90 gradi verso destra per apparire dall'alto verso il basso (tb-rl-v).

### VERTICAL_ROTATED_FAR_EAST {#VERTICAL-ROTATED-FAR-EAST}
```
public static int VERTICAL_ROTATED_FAR_EAST
```


I caratteri dell'Estremo Oriente appaiono verticali, gli altri testi sono ruotati di 90 gradi verso destra per apparire dall'alto verso il basso verticalmente, poi da sinistra a destra orizzontalmente (tb-lr-v).

### length {#length}
```
public static int length
```


### fromName(String textOrientationName) {#fromName-java.lang.String}
```
public static int fromName(String textOrientationName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| textOrientationName | java.lang.String |  |

**Returns:**
int
### getName(int textOrientation) {#getName-int}
```
public static String getName(int textOrientation)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| textOrientation | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int textOrientation) {#toString-int}
```
public static String toString(int textOrientation)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| textOrientation | int |  |

**Returns:**
java.lang.String
