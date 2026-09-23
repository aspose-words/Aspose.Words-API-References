---
title: "AxisBuiltInUnit"
linktitle: "AxisBuiltInUnit"
second_title: "Aspose.Words pour Java"
description: "Spécifie les unités d'affichage pour un axe en Java."
type: docs
weight: 23
url: /fr/java/com.aspose.words/axisbuiltinunit/
---

**Inheritance:**
java.lang.Object
```
public class AxisBuiltInUnit
```

Spécifie les unités d'affichage pour un axe.

 **Examples:** 

Montre comment manipuler les marques de graduation et les valeurs affichées d'un axe de graphique.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 450.0, 250.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Y-Values", chart.getSeries().get(0).getName());

 // Set the minor tick marks of the Y-axis to point away from the plot area,
 // and the major tick marks to cross the axis.
 ChartAxis axis = chart.getAxisY();
 axis.setMajorTickMark(AxisTickMark.CROSS);
 axis.setMinorTickMark(AxisTickMark.OUTSIDE);

 // Set they Y-axis to show a major tick every 10 units, and a minor tick every 1 unit.
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(1.0);

 // Set the Y-axis bounds to -10 and 20.
 // This Y-axis will now display 4 major tick marks and 27 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(20.0));

 // For the X-axis, set the major tick marks at every 10 units,
 // every minor tick mark at 2.5 units.
 axis = chart.getAxisX();
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(2.5);

 // Configure both types of tick marks to appear inside the graph plot area.
 axis.setMajorTickMark(AxisTickMark.INSIDE);
 axis.setMinorTickMark(AxisTickMark.INSIDE);

 // Set the X-axis bounds so that the X-axis spans 5 major tick marks and 12 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(30.0));
 axis.getTickLabels().setAlignment(ParagraphAlignment.RIGHT);

 Assert.assertEquals(1, axis.getTickLabels().getSpacing());
 Assert.assertEquals(doc, axis.getDisplayUnit().getDocument());

 // Set the tick labels to display their value in millions.
 axis.getDisplayUnit().setUnit(AxisBuiltInUnit.MILLIONS);

 // We can set a more specific value by which tick labels will display their values.
 // This statement is equivalent to the one above.
 axis.getDisplayUnit().setCustomUnit(1000000.0);
 doc.save(getArtifactsDir() + "Charts.AxisDisplayUnit.docx");
 
```
## Champs

| Champ | Description |
| --- | --- |
| [BILLIONS](#BILLIONS) | Spécifie que les valeurs du graphique doivent être divisées par 1,000,000,000. |
| [CUSTOM](#CUSTOM) | Spécifie que les valeurs du graphique doivent être divisées par un diviseur défini par l'utilisateur. |
| [HUNDREDS](#HUNDREDS) | Spécifie que les valeurs du graphique doivent être divisées par 100. |
| [HUNDRED_MILLIONS](#HUNDRED-MILLIONS) | Spécifie que les valeurs du graphique doivent être divisées par 100,000,000. |
| [HUNDRED_THOUSANDS](#HUNDRED-THOUSANDS) | Spécifie que les valeurs du graphique doivent être divisées par 100,000. |
| [MILLIONS](#MILLIONS) | Spécifie que les valeurs du graphique doivent être divisées par 1,000,000. |
| [NONE](#NONE) | Spécifie que les valeurs du graphique doivent être affichées telles quelles. |
| [PERCENTAGE](#PERCENTAGE) | Spécifie que les valeurs du graphique doivent être divisées par 0.01. |
| [TEN_MILLIONS](#TEN-MILLIONS) | Spécifie que les valeurs du graphique doivent être divisées par 10,000,000. |
| [TEN_THOUSANDS](#TEN-THOUSANDS) | Spécifie que les valeurs du graphique doivent être divisées par 10,000. |
| [THOUSANDS](#THOUSANDS) | Spécifie que les valeurs du graphique doivent être divisées par 1,000. |
| [TRILLIONS](#TRILLIONS) | Spécifie que les valeurs du graphique doivent être divisées par 1,000,000,000,0000. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String axisBuiltInUnitName)](#fromName-java.lang.String) |  |
| [getName(int axisBuiltInUnit)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int axisBuiltInUnit)](#toString-int) |  |
### BILLIONS {#BILLIONS}
```
public static int BILLIONS
```


Spécifie que les valeurs du graphique doivent être divisées par 1,000,000,000.

### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Spécifie que les valeurs du graphique doivent être divisées par un diviseur défini par l'utilisateur. Cette valeur n'est pas prise en charge par les nouveaux types de graphiques de MS Office 2016.

### HUNDREDS {#HUNDREDS}
```
public static int HUNDREDS
```


Spécifie que les valeurs du graphique doivent être divisées par 100.

### HUNDRED_MILLIONS {#HUNDRED-MILLIONS}
```
public static int HUNDRED_MILLIONS
```


Spécifie que les valeurs du graphique doivent être divisées par 100,000,000.

### HUNDRED_THOUSANDS {#HUNDRED-THOUSANDS}
```
public static int HUNDRED_THOUSANDS
```


Spécifie que les valeurs du graphique doivent être divisées par 100,000.

### MILLIONS {#MILLIONS}
```
public static int MILLIONS
```


Spécifie que les valeurs du graphique doivent être divisées par 1,000,000.

### NONE {#NONE}
```
public static int NONE
```


Spécifie que les valeurs du graphique doivent être affichées telles quelles.

### PERCENTAGE {#PERCENTAGE}
```
public static int PERCENTAGE
```


Spécifie que les valeurs du graphique doivent être divisées par 0,01. Cette valeur n'est prise en charge que par les nouveaux types de graphiques de MS Office 2016.

### TEN_MILLIONS {#TEN-MILLIONS}
```
public static int TEN_MILLIONS
```


Spécifie que les valeurs du graphique doivent être divisées par 10,000,000.

### TEN_THOUSANDS {#TEN-THOUSANDS}
```
public static int TEN_THOUSANDS
```


Spécifie que les valeurs du graphique doivent être divisées par 10,000.

### THOUSANDS {#THOUSANDS}
```
public static int THOUSANDS
```


Spécifie que les valeurs du graphique doivent être divisées par 1,000.

### TRILLIONS {#TRILLIONS}
```
public static int TRILLIONS
```


Spécifie que les valeurs du graphique doivent être divisées par 1,000,000,000,0000.

### length {#length}
```
public static int length
```


### fromName(String axisBuiltInUnitName) {#fromName-java.lang.String}
```
public static int fromName(String axisBuiltInUnitName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| axisBuiltInUnitName | java.lang.String |  |

**Returns:**
int
### getName(int axisBuiltInUnit) {#getName-int}
```
public static String getName(int axisBuiltInUnit)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| axisBuiltInUnit | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int axisBuiltInUnit) {#toString-int}
```
public static String toString(int axisBuiltInUnit)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| axisBuiltInUnit | int |  |

**Returns:**
java.lang.String
