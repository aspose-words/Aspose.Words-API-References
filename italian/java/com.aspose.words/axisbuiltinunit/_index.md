---
title: "AxisBuiltInUnit"
linktitle: "AxisBuiltInUnit"
second_title: "Aspose.Words per Java"
description: "Specifica le unità di visualizzazione per un asse in Java."
type: docs
weight: 23
url: /it/java/com.aspose.words/axisbuiltinunit/
---

**Inheritance:**
java.lang.Object
```
public class AxisBuiltInUnit
```

Specifica le unità di visualizzazione per un asse.

 **Examples:** 

Mostra come manipolare i segni di graduazione e i valori visualizzati di un asse del grafico.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [BILLIONS](#BILLIONS) | Specifica che i valori sul grafico devono essere divisi per 1,000,000,000. |
| [CUSTOM](#CUSTOM) | Specifica che i valori sul grafico devono essere divisi per un divisore definito dall'utente. |
| [HUNDREDS](#HUNDREDS) | Specifica che i valori sul grafico devono essere divisi per 100. |
| [HUNDRED_MILLIONS](#HUNDRED-MILLIONS) | Specifica che i valori sul grafico devono essere divisi per 100,000,000. |
| [HUNDRED_THOUSANDS](#HUNDRED-THOUSANDS) | Specifica che i valori sul grafico devono essere divisi per 100,000. |
| [MILLIONS](#MILLIONS) | Specifica che i valori sul grafico devono essere divisi per 1,000,000. |
| [NONE](#NONE) | Specifica che i valori sul grafico devono essere visualizzati così come sono. |
| [PERCENTAGE](#PERCENTAGE) | Specifica che i valori sul grafico devono essere divisi per 0.01. |
| [TEN_MILLIONS](#TEN-MILLIONS) | Specifica che i valori sul grafico devono essere divisi per 10,000,000. |
| [TEN_THOUSANDS](#TEN-THOUSANDS) | Specifica che i valori sul grafico devono essere divisi per 10,000. |
| [THOUSANDS](#THOUSANDS) | Specifica che i valori sul grafico devono essere divisi per 1,000. |
| [TRILLIONS](#TRILLIONS) | Specifica che i valori sul grafico devono essere divisi per 1,000,000,000,0000. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String axisBuiltInUnitName)](#fromName-java.lang.String) |  |
| [getName(int axisBuiltInUnit)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int axisBuiltInUnit)](#toString-int) |  |
### BILLIONS {#BILLIONS}
```
public static int BILLIONS
```


Specifica che i valori sul grafico devono essere divisi per 1,000,000,000.

### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Specifica che i valori del grafico devono essere divisi per un divisore definito dall'utente. Questo valore non è supportato dai nuovi tipi di grafico di MS Office 2016.

### HUNDREDS {#HUNDREDS}
```
public static int HUNDREDS
```


Specifica che i valori sul grafico devono essere divisi per 100.

### HUNDRED_MILLIONS {#HUNDRED-MILLIONS}
```
public static int HUNDRED_MILLIONS
```


Specifica che i valori sul grafico devono essere divisi per 100,000,000.

### HUNDRED_THOUSANDS {#HUNDRED-THOUSANDS}
```
public static int HUNDRED_THOUSANDS
```


Specifica che i valori sul grafico devono essere divisi per 100,000.

### MILLIONS {#MILLIONS}
```
public static int MILLIONS
```


Specifica che i valori sul grafico devono essere divisi per 1,000,000.

### NONE {#NONE}
```
public static int NONE
```


Specifica che i valori sul grafico devono essere visualizzati così come sono.

### PERCENTAGE {#PERCENTAGE}
```
public static int PERCENTAGE
```


Specifica che i valori del grafico devono essere divisi per 0,01. Questo valore è supportato solo dai nuovi tipi di grafico di MS Office 2016.

### TEN_MILLIONS {#TEN-MILLIONS}
```
public static int TEN_MILLIONS
```


Specifica che i valori sul grafico devono essere divisi per 10,000,000.

### TEN_THOUSANDS {#TEN-THOUSANDS}
```
public static int TEN_THOUSANDS
```


Specifica che i valori sul grafico devono essere divisi per 10,000.

### THOUSANDS {#THOUSANDS}
```
public static int THOUSANDS
```


Specifica che i valori sul grafico devono essere divisi per 1,000.

### TRILLIONS {#TRILLIONS}
```
public static int TRILLIONS
```


Specifica che i valori sul grafico devono essere divisi per 1,000,000,000,0000.

### length {#length}
```
public static int length
```


### fromName(String axisBuiltInUnitName) {#fromName-java.lang.String}
```
public static int fromName(String axisBuiltInUnitName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| axisBuiltInUnitName | java.lang.String |  |

**Returns:**
int
### getName(int axisBuiltInUnit) {#getName-int}
```
public static String getName(int axisBuiltInUnit)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| axisBuiltInUnit | int |  |

**Returns:**
java.lang.String
