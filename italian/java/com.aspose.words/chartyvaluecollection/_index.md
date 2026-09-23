---
title: "ChartYValueCollection"
linktitle: "ChartYValueCollection"
second_title: "Aspose.Words per Java"
description: "Rappresenta una raccolta di valori Y per una serie di grafico in Java."
type: docs
weight: 98
url: /it/java/com.aspose.words/chartyvaluecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartYValueCollection implements Iterable
```

Rappresenta una raccolta di valori Y per una serie di grafico.

 **Remarks:** 

Tutti gli elementi della raccolta, diversi da **null**, devono avere lo stesso [ChartYValue.getValueType()](../../com.aspose.words/chartyvalue/\#getValueType).

La raccolta consente solo di modificare i valori Y. Per aggiungere o inserire nuovi valori in una serie di grafico, o rimuovere valori, è possibile utilizzare i metodi appropriati della classe [ChartSeries](../../com.aspose.words/chartseries/).

 **Examples:** 

Mostra come ottenere i dati della serie di grafico.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder();

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries series = chart.getSeries().get(0);

 double minValue = Double.MAX_VALUE;
 int minValueIndex = 0;
 double maxValue = -Double.MAX_VALUE;
 int maxValueIndex = 0;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     // Clear individual format of all data points.
     // Data points and data values are one-to-one in column charts.
     series.getDataPoints().get(i).clearFormat();

     // Get Y value.
     double yValue = series.getYValues().get(i).getDoubleValue();

     if (yValue < minValue)
     {
         minValue = yValue;
         minValueIndex = i;
     }

     if (yValue > maxValue)
     {
         maxValue = yValue;
         maxValueIndex = i;
     }
 }

 // Change colors of the max and min values.
 series.getDataPoints().get(minValueIndex).getFormat().getFill().setForeColor(Color.RED);
 series.getDataPoints().get(maxValueIndex).getFormat().getFill().setForeColor(Color.GREEN);

 doc.save(getArtifactsDir() + "Charts.GetChartSeriesData.docx");
 
```
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get(int index)](#get-int) | Restituisce il valore Y all'indice specificato. |
| [getCount()](#getCount) | Restituisce il numero di elementi in questa raccolta. |
| [getFormatCode()](#getFormatCode) | Restituisce il codice di formato applicato ai valori Y. |
| [iterator()](#iterator) | Restituisce un oggetto enumeratore. |
| [set(int index, ChartYValue value)](#set-int-com.aspose.words.ChartYValue) | Imposta il valore Y all'indice specificato. |
| [setFormatCode(String value)](#setFormatCode-java.lang.String) | Imposta il codice di formato applicato ai valori Y. |
### get(int index) {#get-int}
```
public ChartYValue get(int index)
```


Restituisce il valore Y all'indice specificato.

 **Remarks:** 

I valori vuoti sono rappresentati come **null**.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/) - The Y value at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Restituisce il numero di elementi in questa raccolta.

**Returns:**
int - Il numero di elementi in questa raccolta.
### getFormatCode() {#getFormatCode}
```
public String getFormatCode()
```


Restituisce il codice di formato applicato ai valori Y.

 **Remarks:** 

La formattazione dei numeri è usata per modificare il modo in cui i valori appaiono nel grafico. Esempi di formati numerici:

Numero - "\#,\#\#0.00"

Valuta - "\\"$\\"\#,\#\#0.00"

Ora - "[$-x-systime]h:mm:ss AM/PM"

Data - "d/mm/yyyy"

Percentuale - "0.00%"

Frazione - "\# ?/?"

Scientifico - "0.00E+00"

Contabilità - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

Personalizzato con colore - "[Red]-\#,\#\#0.0"

 **Examples:** 

Mostra come lavorare con il codice di formato dei dati del grafico.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Bubble chart.
 Shape shape = builder.insertChart(ChartType.BUBBLE, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();

 ChartSeries series = chart.getSeries().add(
         "Series1",
         new double[] { 1.0, 1.9, 2.45, 3.0 },
         new double[] { 1.0, -0.9, 1.82, 0.0 },
         new double[] { 2.0, 1.1, 2.95, 2.0 });

 // Show data labels.
 series.hasDataLabels(true);
 series.getDataLabels().setShowCategoryName(true);
 series.getDataLabels().setShowValue(true);
 series.getDataLabels().setShowBubbleSize(true);

 // Set data format codes.
 series.getXValues().setFormatCode("#,##0.0#");
 series.getYValues().setFormatCode("#,##0.0#;[Red]\\-#,##0.0#");
 series.getBubbleSizes().setFormatCode("#,##0.0#");

 doc.save(getArtifactsDir() + "Charts.FormatCode.docx");
 
```

**Returns:**
java.lang.String - Il codice di formato applicato ai valori Y.
### iterator() {#iterator}
```
public Iterator iterator()
```


Restituisce un oggetto enumeratore.

**Returns:**
java.util.Iterator
### set(int index, ChartYValue value) {#set-int-com.aspose.words.ChartYValue}
```
public void set(int index, ChartYValue value)
```


Imposta il valore Y all'indice specificato.

 **Remarks:** 

I valori vuoti sono rappresentati come **null**.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int |  |
| value | [ChartYValue](../../com.aspose.words/chartyvalue/) | Il valore Y all'indice specificato. |

### setFormatCode(String value) {#setFormatCode-java.lang.String}
```
public void setFormatCode(String value)
```


Imposta il codice di formato applicato ai valori Y.

 **Remarks:** 

La formattazione dei numeri è usata per modificare il modo in cui i valori appaiono nel grafico. Esempi di formati numerici:

Numero - "\#,\#\#0.00"

Valuta - "\\"$\\"\#,\#\#0.00"

Ora - "[$-x-systime]h:mm:ss AM/PM"

Data - "d/mm/yyyy"

Percentuale - "0.00%"

Frazione - "\# ?/?"

Scientifico - "0.00E+00"

Contabilità - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

Personalizzato con colore - "[Red]-\#,\#\#0.0"

 **Examples:** 

Mostra come lavorare con il codice di formato dei dati del grafico.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Bubble chart.
 Shape shape = builder.insertChart(ChartType.BUBBLE, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();

 ChartSeries series = chart.getSeries().add(
         "Series1",
         new double[] { 1.0, 1.9, 2.45, 3.0 },
         new double[] { 1.0, -0.9, 1.82, 0.0 },
         new double[] { 2.0, 1.1, 2.95, 2.0 });

 // Show data labels.
 series.hasDataLabels(true);
 series.getDataLabels().setShowCategoryName(true);
 series.getDataLabels().setShowValue(true);
 series.getDataLabels().setShowBubbleSize(true);

 // Set data format codes.
 series.getXValues().setFormatCode("#,##0.0#");
 series.getYValues().setFormatCode("#,##0.0#;[Red]\\-#,##0.0#");
 series.getBubbleSizes().setFormatCode("#,##0.0#");

 doc.save(getArtifactsDir() + "Charts.FormatCode.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il codice di formato applicato ai valori Y. |

