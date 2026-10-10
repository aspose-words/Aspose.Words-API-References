---
title: "ChartYValue"
linktitle: "ChartYValue"
second_title: "Aspose.Words pour Java"
description: "Représente une valeur Y pour une série de graphique en Java."
type: docs
weight: 97
url: /fr/java/com.aspose.words/chartyvalue/
---

**Inheritance:**
java.lang.Object
```
public class ChartYValue
```

Représente une valeur Y pour une série de graphique.

 **Remarks:** 

Cette classe contient un certain nombre de méthodes statiques pour créer une valeur Y d'un type particulier. La propriété [getValueType()](../../com.aspose.words/chartyvalue/\#getValueType) vous permet de déterminer le type d'une valeur Y existante.

Toutes les valeurs Y non nulles d'une série de graphique doivent être du même type [ChartYValueType](../../com.aspose.words/chartyvaluetype/).
## Méthodes

| Méthode | Description |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Obtient un indicateur indiquant si l'objet spécifié est égal à l'objet valeur Y actuel. |
| [fromDateTime(Date value)](#fromDateTime-java.util.Date) | Crée une instance [ChartYValue](../../com.aspose.words/chartyvalue/) du type [ChartYValueType.DATE\_TIME](../../com.aspose.words/chartyvaluetype/\#DATE-TIME). |
| [fromDouble(double value)](#fromDouble-double) | Crée une instance [ChartYValue](../../com.aspose.words/chartyvalue/) du type [ChartYValueType.DOUBLE](../../com.aspose.words/chartyvaluetype/\#DOUBLE). |
| [fromTimeSpan(long value)](#fromTimeSpan-long) | Crée une instance [ChartYValue](../../com.aspose.words/chartyvalue/) du type [ChartYValueType.TIME](../../com.aspose.words/chartyvaluetype/\#TIME). |
| [getDateTimeValue()](#getDateTimeValue) | Obtient la valeur datetime stockée. |
| [getDoubleValue()](#getDoubleValue) | Obtient la valeur numérique stockée. |
| [getTimeValue()](#getTimeValue) | Obtient la valeur de temps stockée. |
| [getValueType()](#getValueType) | Obtient le type de la valeur Y stockée dans l'objet. |
| [hashCode()](#hashCode) |  |
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Obtient un indicateur indiquant si l'objet spécifié est égal à l'objet valeur Y actuel.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### fromDateTime(Date value) {#fromDateTime-java.util.Date}
```
public static ChartYValue fromDateTime(Date value)
```


Crée une instance [ChartYValue](../../com.aspose.words/chartyvalue/) du type [ChartYValueType.DATE\_TIME](../../com.aspose.words/chartyvaluetype/\#DATE-TIME).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.util.Date |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/)
### fromDouble(double value) {#fromDouble-double}
```
public static ChartYValue fromDouble(double value)
```


Crée une instance [ChartYValue](../../com.aspose.words/chartyvalue/) du type [ChartYValueType.DOUBLE](../../com.aspose.words/chartyvaluetype/\#DOUBLE).

 **Examples:** 

Montre comment remplir la série de graphique avec des données.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries series1 = chart.getSeries().get(0);

 // Clear X and Y values of the first series.
 series1.clearValues();

 // Populate the series with data.
 series1.add(ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0), 10.0);
 series1.add(ChartXValue.fromDouble(5.0), ChartYValue.fromDouble(5.0));
 series1.add(ChartXValue.fromDouble(7.0), ChartYValue.fromDouble(11.0));
 series1.add(ChartXValue.fromDouble(9.0));

 ChartSeries series2 = chart.getSeries().get(1);

 // Clear X and Y values of the second series.
 series2.clear();

 // Populate the series with data.
 series2.add(ChartXValue.fromDouble(2.0), ChartYValue.fromDouble(4.0));
 series2.add(ChartXValue.fromDouble(4.0), ChartYValue.fromDouble(7.0));
 series2.add(ChartXValue.fromDouble(6.0), ChartYValue.fromDouble(14.0));
 series2.add(ChartXValue.fromDouble(8.0), ChartYValue.fromDouble(7.0));

 doc.save(getArtifactsDir() + "Charts.PopulateChartWithData.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/)
### fromTimeSpan(long value) {#fromTimeSpan-long}
```
public static ChartYValue fromTimeSpan(long value)
```


Crée une instance [ChartYValue](../../com.aspose.words/chartyvalue/) du type [ChartYValueType.TIME](../../com.aspose.words/chartyvaluetype/\#TIME).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | long |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/)
### getDateTimeValue() {#getDateTimeValue}
```
public Date getDateTimeValue()
```


Obtient la valeur datetime stockée.

**Returns:**
java.util.Date - La valeur de date/heure stockée.
### getDoubleValue() {#getDoubleValue}
```
public double getDoubleValue()
```


Obtient la valeur numérique stockée.

**Returns:**
double - La valeur numérique stockée.
### getTimeValue() {#getTimeValue}
```
public long getTimeValue()
```


Obtient la valeur de temps stockée.

**Returns:**
long - La valeur de temps stockée.
### getValueType() {#getValueType}
```
public int getValueType()
```


Obtient le type de la valeur Y stockée dans l'objet.

**Returns:**
int - Le type de la valeur Y stockée dans l'objet. La valeur retournée est l'une des constantes [ChartYValueType](../../com.aspose.words/chartyvaluetype/).
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
