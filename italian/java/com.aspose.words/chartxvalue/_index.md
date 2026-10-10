---
title: "ChartXValue"
linktitle: "ChartXValue"
second_title: "Aspose.Words per Java"
description: "Rappresenta un valore X per una serie di grafico in Java."
type: docs
weight: 94
url: /it/java/com.aspose.words/chartxvalue/
---

**Inheritance:**
java.lang.Object
```
public class ChartXValue
```

Rappresenta un valore X per una serie di grafico.

 **Remarks:** 

Questa classe contiene numerosi metodi statici per creare un valore X di un tipo particolare. La proprietà [getValueType()](../../com.aspose.words/chartxvalue/\#getValueType) consente di determinare il tipo di un valore X esistente.

Tutti i valori X non nulli di una serie di grafico devono essere dello stesso tipo [ChartXValueType](../../com.aspose.words/chartxvaluetype/).

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Restituisce un flag che indica se l'oggetto specificato è uguale all'oggetto valore X corrente. |
| [fromDateTime(Date value)](#fromDateTime-java.util.Date) | Crea un'istanza di [ChartXValue](../../com.aspose.words/chartxvalue/) del tipo [ChartXValueType.DATE\_TIME](../../com.aspose.words/chartxvaluetype/\#DATE-TIME). |
| [fromDouble(double value)](#fromDouble-double) | Crea un'istanza di [ChartXValue](../../com.aspose.words/chartxvalue/) del tipo [ChartXValueType.DOUBLE](../../com.aspose.words/chartxvaluetype/\#DOUBLE). |
| [fromMultilevelValue(ChartMultilevelValue value)](#fromMultilevelValue-com.aspose.words.ChartMultilevelValue) | Crea un'istanza di [ChartXValue](../../com.aspose.words/chartxvalue/) del tipo [ChartXValueType.MULTILEVEL](../../com.aspose.words/chartxvaluetype/\#MULTILEVEL). |
| [fromString(String value)](#fromString-java.lang.String) | Crea un'istanza di [ChartXValue](../../com.aspose.words/chartxvalue/) del tipo [ChartXValueType.STRING](../../com.aspose.words/chartxvaluetype/\#STRING). |
| [fromTimeSpan(long value)](#fromTimeSpan-long) | Crea un'istanza di [ChartXValue](../../com.aspose.words/chartxvalue/) del tipo [ChartXValueType.TIME](../../com.aspose.words/chartxvaluetype/\#TIME). |
| [getDateTimeValue()](#getDateTimeValue) | Restituisce il valore datetime memorizzato. |
| [getDoubleValue()](#getDoubleValue) | Restituisce il valore numerico memorizzato. |
| [getMultilevelValue()](#getMultilevelValue) | Restituisce il valore multilevel memorizzato. |
| [getStringValue()](#getStringValue) | Restituisce il valore stringa memorizzato. |
| [getTimeValue()](#getTimeValue) | Restituisce il valore temporale memorizzato. |
| [getValueType()](#getValueType) | Restituisce il tipo del valore X memorizzato nell'oggetto. |
| [hashCode()](#hashCode) |  |
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Restituisce un flag che indica se l'oggetto specificato è uguale all'oggetto valore X corrente.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### fromDateTime(Date value) {#fromDateTime-java.util.Date}
```
public static ChartXValue fromDateTime(Date value)
```


Crea un'istanza di [ChartXValue](../../com.aspose.words/chartxvalue/) del tipo [ChartXValueType.DATE\_TIME](../../com.aspose.words/chartxvaluetype/\#DATE-TIME).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.util.Date |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromDouble(double value) {#fromDouble-double}
```
public static ChartXValue fromDouble(double value)
```


Crea un'istanza di [ChartXValue](../../com.aspose.words/chartxvalue/) del tipo [ChartXValueType.DOUBLE](../../com.aspose.words/chartxvaluetype/\#DOUBLE).

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
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromMultilevelValue(ChartMultilevelValue value) {#fromMultilevelValue-com.aspose.words.ChartMultilevelValue}
```
public static ChartXValue fromMultilevelValue(ChartMultilevelValue value)
```


Crea un'istanza di [ChartXValue](../../com.aspose.words/chartxvalue/) del tipo [ChartXValueType.MULTILEVEL](../../com.aspose.words/chartxvaluetype/\#MULTILEVEL).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | [ChartMultilevelValue](../../com.aspose.words/chartmultilevelvalue/) |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromString(String value) {#fromString-java.lang.String}
```
public static ChartXValue fromString(String value)
```


Crea un'istanza di [ChartXValue](../../com.aspose.words/chartxvalue/) del tipo [ChartXValueType.STRING](../../com.aspose.words/chartxvaluetype/\#STRING).

 **Examples:** 

Mostra come aggiungere/rimuovere i valori dei dati del grafico.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromTimeSpan(long value) {#fromTimeSpan-long}
```
public static ChartXValue fromTimeSpan(long value)
```


Crea un'istanza di [ChartXValue](../../com.aspose.words/chartxvalue/) del tipo [ChartXValueType.TIME](../../com.aspose.words/chartxvaluetype/\#TIME).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | long |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
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
### getMultilevelValue() {#getMultilevelValue}
```
public ChartMultilevelValue getMultilevelValue()
```


Restituisce il valore multilevel memorizzato.

**Returns:**
[ChartMultilevelValue](../../com.aspose.words/chartmultilevelvalue/) - The stored multilevel value.
### getStringValue() {#getStringValue}
```
public String getStringValue()
```


Restituisce il valore stringa memorizzato.

**Returns:**
java.lang.String - Il valore stringa memorizzato.
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


Restituisce il tipo del valore X memorizzato nell'oggetto.

**Returns:**
int - Il tipo del valore X memorizzato nell'oggetto. Il valore restituito è una delle costanti [ChartXValueType](../../com.aspose.words/chartxvaluetype/) .
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
