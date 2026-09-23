---
title: "BubbleSizeCollection"
linktitle: "BubbleSizeCollection"
second_title: "Aspose.Words per Java"
description: "Rappresenta una raccolta di dimensioni delle bolle per una serie di grafico in Java."
type: docs
weight: 50
url: /it/java/com.aspose.words/bubblesizecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class BubbleSizeCollection implements Iterable
```

Rappresenta una raccolta di dimensioni delle bolle per una serie di grafico.

 **Remarks:** 

La raccolta consente solo di modificare le dimensioni delle bolle. Per aggiungere o inserire nuovi valori a una serie di grafico, o rimuovere valori, è possibile utilizzare i metodi appropriati della classe [ChartSeries](../../com.aspose.words/chartseries/).

I valori vuoti delle dimensioni delle bolle sono rappresentati come double\#NA\_N.NA\_N.
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get(int index)](#get-int) | Ottiene il valore della dimensione della bolla all'indice specificato. |
| [getCount()](#getCount) | Restituisce il numero di elementi in questa raccolta. |
| [getFormatCode()](#getFormatCode) | Ottiene il codice di formato applicato alle dimensioni delle bolle. |
| [iterator()](#iterator) | Restituisce un oggetto enumeratore. |
| [set(int index, double value)](#set-int-double) | Imposta il valore della dimensione della bolla all'indice specificato. |
| [setFormatCode(String value)](#setFormatCode-java.lang.String) | Imposta il codice di formato applicato alle dimensioni delle bolle. |
### get(int index) {#get-int}
```
public double get(int index)
```


Ottiene il valore della dimensione della bolla all'indice specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int |  |

**Returns:**
double - Il valore della dimensione della bolla all'indice specificato.
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


Ottiene il codice di formato applicato alle dimensioni delle bolle.

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
java.lang.String - Il codice di formato applicato alle dimensioni delle bolle.
### iterator() {#iterator}
```
public Iterator iterator()
```


Restituisce un oggetto enumeratore.

**Returns:**
java.util.Iterator
### set(int index, double value) {#set-int-double}
```
public void set(int index, double value)
```


Imposta il valore della dimensione della bolla all'indice specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int |  |
| valore | double | Il valore della dimensione della bolla all'indice specificato. |

### setFormatCode(String value) {#setFormatCode-java.lang.String}
```
public void setFormatCode(String value)
```


Imposta il codice di formato applicato alle dimensioni delle bolle.

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
| valore | java.lang.String | Il codice di formato applicato alle dimensioni delle bolle. |

