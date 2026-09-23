---
title: "ChartYValue"
linktitle: "ChartYValue"
second_title: "Aspose.Words für Java"
description: "Stellt einen Y‑Wert für eine Diagrammreihe in Java dar."
type: docs
weight: 97
url: /de/java/com.aspose.words/chartyvalue/
---

**Inheritance:**
java.lang.Object
```
public class ChartYValue
```

Stellt einen Y-Wert für eine Diagrammserie dar.

 **Remarks:** 

Diese Klasse enthält mehrere statische Methoden zum Erstellen eines Y‑Werts eines bestimmten Typs. Die Eigenschaft [getValueType()](../../com.aspose.words/chartyvalue/\#getValueType) ermöglicht es Ihnen, den Typ eines vorhandenen Y‑Werts zu bestimmen.

Alle nicht‑null Y‑Werte einer Diagrammreihe müssen vom selben Typ [ChartYValueType](../../com.aspose.words/chartyvaluetype/) sein.
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Gibt ein Flag zurück, das angibt, ob das angegebene Objekt dem aktuellen Y‑Wert‑Objekt gleich ist. |
| [fromDateTime(Date value)](#fromDateTime-java.util.Date) | Erstellt eine Instanz von [ChartYValue](../../com.aspose.words/chartyvalue/) des Typs [ChartYValueType.DATE\_TIME](../../com.aspose.words/chartyvaluetype/\#DATE-TIME). |
| [fromDouble(double value)](#fromDouble-double) | Erstellt eine Instanz von [ChartYValue](../../com.aspose.words/chartyvalue/) des Typs [ChartYValueType.DOUBLE](../../com.aspose.words/chartyvaluetype/\#DOUBLE). |
| [fromTimeSpan(long value)](#fromTimeSpan-long) | Erstellt eine Instanz von [ChartYValue](../../com.aspose.words/chartyvalue/) des Typs [ChartYValueType.TIME](../../com.aspose.words/chartyvaluetype/\#TIME). |
| [getDateTimeValue()](#getDateTimeValue) | Gibt den gespeicherten Datums‑Zeit‑Wert zurück. |
| [getDoubleValue()](#getDoubleValue) | Gibt den gespeicherten numerischen Wert zurück. |
| [getTimeValue()](#getTimeValue) | Gibt den gespeicherten Zeitwert zurück. |
| [getValueType()](#getValueType) | Gibt den Typ des im Objekt gespeicherten Y‑Werts zurück. |
| [hashCode()](#hashCode) |  |
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Gibt ein Flag zurück, das angibt, ob das angegebene Objekt dem aktuellen Y‑Wert‑Objekt gleich ist.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### fromDateTime(Date value) {#fromDateTime-java.util.Date}
```
public static ChartYValue fromDateTime(Date value)
```


Erstellt eine Instanz von [ChartYValue](../../com.aspose.words/chartyvalue/) des Typs [ChartYValueType.DATE\_TIME](../../com.aspose.words/chartyvaluetype/\#DATE-TIME).

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.util.Date |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/)
### fromDouble(double value) {#fromDouble-double}
```
public static ChartYValue fromDouble(double value)
```


Erstellt eine Instanz von [ChartYValue](../../com.aspose.words/chartyvalue/) des Typs [ChartYValueType.DOUBLE](../../com.aspose.words/chartyvaluetype/\#DOUBLE).

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
[ChartYValue](../../com.aspose.words/chartyvalue/)
### fromTimeSpan(long value) {#fromTimeSpan-long}
```
public static ChartYValue fromTimeSpan(long value)
```


Erstellt eine Instanz von [ChartYValue](../../com.aspose.words/chartyvalue/) des Typs [ChartYValueType.TIME](../../com.aspose.words/chartyvaluetype/\#TIME).

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | long |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/)
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


Gibt den Typ des im Objekt gespeicherten Y‑Werts zurück.

**Returns:**
int – Der Typ des im Objekt gespeicherten Y‑Werts. Der zurückgegebene Wert ist einer der Konstanten von [ChartYValueType](../../com.aspose.words/chartyvaluetype/).
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
