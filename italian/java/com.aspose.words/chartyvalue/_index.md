---
title: "ChartYValue"
linktitle: "ChartYValue"
second_title: "Aspose.Words per Java"
description: "Rappresenta un valore Y per una serie di grafico in Java."
type: docs
weight: 97
url: /it/java/com.aspose.words/chartyvalue/
---

**Inheritance:**
java.lang.Object
```
public class ChartYValue
```

Rappresenta un valore Y per una serie di grafico.

 **Remarks:** 

Questa classe contiene numerosi metodi statici per creare un valore Y di un tipo particolare. La proprietà [getValueType()](../../com.aspose.words/chartyvalue/\#getValueType) consente di determinare il tipo di un valore Y esistente.

Tutti i valori Y non nulli di una serie di grafico devono essere dello stesso tipo [ChartYValueType](../../com.aspose.words/chartyvaluetype/).
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Restituisce un flag che indica se l'oggetto specificato è uguale all'oggetto valore Y corrente. |
| [fromDateTime(Date value)](#fromDateTime-java.util.Date) | Crea un'istanza di [ChartYValue](../../com.aspose.words/chartyvalue/) del tipo [ChartYValueType.DATE\_TIME](../../com.aspose.words/chartyvaluetype/\#DATE-TIME). |
| [fromDouble(double value)](#fromDouble-double) | Crea un'istanza di [ChartYValue](../../com.aspose.words/chartyvalue/) del tipo [ChartYValueType.DOUBLE](../../com.aspose.words/chartyvaluetype/\#DOUBLE). |
| [fromTimeSpan(long value)](#fromTimeSpan-long) | Crea un'istanza di [ChartYValue](../../com.aspose.words/chartyvalue/) del tipo [ChartYValueType.TIME](../../com.aspose.words/chartyvaluetype/\#TIME). |
| [getDateTimeValue()](#getDateTimeValue) | Restituisce il valore datetime memorizzato. |
| [getDoubleValue()](#getDoubleValue) | Restituisce il valore numerico memorizzato. |
| [getTimeValue()](#getTimeValue) | Restituisce il valore temporale memorizzato. |
| [getValueType()](#getValueType) | Restituisce il tipo del valore Y memorizzato nell'oggetto. |
| [hashCode()](#hashCode) |  |
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Restituisce un flag che indica se l'oggetto specificato è uguale all'oggetto valore Y corrente.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### fromDateTime(Date value) {#fromDateTime-java.util.Date}
```
public static ChartYValue fromDateTime(Date value)
```


Crea un'istanza di [ChartYValue](../../com.aspose.words/chartyvalue/) del tipo [ChartYValueType.DATE\_TIME](../../com.aspose.words/chartyvaluetype/\#DATE-TIME).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.util.Date |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/)
### fromDouble(double value) {#fromDouble-double}
```
public static ChartYValue fromDouble(double value)
```


Crea un'istanza di [ChartYValue](../../com.aspose.words/chartyvalue/) del tipo [ChartYValueType.DOUBLE](../../com.aspose.words/chartyvaluetype/\#DOUBLE).

 **Examples:** 

Mostra come popolare le serie del grafico con i dati.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/)
### fromTimeSpan(long value) {#fromTimeSpan-long}
```
public static ChartYValue fromTimeSpan(long value)
```


Crea un'istanza di [ChartYValue](../../com.aspose.words/chartyvalue/) del tipo [ChartYValueType.TIME](../../com.aspose.words/chartyvaluetype/\#TIME).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | long |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/)
### getDateTimeValue() {#getDateTimeValue}
```
public Date getDateTimeValue()
```


Restituisce il valore datetime memorizzato.

**Returns:**
java.util.Date - Il valore data/ora memorizzato.
### getDoubleValue() {#getDoubleValue}
```
public double getDoubleValue()
```


Restituisce il valore numerico memorizzato.

**Returns:**
double - Il valore numerico memorizzato.
### getTimeValue() {#getTimeValue}
```
public long getTimeValue()
```


Restituisce il valore temporale memorizzato.

**Returns:**
long - Il valore temporale memorizzato.
### getValueType() {#getValueType}
```
public int getValueType()
```


Restituisce il tipo del valore Y memorizzato nell'oggetto.

**Returns:**
int - Il tipo del valore Y memorizzato nell'oggetto. Il valore restituito è una delle costanti [ChartYValueType](../../com.aspose.words/chartyvaluetype/).
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
