---
title: "ChartDataLabelPosition"
linktitle: "ChartDataLabelPosition"
second_title: "Aspose.Words für Java"
description: "Gibt die Position für eine Diagrammdatenbeschriftung in Java an."
type: docs
weight: 74
url: /de/java/com.aspose.words/chartdatalabelposition/
---

**Inheritance:**
java.lang.Object
```
public class ChartDataLabelPosition
```

Gibt die Position für eine Diagrammdatenbeschriftung an.

 **Remarks:** 

Nicht alle Serientypen erlauben das Festlegen von Beschriftungspositionen. Und diejenigen, die es tun, unterstützen nicht alle Werte.

 **Examples:** 

Zeigt, wie die Position des Datenlabels festgelegt wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert column chart.
 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();

 // Delete default generated series.
 seriesColl.clear();

 // Add series.
 ChartSeries series = seriesColl.add(
         "Series 1",
         new String[] { "Category 1", "Category 2", "Category 3" },
         new double[] { 4.0, 5.0, 6.0 });

 // Show data labels and set font color.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.getFont().setColor(Color.WHITE);

 // Set data label position.
 dataLabels.setPosition(ChartDataLabelPosition.INSIDE_BASE);
 dataLabels.get(0).setPosition(ChartDataLabelPosition.OUTSIDE_END);
 dataLabels.get(0).getFont().setColor(Color.RED);

 doc.save(getArtifactsDir() + "Charts.LabelPosition.docx");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [ABOVE](#ABOVE) | Gibt an, dass eine Datenbeschriftung über einem Datenmarker angezeigt werden soll. |
| [BELOW](#BELOW) | Gibt an, dass eine Datenbeschriftung unter einem Datenmarker angezeigt werden soll. |
| [BEST_FIT](#BEST-FIT) | Gibt an, dass eine Datenbeschriftung in der am besten geeigneten Position angezeigt werden soll. |
| [CENTER](#CENTER) | Gibt an, dass eine Datenbeschriftung zentriert auf einem Datenmarker angezeigt werden soll. |
| [INSIDE_BASE](#INSIDE-BASE) | Gibt an, dass eine Datenbeschriftung innerhalb der Basis eines Datenmarkers angezeigt werden soll. |
| [INSIDE_END](#INSIDE-END) | Gibt an, dass eine Datenbeschriftung innerhalb des Endes eines Datenmarkers angezeigt werden soll. |
| [LEFT](#LEFT) | Gibt an, dass eine Datenbeschriftung links von einem Datenmarker angezeigt werden soll. |
| [OUTSIDE_END](#OUTSIDE-END) | Gibt an, dass eine Datenbeschriftung außerhalb des Endes eines Datenmarkers angezeigt werden soll. |
| [RIGHT](#RIGHT) | Gibt an, dass eine Datenbeschriftung rechts von einem Datenmarker angezeigt werden soll. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String chartDataLabelPositionName)](#fromName-java.lang.String) |  |
| [getName(int chartDataLabelPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartDataLabelPosition)](#toString-int) |  |
### ABOVE {#ABOVE}
```
public static int ABOVE
```


Gibt an, dass eine Datenbeschriftung über einem Datenmarker angezeigt werden soll.

### BELOW {#BELOW}
```
public static int BELOW
```


Gibt an, dass eine Datenbeschriftung unter einem Datenmarker angezeigt werden soll.

### BEST_FIT {#BEST-FIT}
```
public static int BEST_FIT
```


Gibt an, dass eine Datenbeschriftung in der am besten geeigneten Position angezeigt werden soll.

### CENTER {#CENTER}
```
public static int CENTER
```


Gibt an, dass eine Datenbeschriftung zentriert auf einem Datenmarker angezeigt werden soll.

### INSIDE_BASE {#INSIDE-BASE}
```
public static int INSIDE_BASE
```


Gibt an, dass eine Datenbeschriftung innerhalb der Basis eines Datenmarkers angezeigt werden soll.

### INSIDE_END {#INSIDE-END}
```
public static int INSIDE_END
```


Gibt an, dass eine Datenbeschriftung innerhalb des Endes eines Datenmarkers angezeigt werden soll.

### LEFT {#LEFT}
```
public static int LEFT
```


Gibt an, dass eine Datenbeschriftung links von einem Datenmarker angezeigt werden soll.

### OUTSIDE_END {#OUTSIDE-END}
```
public static int OUTSIDE_END
```


Gibt an, dass eine Datenbeschriftung außerhalb des Endes eines Datenmarkers angezeigt werden soll.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Gibt an, dass eine Datenbeschriftung rechts von einem Datenmarker angezeigt werden soll.

### length {#length}
```
public static int length
```


### fromName(String chartDataLabelPositionName) {#fromName-java.lang.String}
```
public static int fromName(String chartDataLabelPositionName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| chartDataLabelPositionName | java.lang.String |  |

**Returns:**
int
### getName(int chartDataLabelPosition) {#getName-int}
```
public static String getName(int chartDataLabelPosition)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| chartDataLabelPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int chartDataLabelPosition) {#toString-int}
```
public static String toString(int chartDataLabelPosition)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| chartDataLabelPosition | int |  |

**Returns:**
java.lang.String
