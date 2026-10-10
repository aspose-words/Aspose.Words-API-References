---
title: "ChartXValue"
linktitle: "ChartXValue"
second_title: "Aspose.Words pour Java"
description: "Représente une valeur X pour une série de graphique en Java."
type: docs
weight: 94
url: /fr/java/com.aspose.words/chartxvalue/
---

**Inheritance:**
java.lang.Object
```
public class ChartXValue
```

Représente une valeur X pour une série de graphique.

 **Remarks:** 

Cette classe contient un certain nombre de méthodes statiques pour créer une valeur X d'un type particulier. La propriété [getValueType()](../../com.aspose.words/chartxvalue/\#getValueType) vous permet de déterminer le type d'une valeur X existante.

Toutes les valeurs X non nulles d'une série de graphique doivent être du même type [ChartXValueType](../../com.aspose.words/chartxvaluetype/).

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Obtient un indicateur indiquant si l'objet spécifié est égal à l'objet valeur X actuel. |
| [fromDateTime(Date value)](#fromDateTime-java.util.Date) | Crée une instance de [ChartXValue](../../com.aspose.words/chartxvalue/) du type [ChartXValueType.DATE\_TIME](../../com.aspose.words/chartxvaluetype/\#DATE-TIME). |
| [fromDouble(double value)](#fromDouble-double) | Crée une instance de [ChartXValue](../../com.aspose.words/chartxvalue/) du type [ChartXValueType.DOUBLE](../../com.aspose.words/chartxvaluetype/\#DOUBLE). |
| [fromMultilevelValue(ChartMultilevelValue value)](#fromMultilevelValue-com.aspose.words.ChartMultilevelValue) | Crée une instance de [ChartXValue](../../com.aspose.words/chartxvalue/) du type [ChartXValueType.MULTILEVEL](../../com.aspose.words/chartxvaluetype/\#MULTILEVEL). |
| [fromString(String value)](#fromString-java.lang.String) | Crée une instance de [ChartXValue](../../com.aspose.words/chartxvalue/) du type [ChartXValueType.STRING](../../com.aspose.words/chartxvaluetype/\#STRING). |
| [fromTimeSpan(long value)](#fromTimeSpan-long) | Crée une instance de [ChartXValue](../../com.aspose.words/chartxvalue/) du type [ChartXValueType.TIME](../../com.aspose.words/chartxvaluetype/\#TIME). |
| [getDateTimeValue()](#getDateTimeValue) | Obtient la valeur datetime stockée. |
| [getDoubleValue()](#getDoubleValue) | Obtient la valeur numérique stockée. |
| [getMultilevelValue()](#getMultilevelValue) | Obtient la valeur multilevel stockée. |
| [getStringValue()](#getStringValue) | Obtient la valeur de chaîne stockée. |
| [getTimeValue()](#getTimeValue) | Obtient la valeur de temps stockée. |
| [getValueType()](#getValueType) | Obtient le type de la valeur X stockée dans l'objet. |
| [hashCode()](#hashCode) |  |
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Obtient un indicateur indiquant si l'objet spécifié est égal à l'objet valeur X actuel.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### fromDateTime(Date value) {#fromDateTime-java.util.Date}
```
public static ChartXValue fromDateTime(Date value)
```


Crée une instance de [ChartXValue](../../com.aspose.words/chartxvalue/) du type [ChartXValueType.DATE\_TIME](../../com.aspose.words/chartxvaluetype/\#DATE-TIME).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.util.Date |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromDouble(double value) {#fromDouble-double}
```
public static ChartXValue fromDouble(double value)
```


Crée une instance de [ChartXValue](../../com.aspose.words/chartxvalue/) du type [ChartXValueType.DOUBLE](../../com.aspose.words/chartxvaluetype/\#DOUBLE).

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
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromMultilevelValue(ChartMultilevelValue value) {#fromMultilevelValue-com.aspose.words.ChartMultilevelValue}
```
public static ChartXValue fromMultilevelValue(ChartMultilevelValue value)
```


Crée une instance de [ChartXValue](../../com.aspose.words/chartxvalue/) du type [ChartXValueType.MULTILEVEL](../../com.aspose.words/chartxvaluetype/\#MULTILEVEL).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | [ChartMultilevelValue](../../com.aspose.words/chartmultilevelvalue/) |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromString(String value) {#fromString-java.lang.String}
```
public static ChartXValue fromString(String value)
```


Crée une instance de [ChartXValue](../../com.aspose.words/chartxvalue/) du type [ChartXValueType.STRING](../../com.aspose.words/chartxvaluetype/\#STRING).

 **Examples:** 

Montre comment ajouter/supprimer des valeurs de données de graphique.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder();

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries department1Series = chart.getSeries().get(0);
 ChartSeries department2Series = chart.getSeries().get(1);

 // Remove the first value in the both series.
 department1Series.remove(0);
 department2Series.remove(0);

 // Add new values to the both series.
 ChartXValue newXCategory = ChartXValue.fromString("Q1, 2023");
 department1Series.add(newXCategory, ChartYValue.fromDouble(10.3));
 department2Series.add(newXCategory, ChartYValue.fromDouble(5.7));

 doc.save(getArtifactsDir() + "Charts.ChartDataValues.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromTimeSpan(long value) {#fromTimeSpan-long}
```
public static ChartXValue fromTimeSpan(long value)
```


Crée une instance de [ChartXValue](../../com.aspose.words/chartxvalue/) du type [ChartXValueType.TIME](../../com.aspose.words/chartxvaluetype/\#TIME).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | long |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
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
### getMultilevelValue() {#getMultilevelValue}
```
public ChartMultilevelValue getMultilevelValue()
```


Obtient la valeur multilevel stockée.

**Returns:**
[ChartMultilevelValue](../../com.aspose.words/chartmultilevelvalue/) - The stored multilevel value.
### getStringValue() {#getStringValue}
```
public String getStringValue()
```


Obtient la valeur de chaîne stockée.

**Returns:**
java.lang.String - La valeur de chaîne stockée.
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


Obtient le type de la valeur X stockée dans l'objet.

**Returns:**
int - Le type de la valeur X stockée dans l'objet. La valeur renvoyée est l'une des constantes [ChartXValueType](../../com.aspose.words/chartxvaluetype/).
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
