---
title: "AutoFitBehavior"
linktitle: "AutoFitBehavior"
second_title: "Aspose.Words pour Java"
description: "Détermine comment Aspose.Words redimensionne le tableau lorsque vous invoquez la méthode MAspose.Words.Tables.Table.AutoFitAspose.Words.Tables.AutoFitBehavior en Java."
type: docs
weight: 21
url: /fr/java/com.aspose.words/autofitbehavior/
---

**Inheritance:**
java.lang.Object
```
public class AutoFitBehavior
```

Détermine comment Aspose.Words redimensionne le tableau lorsque vous invoquez la méthode **M:Aspose.Words.Tables.Table.AutoFit(Aspose.Words.Tables.AutoFitBehavior)**.

 **Examples:** 

Montre comment créer un nouveau tableau tout en appliquant un style.

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

Montre comment créer un tableau 2x2 formaté.

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
## Champs

| Champ | Description |
| --- | --- |
| [AUTO_FIT_TO_CONTENTS](#AUTO-FIT-TO-CONTENTS) | Aspose.Words active l'option AutoFit, supprime la largeur préférée du tableau et de toutes les cellules, puis met à jour la mise en page du tableau. |
| [AUTO_FIT_TO_WINDOW](#AUTO-FIT-TO-WINDOW) | Lorsque vous utilisez cette valeur, Aspose.Words active l'option AutoFit, définit la largeur préférée du tableau à 100 %, supprime les largeurs préférées de toutes les cellules, puis met à jour la mise en page du tableau. |
| [FIXED_COLUMN_WIDTHS](#FIXED-COLUMN-WIDTHS) | Aspose.Words désactive l'option AutoFit et supprime la largeur préférée du tableau. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String autoFitBehaviorName)](#fromName-java.lang.String) |  |
| [getName(int autoFitBehavior)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int autoFitBehavior)](#toString-int) |  |
### AUTO_FIT_TO_CONTENTS {#AUTO-FIT-TO-CONTENTS}
```
public static int AUTO_FIT_TO_CONTENTS
```


Aspose.Words active l'option AutoFit, supprime la largeur préférée du tableau et de toutes les cellules, puis met à jour la mise en page du tableau.

Dans le tableau résultant, les largeurs des cellules sont mises à jour pour s'adapter au contenu du tableau. Très probablement, le tableau rétrécira.

### AUTO_FIT_TO_WINDOW {#AUTO-FIT-TO-WINDOW}
```
public static int AUTO_FIT_TO_WINDOW
```


Lorsque vous utilisez cette valeur, Aspose.Words active l'option AutoFit, définit la largeur préférée du tableau à 100 %, supprime les largeurs préférées de toutes les cellules, puis met à jour la mise en page du tableau.

En conséquence, le tableau occupe toute la largeur disponible et les largeurs des cellules sont mises à jour pour s'adapter au contenu du tableau.

### FIXED_COLUMN_WIDTHS {#FIXED-COLUMN-WIDTHS}
```
public static int FIXED_COLUMN_WIDTHS
```


Aspose.Words désactive l'option AutoFit et supprime la largeur préférée du tableau.

Les largeurs des cellules restent telles qu'elles sont spécifiées par leurs propriétés [CellFormat.getWidth()](../../com.aspose.words/cellformat/\#getWidth) / [CellFormat.setWidth(double)](../../com.aspose.words/cellformat/\#setWidth-double).

### length {#length}
```
public static int length
```


### fromName(String autoFitBehaviorName) {#fromName-java.lang.String}
```
public static int fromName(String autoFitBehaviorName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| autoFitBehaviorName | java.lang.String |  |

**Returns:**
int
### getName(int autoFitBehavior) {#getName-int}
```
public static String getName(int autoFitBehavior)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| autoFitBehavior | int |  |

**Returns:**
java.lang.String
