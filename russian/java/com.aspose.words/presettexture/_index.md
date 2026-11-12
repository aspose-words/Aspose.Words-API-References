---
title: "PresetTexture"
linktitle: "PresetTexture"
second_title: "Aspose.Words для Java"
description: "Указывает текстуру, используемую для заполнения фигуры в Java."
type: docs
weight: 552
url: /ru/java/com.aspose.words/presettexture/
---

**Inheritance:**
java.lang.Object
```
public class PresetTexture
```

Указывает текстуру, используемую для заполнения фигуры.

 **Examples:** 

Показывает, как задать форматирование маркера.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();
 ChartSeries series = chart.getSeries().add("AW Series 1", new double[] { 0.7, 1.8, 2.6, 3.9 },
         new double[] { 2.7, 3.2, 0.8, 1.7 });

 // Set marker formatting.
 series.getMarker().setSize(40);
 series.getMarker().setSymbol(MarkerSymbol.SQUARE);
 ChartDataPointCollection dataPoints = series.getDataPoints();
 dataPoints.get(0).getMarker().getFormat().getFill().presetTextured(PresetTexture.DENIM);
 dataPoints.get(0).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(0).getMarker().getFormat().getStroke().setBackColor(Color.RED);
 dataPoints.get(1).getMarker().getFormat().getFill().presetTextured(PresetTexture.WATER_DROPLETS);
 dataPoints.get(1).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(1).getMarker().getFormat().getStroke().setVisible(false);
 dataPoints.get(2).getMarker().getFormat().getFill().presetTextured(PresetTexture.GREEN_MARBLE);
 dataPoints.get(2).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getFill().presetTextured(PresetTexture.OAK);
 dataPoints.get(3).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getStroke().setTransparency(0.5);

 doc.save(getArtifactsDir() + "Charts.MarkerFormatting.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [BLUE_TISSUE_PAPER](#BLUE-TISSUE-PAPER) | Текстура синей бумажной салфетки. |
| [BOUQUET](#BOUQUET) | Текстура букета. |
| [BROWN_MARBLE](#BROWN-MARBLE) | Текстура коричневого мрамора. |
| [CANVAS](#CANVAS) | Текстура холста. |
| [CORK](#CORK) | Текстура пробки. |
| [DENIM](#DENIM) | Текстура денима. |
| [FISH_FOSSIL](#FISH-FOSSIL) | Текстура окаменелой рыбы. |
| [GRANITE](#GRANITE) | Текстура гранита. |
| [GREEN_MARBLE](#GREEN-MARBLE) | Текстура зелёного мрамора. |
| [MEDIUM_WOOD](#MEDIUM-WOOD) | Текстура средней древесины. |
| [NEWSPRINT](#NEWSPRINT) | Текстура газетной бумаги. |
| [NONE](#NONE) | Без текстуры. |
| [OAK](#OAK) | Текстура дуба. |
| [PAPER_BAG](#PAPER-BAG) | Текстура бумажного пакета. |
| [PAPYRUS](#PAPYRUS) | Текстура папируса. |
| [PARCHMENT](#PARCHMENT) | Текстура пергамента. |
| [PINK_TISSUE_PAPER](#PINK-TISSUE-PAPER) | Текстура розовой туалетной бумаги. |
| [PURPLE_MESH](#PURPLE-MESH) | Текстура фиолетовой сетки. |
| [RECYCLED_PAPER](#RECYCLED-PAPER) | Текстура переработанной бумаги. |
| [SAND](#SAND) | Текстура песка. |
| [STATIONERY](#STATIONERY) | Текстура канцелярии. |
| [WALNUT](#WALNUT) | Текстура ореха. |
| [WATER_DROPLETS](#WATER-DROPLETS) | Текстура капель воды. |
| [WHITE_MARBLE](#WHITE-MARBLE) | Текстура белого мрамора. |
| [WOVEN_MAT](#WOVEN-MAT) | Текстура плетёного коврика. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String presetTextureName)](#fromName-java.lang.String) |  |
| [getName(int presetTexture)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int presetTexture)](#toString-int) |  |
### BLUE_TISSUE_PAPER {#BLUE-TISSUE-PAPER}
```
public static int BLUE_TISSUE_PAPER
```


Текстура синей бумажной салфетки.

### BOUQUET {#BOUQUET}
```
public static int BOUQUET
```


Текстура букета.

### BROWN_MARBLE {#BROWN-MARBLE}
```
public static int BROWN_MARBLE
```


Текстура коричневого мрамора.

### CANVAS {#CANVAS}
```
public static int CANVAS
```


Текстура холста.

### CORK {#CORK}
```
public static int CORK
```


Текстура пробки.

### DENIM {#DENIM}
```
public static int DENIM
```


Текстура денима.

### FISH_FOSSIL {#FISH-FOSSIL}
```
public static int FISH_FOSSIL
```


Текстура окаменелой рыбы.

### GRANITE {#GRANITE}
```
public static int GRANITE
```


Текстура гранита.

### GREEN_MARBLE {#GREEN-MARBLE}
```
public static int GREEN_MARBLE
```


Текстура зелёного мрамора.

### MEDIUM_WOOD {#MEDIUM-WOOD}
```
public static int MEDIUM_WOOD
```


Текстура средней древесины.

### NEWSPRINT {#NEWSPRINT}
```
public static int NEWSPRINT
```


Текстура газетной бумаги.

### NONE {#NONE}
```
public static int NONE
```


Без текстуры.

### OAK {#OAK}
```
public static int OAK
```


Текстура дуба.

### PAPER_BAG {#PAPER-BAG}
```
public static int PAPER_BAG
```


Текстура бумажного пакета.

### PAPYRUS {#PAPYRUS}
```
public static int PAPYRUS
```


Текстура папируса.

### PARCHMENT {#PARCHMENT}
```
public static int PARCHMENT
```


Текстура пергамента.

### PINK_TISSUE_PAPER {#PINK-TISSUE-PAPER}
```
public static int PINK_TISSUE_PAPER
```


Текстура розовой туалетной бумаги.

### PURPLE_MESH {#PURPLE-MESH}
```
public static int PURPLE_MESH
```


Текстура фиолетовой сетки.

### RECYCLED_PAPER {#RECYCLED-PAPER}
```
public static int RECYCLED_PAPER
```


Текстура переработанной бумаги.

### SAND {#SAND}
```
public static int SAND
```


Текстура песка.

### STATIONERY {#STATIONERY}
```
public static int STATIONERY
```


Текстура канцелярии.

### WALNUT {#WALNUT}
```
public static int WALNUT
```


Текстура ореха.

### WATER_DROPLETS {#WATER-DROPLETS}
```
public static int WATER_DROPLETS
```


Текстура капель воды.

### WHITE_MARBLE {#WHITE-MARBLE}
```
public static int WHITE_MARBLE
```


Текстура белого мрамора.

### WOVEN_MAT {#WOVEN-MAT}
```
public static int WOVEN_MAT
```


Текстура плетёного коврика.

### length {#length}
```
public static int length
```


### fromName(String presetTextureName) {#fromName-java.lang.String}
```
public static int fromName(String presetTextureName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| presetTextureName | java.lang.String |  |

**Returns:**
int
### getName(int presetTexture) {#getName-int}
```
public static String getName(int presetTexture)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| presetTexture | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int presetTexture) {#toString-int}
```
public static String toString(int presetTexture)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| presetTexture | int |  |

**Returns:**
java.lang.String
