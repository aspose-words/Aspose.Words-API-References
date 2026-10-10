---
title: "ChartXValue"
linktitle: "ChartXValue"
second_title: "Aspose.Words für Java"
description: "Stellt einen X-Wert für eine Diagrammreihe in Java dar."
type: docs
weight: 94
url: /de/java/com.aspose.words/chartxvalue/
---

**Inheritance:**
java.lang.Object
```
public class ChartXValue
```

Stellt einen X-Wert für eine Diagrammserie dar.

 **Remarks:** 

Diese Klasse enthält mehrere statische Methoden zum Erzeugen eines X-Werts eines bestimmten Typs. Die Eigenschaft [getValueType()](../../com.aspose.words/chartxvalue/\#getValueType) ermöglicht es, den Typ eines vorhandenen X-Werts zu bestimmen.

Alle nicht‑null X-Werte einer Diagrammreihe müssen vom selben Typ [ChartXValueType](../../com.aspose.words/chartxvaluetype/) sein.

 **Examples:** 

Zeigt, wie man Diagrammserien mit Daten füllt.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Gibt ein Flag zurück, das angibt, ob das angegebene Objekt dem aktuellen X-Wert-Objekt entspricht. |
| [fromDateTime(Date value)](#fromDateTime-java.util.Date) | Erstellt eine Instanz von [ChartXValue](../../com.aspose.words/chartxvalue/) vom Typ [ChartXValueType.DATE\_TIME](../../com.aspose.words/chartxvaluetype/\#DATE-TIME). |
| [fromDouble(double value)](#fromDouble-double) | Erstellt eine Instanz von [ChartXValue](../../com.aspose.words/chartxvalue/) vom Typ [ChartXValueType.DOUBLE](../../com.aspose.words/chartxvaluetype/\#DOUBLE). |
| [fromMultilevelValue(ChartMultilevelValue value)](#fromMultilevelValue-com.aspose.words.ChartMultilevelValue) | Erstellt eine Instanz von [ChartXValue](../../com.aspose.words/chartxvalue/) vom Typ [ChartXValueType.MULTILEVEL](../../com.aspose.words/chartxvaluetype/\#MULTILEVEL). |
| [fromString(String value)](#fromString-java.lang.String) | Erstellt eine Instanz von [ChartXValue](../../com.aspose.words/chartxvalue/) vom Typ [ChartXValueType.STRING](../../com.aspose.words/chartxvaluetype/\#STRING). |
| [fromTimeSpan(long value)](#fromTimeSpan-long) | Erstellt eine Instanz von [ChartXValue](../../com.aspose.words/chartxvalue/) vom Typ [ChartXValueType.TIME](../../com.aspose.words/chartxvaluetype/\#TIME). |
| [getDateTimeValue()](#getDateTimeValue) | Gibt den gespeicherten Datums‑Zeit‑Wert zurück. |
| [getDoubleValue()](#getDoubleValue) | Gibt den gespeicherten numerischen Wert zurück. |
| [getMultilevelValue()](#getMultilevelValue) | Gibt den gespeicherten mehrstufigen Wert zurück. |
| [getStringValue()](#getStringValue) | Gibt den gespeicherten Zeichenkettenwert zurück. |
| [getTimeValue()](#getTimeValue) | Gibt den gespeicherten Zeitwert zurück. |
| [getValueType()](#getValueType) | Gibt den Typ des im Objekt gespeicherten X-Werts zurück. |
| [hashCode()](#hashCode) |  |
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Gibt ein Flag zurück, das angibt, ob das angegebene Objekt dem aktuellen X-Wert-Objekt entspricht.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### fromDateTime(Date value) {#fromDateTime-java.util.Date}
```
public static ChartXValue fromDateTime(Date value)
```


Erstellt eine Instanz von [ChartXValue](../../com.aspose.words/chartxvalue/) vom Typ [ChartXValueType.DATE\_TIME](../../com.aspose.words/chartxvaluetype/\#DATE-TIME).

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.util.Date |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromDouble(double value) {#fromDouble-double}
```
public static ChartXValue fromDouble(double value)
```


Erstellt eine Instanz von [ChartXValue](../../com.aspose.words/chartxvalue/) vom Typ [ChartXValueType.DOUBLE](../../com.aspose.words/chartxvaluetype/\#DOUBLE).

 **Examples:** 

Zeigt, wie man Diagrammserien mit Daten füllt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromMultilevelValue(ChartMultilevelValue value) {#fromMultilevelValue-com.aspose.words.ChartMultilevelValue}
```
public static ChartXValue fromMultilevelValue(ChartMultilevelValue value)
```


Erstellt eine Instanz von [ChartXValue](../../com.aspose.words/chartxvalue/) vom Typ [ChartXValueType.MULTILEVEL](../../com.aspose.words/chartxvaluetype/\#MULTILEVEL).

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [ChartMultilevelValue](../../com.aspose.words/chartmultilevelvalue/) |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromString(String value) {#fromString-java.lang.String}
```
public static ChartXValue fromString(String value)
```


Erstellt eine Instanz von [ChartXValue](../../com.aspose.words/chartxvalue/) vom Typ [ChartXValueType.STRING](../../com.aspose.words/chartxvaluetype/\#STRING).

 **Examples:** 

Zeigt, wie man Diagrammdatenwerte hinzufügt/entfernt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromTimeSpan(long value) {#fromTimeSpan-long}
```
public static ChartXValue fromTimeSpan(long value)
```


Erstellt eine Instanz von [ChartXValue](../../com.aspose.words/chartxvalue/) vom Typ [ChartXValueType.TIME](../../com.aspose.words/chartxvaluetype/\#TIME).

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | long |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### getDateTimeValue() {#getDateTimeValue}
```
public Date getDateTimeValue()
```


Gibt den gespeicherten Datums‑Zeit‑Wert zurück.

**Returns:**
java.util.Date - Der gespeicherte Datums‑Zeit‑Wert.
### getDoubleValue() {#getDoubleValue}
```
public double getDoubleValue()
```


Gibt den gespeicherten numerischen Wert zurück.

**Returns:**
double - Der gespeicherte numerische Wert.
### getMultilevelValue() {#getMultilevelValue}
```
public ChartMultilevelValue getMultilevelValue()
```


Gibt den gespeicherten mehrstufigen Wert zurück.

**Returns:**
[ChartMultilevelValue](../../com.aspose.words/chartmultilevelvalue/) - The stored multilevel value.
### getStringValue() {#getStringValue}
```
public String getStringValue()
```


Gibt den gespeicherten Zeichenkettenwert zurück.

**Returns:**
java.lang.String - Der gespeicherte Zeichenkettenwert.
### getTimeValue() {#getTimeValue}
```
public long getTimeValue()
```


Gibt den gespeicherten Zeitwert zurück.

**Returns:**
long - Der gespeicherte Zeitwert.
### getValueType() {#getValueType}
```
public int getValueType()
```


Gibt den Typ des im Objekt gespeicherten X-Werts zurück.

**Returns:**
int - Der Typ des im Objekt gespeicherten X-Werts. Der zurückgegebene Wert ist einer der [ChartXValueType](../../com.aspose.words/chartxvaluetype/) Konstanten.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
