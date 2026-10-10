---
title: "TableAlignment"
linktitle: "TableAlignment"
second_title: "Aspose.Words pour Java"
description: "Spécifie l’alignement d’un tableau en ligne en Java."
type: docs
weight: 657
url: /fr/java/com.aspose.words/tablealignment/
---

**Inheritance:**
java.lang.Object
```
public class TableAlignment
```

Spécifie l'alignement d'un tableau en ligne.

 **Examples:** 

Montre comment appliquer une bordure de contour à un tableau.

```

 Document doc = new Document(getMyDir() + "Tables.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Align the table to the center of the page.
 table.setAlignment(TableAlignment.CENTER);

 // Clear any existing borders and shading from the table.
 table.clearBorders();
 table.clearShading();

 // Add green borders to the outline of the table.
 table.setBorder(BorderType.LEFT, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.RIGHT, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.TOP, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.BOTTOM, LineStyle.SINGLE, 1.5, Color.GREEN, true);

 // Fill the cells with a light green solid color.
 table.setShading(TextureIndex.TEXTURE_SOLID, Color.GREEN, Color.GREEN);

 doc.save(getArtifactsDir() + "Table.SetOutlineBorders.docx");
 
```
## Champs

| Champ | Description |
| --- | --- |
| [CENTER](#CENTER) | Le tableau est centré. |
| [LEFT](#LEFT) | Le tableau est aligné à gauche. |
| [RIGHT](#RIGHT) | Le tableau est aligné à droite. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String tableAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int tableAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tableAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Le tableau est centré.

### LEFT {#LEFT}
```
public static int LEFT
```


Le tableau est aligné à gauche.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Le tableau est aligné à droite.

### length {#length}
```
public static int length
```


### fromName(String tableAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String tableAlignmentName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| tableAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int tableAlignment) {#getName-int}
```
public static String getName(int tableAlignment)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| tableAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int tableAlignment) {#toString-int}
```
public static String toString(int tableAlignment)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| tableAlignment | int |  |

**Returns:**
java.lang.String
