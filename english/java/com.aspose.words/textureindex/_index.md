---
title: TextureIndex
linktitle: TextureIndex
second_title: Aspose.Words for Java
description: Specifies shading texture in Java.
type: docs
weight: 621
url: /java/com.aspose.words/textureindex/
---

**Inheritance:**
java.lang.Object
```
public class TextureIndex
```

Specifies shading texture.

 **Examples:** 

Shows how to apply an outline border to a table.

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

Shows how to decorate text with borders and shading.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [TEXTURE_10_PERCENT](#TEXTURE-10-PERCENT) |  |
| [TEXTURE_12_PT_5_PERCENT](#TEXTURE-12-PT-5-PERCENT) |  |
| [TEXTURE_15_PERCENT](#TEXTURE-15-PERCENT) |  |
| [TEXTURE_17_PT_5_PERCENT](#TEXTURE-17-PT-5-PERCENT) |  |
| [TEXTURE_20_PERCENT](#TEXTURE-20-PERCENT) |  |
| [TEXTURE_22_PT_5_PERCENT](#TEXTURE-22-PT-5-PERCENT) |  |
| [TEXTURE_25_PERCENT](#TEXTURE-25-PERCENT) |  |
| [TEXTURE_27_PT_5_PERCENT](#TEXTURE-27-PT-5-PERCENT) |  |
| [TEXTURE_2_PT_5_PERCENT](#TEXTURE-2-PT-5-PERCENT) |  |
| [TEXTURE_30_PERCENT](#TEXTURE-30-PERCENT) |  |
| [TEXTURE_32_PT_5_PERCENT](#TEXTURE-32-PT-5-PERCENT) |  |
| [TEXTURE_35_PERCENT](#TEXTURE-35-PERCENT) |  |
| [TEXTURE_37_PT_5_PERCENT](#TEXTURE-37-PT-5-PERCENT) |  |
| [TEXTURE_40_PERCENT](#TEXTURE-40-PERCENT) |  |
| [TEXTURE_42_PT_5_PERCENT](#TEXTURE-42-PT-5-PERCENT) |  |
| [TEXTURE_45_PERCENT](#TEXTURE-45-PERCENT) |  |
| [TEXTURE_47_PT_5_PERCENT](#TEXTURE-47-PT-5-PERCENT) |  |
| [TEXTURE_50_PERCENT](#TEXTURE-50-PERCENT) |  |
| [TEXTURE_52_PT_5_PERCENT](#TEXTURE-52-PT-5-PERCENT) |  |
| [TEXTURE_55_PERCENT](#TEXTURE-55-PERCENT) |  |
| [TEXTURE_57_PT_5_PERCENT](#TEXTURE-57-PT-5-PERCENT) |  |
| [TEXTURE_5_PERCENT](#TEXTURE-5-PERCENT) |  |
| [TEXTURE_60_PERCENT](#TEXTURE-60-PERCENT) |  |
| [TEXTURE_62_PT_5_PERCENT](#TEXTURE-62-PT-5-PERCENT) |  |
| [TEXTURE_65_PERCENT](#TEXTURE-65-PERCENT) |  |
| [TEXTURE_67_PT_5_PERCENT](#TEXTURE-67-PT-5-PERCENT) |  |
| [TEXTURE_70_PERCENT](#TEXTURE-70-PERCENT) |  |
| [TEXTURE_72_PT_5_PERCENT](#TEXTURE-72-PT-5-PERCENT) |  |
| [TEXTURE_75_PERCENT](#TEXTURE-75-PERCENT) |  |
| [TEXTURE_77_PT_5_PERCENT](#TEXTURE-77-PT-5-PERCENT) |  |
| [TEXTURE_7_PT_5_PERCENT](#TEXTURE-7-PT-5-PERCENT) |  |
| [TEXTURE_80_PERCENT](#TEXTURE-80-PERCENT) |  |
| [TEXTURE_82_PT_5_PERCENT](#TEXTURE-82-PT-5-PERCENT) |  |
| [TEXTURE_85_PERCENT](#TEXTURE-85-PERCENT) |  |
| [TEXTURE_87_PT_5_PERCENT](#TEXTURE-87-PT-5-PERCENT) |  |
| [TEXTURE_90_PERCENT](#TEXTURE-90-PERCENT) |  |
| [TEXTURE_92_PT_5_PERCENT](#TEXTURE-92-PT-5-PERCENT) |  |
| [TEXTURE_95_PERCENT](#TEXTURE-95-PERCENT) |  |
| [TEXTURE_97_PT_5_PERCENT](#TEXTURE-97-PT-5-PERCENT) |  |
| [TEXTURE_CROSS](#TEXTURE-CROSS) |  |
| [TEXTURE_DARK_CROSS](#TEXTURE-DARK-CROSS) |  |
| [TEXTURE_DARK_DIAGONAL_CROSS](#TEXTURE-DARK-DIAGONAL-CROSS) |  |
| [TEXTURE_DARK_DIAGONAL_DOWN](#TEXTURE-DARK-DIAGONAL-DOWN) |  |
| [TEXTURE_DARK_DIAGONAL_UP](#TEXTURE-DARK-DIAGONAL-UP) |  |
| [TEXTURE_DARK_HORIZONTAL](#TEXTURE-DARK-HORIZONTAL) |  |
| [TEXTURE_DARK_VERTICAL](#TEXTURE-DARK-VERTICAL) |  |
| [TEXTURE_DIAGONAL_CROSS](#TEXTURE-DIAGONAL-CROSS) |  |
| [TEXTURE_DIAGONAL_DOWN](#TEXTURE-DIAGONAL-DOWN) |  |
| [TEXTURE_DIAGONAL_UP](#TEXTURE-DIAGONAL-UP) |  |
| [TEXTURE_HORIZONTAL](#TEXTURE-HORIZONTAL) |  |
| [TEXTURE_NIL](#TEXTURE-NIL) | Specifies that there shall be no pattern used on the current shaded region (i.e. |
| [TEXTURE_NONE](#TEXTURE-NONE) |  |
| [TEXTURE_SOLID](#TEXTURE-SOLID) |  |
| [TEXTURE_VERTICAL](#TEXTURE-VERTICAL) |  |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String textureIndexName)](#fromName-java.lang.String) |  |
| [getName(int textureIndex)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textureIndex)](#toString-int) |  |
### TEXTURE_10_PERCENT {#TEXTURE-10-PERCENT}
```
public static int TEXTURE_10_PERCENT
```




### TEXTURE_12_PT_5_PERCENT {#TEXTURE-12-PT-5-PERCENT}
```
public static int TEXTURE_12_PT_5_PERCENT
```




### TEXTURE_15_PERCENT {#TEXTURE-15-PERCENT}
```
public static int TEXTURE_15_PERCENT
```




### TEXTURE_17_PT_5_PERCENT {#TEXTURE-17-PT-5-PERCENT}
```
public static int TEXTURE_17_PT_5_PERCENT
```




### TEXTURE_20_PERCENT {#TEXTURE-20-PERCENT}
```
public static int TEXTURE_20_PERCENT
```




### TEXTURE_22_PT_5_PERCENT {#TEXTURE-22-PT-5-PERCENT}
```
public static int TEXTURE_22_PT_5_PERCENT
```




### TEXTURE_25_PERCENT {#TEXTURE-25-PERCENT}
```
public static int TEXTURE_25_PERCENT
```




### TEXTURE_27_PT_5_PERCENT {#TEXTURE-27-PT-5-PERCENT}
```
public static int TEXTURE_27_PT_5_PERCENT
```




### TEXTURE_2_PT_5_PERCENT {#TEXTURE-2-PT-5-PERCENT}
```
public static int TEXTURE_2_PT_5_PERCENT
```




### TEXTURE_30_PERCENT {#TEXTURE-30-PERCENT}
```
public static int TEXTURE_30_PERCENT
```




### TEXTURE_32_PT_5_PERCENT {#TEXTURE-32-PT-5-PERCENT}
```
public static int TEXTURE_32_PT_5_PERCENT
```




### TEXTURE_35_PERCENT {#TEXTURE-35-PERCENT}
```
public static int TEXTURE_35_PERCENT
```




### TEXTURE_37_PT_5_PERCENT {#TEXTURE-37-PT-5-PERCENT}
```
public static int TEXTURE_37_PT_5_PERCENT
```




### TEXTURE_40_PERCENT {#TEXTURE-40-PERCENT}
```
public static int TEXTURE_40_PERCENT
```




### TEXTURE_42_PT_5_PERCENT {#TEXTURE-42-PT-5-PERCENT}
```
public static int TEXTURE_42_PT_5_PERCENT
```




### TEXTURE_45_PERCENT {#TEXTURE-45-PERCENT}
```
public static int TEXTURE_45_PERCENT
```




### TEXTURE_47_PT_5_PERCENT {#TEXTURE-47-PT-5-PERCENT}
```
public static int TEXTURE_47_PT_5_PERCENT
```




### TEXTURE_50_PERCENT {#TEXTURE-50-PERCENT}
```
public static int TEXTURE_50_PERCENT
```




### TEXTURE_52_PT_5_PERCENT {#TEXTURE-52-PT-5-PERCENT}
```
public static int TEXTURE_52_PT_5_PERCENT
```




### TEXTURE_55_PERCENT {#TEXTURE-55-PERCENT}
```
public static int TEXTURE_55_PERCENT
```




### TEXTURE_57_PT_5_PERCENT {#TEXTURE-57-PT-5-PERCENT}
```
public static int TEXTURE_57_PT_5_PERCENT
```




### TEXTURE_5_PERCENT {#TEXTURE-5-PERCENT}
```
public static int TEXTURE_5_PERCENT
```




### TEXTURE_60_PERCENT {#TEXTURE-60-PERCENT}
```
public static int TEXTURE_60_PERCENT
```




### TEXTURE_62_PT_5_PERCENT {#TEXTURE-62-PT-5-PERCENT}
```
public static int TEXTURE_62_PT_5_PERCENT
```




### TEXTURE_65_PERCENT {#TEXTURE-65-PERCENT}
```
public static int TEXTURE_65_PERCENT
```




### TEXTURE_67_PT_5_PERCENT {#TEXTURE-67-PT-5-PERCENT}
```
public static int TEXTURE_67_PT_5_PERCENT
```




### TEXTURE_70_PERCENT {#TEXTURE-70-PERCENT}
```
public static int TEXTURE_70_PERCENT
```




### TEXTURE_72_PT_5_PERCENT {#TEXTURE-72-PT-5-PERCENT}
```
public static int TEXTURE_72_PT_5_PERCENT
```




### TEXTURE_75_PERCENT {#TEXTURE-75-PERCENT}
```
public static int TEXTURE_75_PERCENT
```




### TEXTURE_77_PT_5_PERCENT {#TEXTURE-77-PT-5-PERCENT}
```
public static int TEXTURE_77_PT_5_PERCENT
```




### TEXTURE_7_PT_5_PERCENT {#TEXTURE-7-PT-5-PERCENT}
```
public static int TEXTURE_7_PT_5_PERCENT
```




### TEXTURE_80_PERCENT {#TEXTURE-80-PERCENT}
```
public static int TEXTURE_80_PERCENT
```




### TEXTURE_82_PT_5_PERCENT {#TEXTURE-82-PT-5-PERCENT}
```
public static int TEXTURE_82_PT_5_PERCENT
```




### TEXTURE_85_PERCENT {#TEXTURE-85-PERCENT}
```
public static int TEXTURE_85_PERCENT
```




### TEXTURE_87_PT_5_PERCENT {#TEXTURE-87-PT-5-PERCENT}
```
public static int TEXTURE_87_PT_5_PERCENT
```




### TEXTURE_90_PERCENT {#TEXTURE-90-PERCENT}
```
public static int TEXTURE_90_PERCENT
```




### TEXTURE_92_PT_5_PERCENT {#TEXTURE-92-PT-5-PERCENT}
```
public static int TEXTURE_92_PT_5_PERCENT
```




### TEXTURE_95_PERCENT {#TEXTURE-95-PERCENT}
```
public static int TEXTURE_95_PERCENT
```




### TEXTURE_97_PT_5_PERCENT {#TEXTURE-97-PT-5-PERCENT}
```
public static int TEXTURE_97_PT_5_PERCENT
```




### TEXTURE_CROSS {#TEXTURE-CROSS}
```
public static int TEXTURE_CROSS
```




### TEXTURE_DARK_CROSS {#TEXTURE-DARK-CROSS}
```
public static int TEXTURE_DARK_CROSS
```




### TEXTURE_DARK_DIAGONAL_CROSS {#TEXTURE-DARK-DIAGONAL-CROSS}
```
public static int TEXTURE_DARK_DIAGONAL_CROSS
```




### TEXTURE_DARK_DIAGONAL_DOWN {#TEXTURE-DARK-DIAGONAL-DOWN}
```
public static int TEXTURE_DARK_DIAGONAL_DOWN
```




### TEXTURE_DARK_DIAGONAL_UP {#TEXTURE-DARK-DIAGONAL-UP}
```
public static int TEXTURE_DARK_DIAGONAL_UP
```




### TEXTURE_DARK_HORIZONTAL {#TEXTURE-DARK-HORIZONTAL}
```
public static int TEXTURE_DARK_HORIZONTAL
```




### TEXTURE_DARK_VERTICAL {#TEXTURE-DARK-VERTICAL}
```
public static int TEXTURE_DARK_VERTICAL
```




### TEXTURE_DIAGONAL_CROSS {#TEXTURE-DIAGONAL-CROSS}
```
public static int TEXTURE_DIAGONAL_CROSS
```




### TEXTURE_DIAGONAL_DOWN {#TEXTURE-DIAGONAL-DOWN}
```
public static int TEXTURE_DIAGONAL_DOWN
```




### TEXTURE_DIAGONAL_UP {#TEXTURE-DIAGONAL-UP}
```
public static int TEXTURE_DIAGONAL_UP
```




### TEXTURE_HORIZONTAL {#TEXTURE-HORIZONTAL}
```
public static int TEXTURE_HORIZONTAL
```




### TEXTURE_NIL {#TEXTURE-NIL}
```
public static int TEXTURE_NIL
```


Specifies that there shall be no pattern used on the current shaded region (i.e. the pattern shall be a complete fill with the background color).

### TEXTURE_NONE {#TEXTURE-NONE}
```
public static int TEXTURE_NONE
```




### TEXTURE_SOLID {#TEXTURE-SOLID}
```
public static int TEXTURE_SOLID
```




### TEXTURE_VERTICAL {#TEXTURE-VERTICAL}
```
public static int TEXTURE_VERTICAL
```




### length {#length}
```
public static int length
```


### fromName(String textureIndexName) {#fromName-java.lang.String}
```
public static int fromName(String textureIndexName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| textureIndexName | java.lang.String |  |

**Returns:**
int
### getName(int textureIndex) {#getName-int}
```
public static String getName(int textureIndex)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| textureIndex | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int textureIndex) {#toString-int}
```
public static String toString(int textureIndex)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| textureIndex | int |  |

**Returns:**
java.lang.String
