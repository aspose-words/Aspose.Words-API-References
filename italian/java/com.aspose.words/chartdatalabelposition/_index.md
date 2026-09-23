---
title: "ChartDataLabelPosition"
linktitle: "ChartDataLabelPosition"
second_title: "Aspose.Words per Java"
description: "Specifica la posizione per un'etichetta dati del grafico in Java."
type: docs
weight: 74
url: /it/java/com.aspose.words/chartdatalabelposition/
---

**Inheritance:**
java.lang.Object
```
public class ChartDataLabelPosition
```

Specifica la posizione per un'etichetta dati del grafico.

 **Remarks:** 

Non tutti i tipi di serie consentono di specificare le posizioni delle etichette. E quelli che lo consentono, non supportano tutti i valori.

 **Examples:** 

Mostra come impostare la posizione dell'etichetta dei dati.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [ABOVE](#ABOVE) | Specifica che un'etichetta dati deve essere visualizzata sopra un marcatore dati. |
| [BELOW](#BELOW) | Specifica che un'etichetta dati deve essere visualizzata sotto un marcatore dati. |
| [BEST_FIT](#BEST-FIT) | Specifica che un'etichetta dati deve essere visualizzata nella posizione più appropriata. |
| [CENTER](#CENTER) | Specifica che un'etichetta dati deve essere visualizzata centrata su un marcatore dati. |
| [INSIDE_BASE](#INSIDE-BASE) | Specifica che un'etichetta dati deve essere visualizzata all'interno della base di un marcatore dati. |
| [INSIDE_END](#INSIDE-END) | Specifica che un'etichetta dati deve essere visualizzata all'interno dell'estremità di un marcatore dati. |
| [LEFT](#LEFT) | Specifica che un'etichetta dati deve essere visualizzata a sinistra di un marcatore dati. |
| [OUTSIDE_END](#OUTSIDE-END) | Specifica che un'etichetta dati deve essere visualizzata all'esterno dell'estremità di un marcatore dati. |
| [RIGHT](#RIGHT) | Specifica che un'etichetta dati deve essere visualizzata a destra di un marcatore dati. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String chartDataLabelPositionName)](#fromName-java.lang.String) |  |
| [getName(int chartDataLabelPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartDataLabelPosition)](#toString-int) |  |
### ABOVE {#ABOVE}
```
public static int ABOVE
```


Specifica che un'etichetta dati deve essere visualizzata sopra un marcatore dati.

### BELOW {#BELOW}
```
public static int BELOW
```


Specifica che un'etichetta dati deve essere visualizzata sotto un marcatore dati.

### BEST_FIT {#BEST-FIT}
```
public static int BEST_FIT
```


Specifica che un'etichetta dati deve essere visualizzata nella posizione più appropriata.

### CENTER {#CENTER}
```
public static int CENTER
```


Specifica che un'etichetta dati deve essere visualizzata centrata su un marcatore dati.

### INSIDE_BASE {#INSIDE-BASE}
```
public static int INSIDE_BASE
```


Specifica che un'etichetta dati deve essere visualizzata all'interno della base di un marcatore dati.

### INSIDE_END {#INSIDE-END}
```
public static int INSIDE_END
```


Specifica che un'etichetta dati deve essere visualizzata all'interno dell'estremità di un marcatore dati.

### LEFT {#LEFT}
```
public static int LEFT
```


Specifica che un'etichetta dati deve essere visualizzata a sinistra di un marcatore dati.

### OUTSIDE_END {#OUTSIDE-END}
```
public static int OUTSIDE_END
```


Specifica che un'etichetta dati deve essere visualizzata all'esterno dell'estremità di un marcatore dati.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Specifica che un'etichetta dati deve essere visualizzata a destra di un marcatore dati.

### length {#length}
```
public static int length
```


### fromName(String chartDataLabelPositionName) {#fromName-java.lang.String}
```
public static int fromName(String chartDataLabelPositionName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| chartDataLabelPositionName | java.lang.String |  |

**Returns:**
int
### getName(int chartDataLabelPosition) {#getName-int}
```
public static String getName(int chartDataLabelPosition)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| chartDataLabelPosition | int |  |

**Returns:**
java.lang.String
