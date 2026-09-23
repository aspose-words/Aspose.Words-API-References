---
title: "ChartDataLabelCollection"
linktitle: "ChartDataLabelCollection"
second_title: "Aspose.Words per Java"
description: "Rappresenta una collezione di ChartDataLabel in Java."
type: docs
weight: 72
url: /it/java/com.aspose.words/chartdatalabelcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartDataLabelCollection implements Iterable
```

Rappresenta una collezione di [ChartDataLabel](../../com.aspose.words/chartdatalabel/).

Per saperne di più, visita l'articolo di documentazione [ Working with Charts ][Working with Charts].

 **Examples:** 

Mostra come applicare etichette ai punti dati in un grafico a linee.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [clearFormat()](#clearFormat) | Cancella il formato di tutti i [ChartDataLabel](../../com.aspose.words/chartdatalabel/) in questa collezione. |
| [get(int index)](#get-int) | Restituisce [ChartDataLabel](../../com.aspose.words/chartdatalabel/) per l'indice specificato. |
| [getCount()](#getCount) | Restituisce il numero di [ChartDataLabel](../../com.aspose.words/chartdatalabel/) in questa collezione. |
| [getFont()](#getFont) | Fornisce l'accesso alla formattazione del carattere delle etichette dati dell'intera serie. |
| [getFormat()](#getFormat) | Fornisce l'accesso alla formattazione di riempimento e linea delle etichette dati. |
| [getNumberFormat()](#getNumberFormat) | Ottiene un'istanza di [ChartNumberFormat](../../com.aspose.words/chartnumberformat/) che consente di impostare il formato numerico per le etichette dati dell'intera serie. |
| [getOrientation()](#getOrientation) | Ottiene l'orientamento del testo delle etichette dati dell'intera serie. |
| [getPosition()](#getPosition) | Ottiene la posizione delle etichette dati. |
| [getRotation()](#getRotation) | Ottiene la rotazione delle etichette dati dell'intera serie in gradi. |
| [getSeparator()](#getSeparator) | Ottiene il separatore di stringa usato per le etichette dati dell'intera serie. |
| [getShapeType()](#getShapeType) |  |
| [getShowBubbleSize()](#getShowBubbleSize) | Consente di specificare se visualizzare la dimensione della bolla per le etichette dati dell'intera serie. |
| [getShowCategoryName()](#getShowCategoryName) | Consente di specificare se visualizzare il nome della categoria per le etichette dati dell'intera serie. |
| [getShowDataLabelsRange()](#getShowDataLabelsRange) | Consente di specificare se visualizzare i valori dell'intervallo delle etichette dati nelle etichette dati dell'intera serie. |
| [getShowLeaderLines()](#getShowLeaderLines) | Consente di specificare se le linee guida dell'etichetta dati devono essere mostrate per le etichette dati dell'intera serie. |
| [getShowLegendKey()](#getShowLegendKey) | Consente di specificare se visualizzare la chiave della legenda per le etichette dati dell'intera serie. |
| [getShowPercentage()](#getShowPercentage) | Consente di specificare se visualizzare il valore percentuale per le etichette dati dell'intera serie. |
| [getShowSeriesName()](#getShowSeriesName) | Ottiene un valore Booleano per indicare il comportamento di visualizzazione del nome della serie per le etichette dati dell'intera serie. |
| [getShowValue()](#getShowValue) | Consente di specificare se visualizzare i valori nelle etichette dati dell'intera serie. |
| [isFillSupported()](#isFillSupported) |  |
| [isFormatDefined()](#isFormatDefined) |  |
| [isInherited()](#isInherited) |  |
| [iterator()](#iterator) | Restituisce un oggetto enumeratore. |
| [materializeSpPr()](#materializeSpPr) |  |
| [setOrientation(int value)](#setOrientation-int) | Imposta l'orientamento del testo delle etichette dati dell'intera serie. |
| [setPosition(int value)](#setPosition-int) | Imposta la posizione delle etichette dati. |
| [setRotation(int value)](#setRotation-int) | Imposta la rotazione delle etichette dati dell'intera serie in gradi. |
| [setSeparator(String value)](#setSeparator-java.lang.String) | Imposta il separatore di stringa utilizzato per le etichette dati dell'intera serie. |
| [setShapeType(int value)](#setShapeType-int) |  |
| [setShowBubbleSize(boolean value)](#setShowBubbleSize-boolean) | Consente di specificare se visualizzare la dimensione della bolla per le etichette dati dell'intera serie. |
| [setShowCategoryName(boolean value)](#setShowCategoryName-boolean) | Consente di specificare se visualizzare il nome della categoria per le etichette dati dell'intera serie. |
| [setShowDataLabelsRange(boolean value)](#setShowDataLabelsRange-boolean) | Consente di specificare se visualizzare i valori dell'intervallo delle etichette dati nelle etichette dati dell'intera serie. |
| [setShowLeaderLines(boolean value)](#setShowLeaderLines-boolean) | Consente di specificare se le linee guida dell'etichetta dati devono essere mostrate per le etichette dati dell'intera serie. |
| [setShowLegendKey(boolean value)](#setShowLegendKey-boolean) | Consente di specificare se visualizzare la chiave della legenda per le etichette dati dell'intera serie. |
| [setShowPercentage(boolean value)](#setShowPercentage-boolean) | Consente di specificare se visualizzare il valore percentuale per le etichette dati dell'intera serie. |
| [setShowSeriesName(boolean value)](#setShowSeriesName-boolean) | Imposta un valore Booleano per indicare il comportamento di visualizzazione del nome della serie per le etichette dati dell'intera serie. |
| [setShowValue(boolean value)](#setShowValue-boolean) | Consente di specificare se visualizzare i valori nelle etichette dati dell'intera serie. |
### clearFormat() {#clearFormat}
```
public void clearFormat()
```


Cancella il formato di tutti i [ChartDataLabel](../../com.aspose.words/chartdatalabel/) in questa collezione.

 **Examples:** 

Mostra come applicare etichette ai punti dati in un grafico a linee.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

### get(int index) {#get-int}
```
public ChartDataLabel get(int index)
```


Restituisce [ChartDataLabel](../../com.aspose.words/chartdatalabel/) per l'indice specificato.

 **Examples:** 

Mostra come applicare etichette ai punti dati in un grafico a linee.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int |  |

**Returns:**
[ChartDataLabel](../../com.aspose.words/chartdatalabel/) - [ChartDataLabel](../../com.aspose.words/chartdatalabel/) for the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Restituisce il numero di [ChartDataLabel](../../com.aspose.words/chartdatalabel/) in questa collezione.

 **Examples:** 

Mostra come applicare etichette ai punti dati in un grafico a linee.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Returns:**
int - Il numero di [ChartDataLabel](../../com.aspose.words/chartdatalabel/) in questa collezione.
### getFont() {#getFont}
```
public Font getFont()
```


Fornisce l'accesso alla formattazione del carattere delle etichette dati dell'intera serie.

 **Remarks:** 

Il valore definito per questa proprietà può essere sovrascritto per un'etichetta dati individuale utilizzando la proprietà [ChartDataLabel.getFont()](../../com.aspose.words/chartdatalabel/\#getFont).

 **Examples:** 

Mostra come abilitare e configurare le etichette dei dati per una serie di grafico.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a line chart, then clear its demo data series to start with a clean chart,
 // and then set a title.
 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();
 chart.getSeries().clear();
 chart.getTitle().setText("Monthly sales report");

 // Insert a custom chart series with months as categories for the X-axis,
 // and respective decimal amounts for the Y-axis.
 ChartSeries series = chart.getSeries().add("Revenue",
         new String[]{"January", "February", "March"},
         new double[]{25.611d, 21.439d, 33.750d});

 // Enable data labels, and then apply a custom number format for values displayed in the data labels.
 // This format will treat displayed decimal values as millions of US Dollars.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.getNumberFormat().setFormatCode("\"US$\" #,##0.000\"M\"");
 dataLabels.getFont().setSize(12.0);

 doc.save(getArtifactsDir() + "Charts.DataLabelNumberFormat.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getFormat() {#getFormat}
```
public ChartFormat getFormat()
```


Fornisce l'accesso alla formattazione di riempimento e linea delle etichette dati.

 **Examples:** 

Mostra come impostare il riempimento, il tratto e la formattazione delle note a margine per le etichette dei dati del grafico.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();

 // Add new series.
 ChartSeries series = chart.getSeries().add("AW Series 1",
         new String[] { "AW Category 1", "AW Category 2", "AW Category 3", "AW Category 4" },
         new double[] { 100.0, 200.0, 300.0, 400.0 });

 // Show data labels.
 series.hasDataLabels(true);
 series.getDataLabels().setShowValue(true);

 // Format data labels as callouts.
 ChartFormat format = series.getDataLabels().getFormat();
 format.setShapeType(ChartShapeType.WEDGE_RECT_CALLOUT);
 format.getStroke().setColor(Color.lightGray);
 format.getFill().solid(Color.GREEN);
 series.getDataLabels().getFont().setColor(Color.YELLOW);

 // Change fill and stroke of an individual data label.
 ChartFormat labelFormat = series.getDataLabels().get(0).getFormat();
 labelFormat.getStroke().setColor(Color.BLUE);
 labelFormat.getFill().solid(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.FormatDataLables.docx");
 
```

**Returns:**
[ChartFormat](../../com.aspose.words/chartformat/) - The corresponding [ChartFormat](../../com.aspose.words/chartformat/) value.
### getNumberFormat() {#getNumberFormat}
```
public ChartNumberFormat getNumberFormat()
```


Ottiene un'istanza di [ChartNumberFormat](../../com.aspose.words/chartnumberformat/) che consente di impostare il formato numerico per le etichette dati dell'intera serie.

 **Examples:** 

Mostra come abilitare e configurare le etichette dei dati per una serie di grafico.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a line chart, then clear its demo data series to start with a clean chart,
 // and then set a title.
 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();
 chart.getSeries().clear();
 chart.getTitle().setText("Monthly sales report");

 // Insert a custom chart series with months as categories for the X-axis,
 // and respective decimal amounts for the Y-axis.
 ChartSeries series = chart.getSeries().add("Revenue",
         new String[]{"January", "February", "March"},
         new double[]{25.611d, 21.439d, 33.750d});

 // Enable data labels, and then apply a custom number format for values displayed in the data labels.
 // This format will treat displayed decimal values as millions of US Dollars.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.getNumberFormat().setFormatCode("\"US$\" #,##0.000\"M\"");
 dataLabels.getFont().setSize(12.0);

 doc.save(getArtifactsDir() + "Charts.DataLabelNumberFormat.docx");
 
```

**Returns:**
[ChartNumberFormat](../../com.aspose.words/chartnumberformat/) - An [ChartNumberFormat](../../com.aspose.words/chartnumberformat/) instance allowing to set number format for the data labels of the entire series.
### getOrientation() {#getOrientation}
```
public int getOrientation()
```


Ottiene l'orientamento del testo delle etichette dati dell'intera serie.

 **Remarks:** 

Il valore predefinito è [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL).

 **Examples:** 

Mostra come modificare l'orientamento e la rotazione delle etichette dati.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 ChartSeries series = shape.getChart().getSeries().get(0);
 ChartDataLabelCollection dataLabels = series.getDataLabels();

 // Show data labels.
 series.hasDataLabels(true);
 dataLabels.setShowValue(true);
 dataLabels.setShowCategoryName(true);

 // Define data label shape.
 dataLabels.getFormat().setShapeType(ChartShapeType.UP_ARROW);
 dataLabels.getFormat().getStroke().getFill().solid(Color.blue);

 // Set data label orientation and rotation for the entire series.
 dataLabels.setOrientation(ShapeTextOrientation.VERTICAL_FAR_EAST);
 dataLabels.setRotation(-45);

 // Change orientation and rotation of the first data label.
 dataLabels.get(0).setOrientation(ShapeTextOrientation.HORIZONTAL);
 dataLabels.get(0).setRotation(45);

 doc.save(getArtifactsDir() + "Charts.LabelOrientationRotation.docx");
 
```

**Returns:**
int - L'orientamento del testo delle etichette dati dell'intera serie. Il valore restituito è una delle costanti di [ShapeTextOrientation](../../com.aspose.words/shapetextorientation/).
### getPosition() {#getPosition}
```
public int getPosition()
```


Ottiene la posizione delle etichette dati.

 **Remarks:** 

La posizione può essere impostata per le etichette dati dei seguenti tipi di serie di grafico:

\- [ChartSeriesType.BAR](../../com.aspose.words/chartseriestype/\#BAR), [ChartSeriesType.COLUMN](../../com.aspose.words/chartseriestype/\#COLUMN), [ChartSeriesType.HISTOGRAM](../../com.aspose.words/chartseriestype/\#HISTOGRAM), [ChartSeriesType.PARETO](../../com.aspose.words/chartseriestype/\#PARETO), [ChartSeriesType.WATERFALL](../../com.aspose.words/chartseriestype/\#WATERFALL); valori consentiti: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END) e [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END);

\- [ChartSeriesType.BAR\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-STACKED), [ChartSeriesType.BAR\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-PERCENT-STACKED), [ChartSeriesType.COLUMN\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-STACKED), [ChartSeriesType.COLUMN\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-PERCENT-STACKED); valori consentiti: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE) e [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END);

\- [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE), [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D), [ChartSeriesType.LINE](../../com.aspose.words/chartseriestype/\#LINE), [ChartSeriesType.LINE\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-STACKED), [ChartSeriesType.LINE\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-PERCENT-STACKED), [ChartSeriesType.SCATTER](../../com.aspose.words/chartseriestype/\#SCATTER), [ChartSeriesType.STOCK](../../com.aspose.words/chartseriestype/\#STOCK); valori consentiti: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) e [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW);

- [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D), [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR), [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE); valori consentiti: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END), [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END) e [ChartDataLabelPosition.BEST\_FIT](../../com.aspose.words/chartdatalabelposition/\#BEST-FIT);

- [ChartSeriesType.BOX\_AND\_WHISKER](../../com.aspose.words/chartseriestype/\#BOX-AND-WHISKER); valori consentiti: [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) e [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW).

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

**Returns:**
int - La posizione delle etichette dei dati. Il valore restituito è una delle costanti [ChartDataLabelPosition](../../com.aspose.words/chartdatalabelposition/).
### getRotation() {#getRotation}
```
public int getRotation()
```


Ottiene la rotazione delle etichette dati dell'intera serie in gradi.

 **Remarks:** 

L'intervallo dei valori accettabili è da -180 a 180 inclusi. Il valore predefinito è 0.

Se il valore [getOrientation()](../../com.aspose.words/chartdatalabelcollection/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/chartdatalabelcollection/\#setOrientation-int) è [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL), le forme delle etichette, se esistono, vengono ruotate insieme al testo dell'etichetta. Altrimenti, solo il testo dell'etichetta viene ruotato.

 **Examples:** 

Mostra come modificare l'orientamento e la rotazione delle etichette dati.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 ChartSeries series = shape.getChart().getSeries().get(0);
 ChartDataLabelCollection dataLabels = series.getDataLabels();

 // Show data labels.
 series.hasDataLabels(true);
 dataLabels.setShowValue(true);
 dataLabels.setShowCategoryName(true);

 // Define data label shape.
 dataLabels.getFormat().setShapeType(ChartShapeType.UP_ARROW);
 dataLabels.getFormat().getStroke().getFill().solid(Color.blue);

 // Set data label orientation and rotation for the entire series.
 dataLabels.setOrientation(ShapeTextOrientation.VERTICAL_FAR_EAST);
 dataLabels.setRotation(-45);

 // Change orientation and rotation of the first data label.
 dataLabels.get(0).setOrientation(ShapeTextOrientation.HORIZONTAL);
 dataLabels.get(0).setRotation(45);

 doc.save(getArtifactsDir() + "Charts.LabelOrientationRotation.docx");
 
```

**Returns:**
int - La rotazione delle etichette dei dati dell'intera serie in gradi.
### getSeparator() {#getSeparator}
```
public String getSeparator()
```


Restituisce il separatore di stringa usato per le etichette dei dati dell'intera serie. Il valore predefinito è una virgola, eccetto per i grafici a torta che mostrano solo il nome della categoria e la percentuale, quando invece deve essere usata un'interruzione di riga.

 **Remarks:** 

Il valore definito per questa proprietà può essere sovrascritto per un'etichetta dati individuale utilizzando la proprietà [ChartDataLabel.getSeparator()](../../com.aspose.words/chartdatalabel/\#getSeparator) / [ChartDataLabel.setSeparator(java.lang.String)](../../com.aspose.words/chartdatalabel/\#setSeparator-java.lang.String).

 **Examples:** 

Mostra come lavorare con le etichette dei dati di un grafico a bolle.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

Mostra come lavorare con le etichette dei dati di un grafico a torta.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Returns:**
java.lang.String - Separatore di stringa usato per le etichette dei dati dell'intera serie.
### getShapeType() {#getShapeType}
```
public int getShapeType()
```




**Returns:**
int
### getShowBubbleSize() {#getShowBubbleSize}
```
public boolean getShowBubbleSize()
```


Consente di specificare se la dimensione della bolla deve essere visualizzata per le etichette dei dati dell'intera serie. Si applica solo ai grafici a bolle. Il valore predefinito è false.

 **Remarks:** 

Il valore definito per questa proprietà può essere sovrascritto per un'etichetta dati individuale utilizzando la proprietà [ChartDataLabel.getShowBubbleSize()](../../com.aspose.words/chartdatalabel/\#getShowBubbleSize) / [ChartDataLabel.setShowBubbleSize(boolean)](../../com.aspose.words/chartdatalabel/\#setShowBubbleSize-boolean).

 **Examples:** 

Mostra come lavorare con le etichette dei dati di un grafico a bolle.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getShowCategoryName() {#getShowCategoryName}
```
public boolean getShowCategoryName()
```


Consente di specificare se il nome della categoria deve essere visualizzato per le etichette dei dati dell'intera serie. Il valore predefinito è false.

 **Remarks:** 

Il valore definito per questa proprietà può essere sovrascritto per un'etichetta dati individuale utilizzando la proprietà [ChartDataLabel.getShowCategoryName()](../../com.aspose.words/chartdatalabel/\#getShowCategoryName) / [ChartDataLabel.setShowCategoryName(boolean)](../../com.aspose.words/chartdatalabel/\#setShowCategoryName-boolean).

 **Examples:** 

Mostra come lavorare con le etichette dei dati di un grafico a bolle.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getShowDataLabelsRange() {#getShowDataLabelsRange}
```
public boolean getShowDataLabelsRange()
```


Consente di specificare se i valori dell'intervallo delle etichette dei dati devono essere visualizzati nelle etichette dei dati dell'intera serie. Il valore predefinito è false.

 **Remarks:** 

Il valore definito per questa proprietà può essere sovrascritto per un'etichetta dati individuale utilizzando la proprietà [ChartDataLabel.getShowDataLabelsRange()](../../com.aspose.words/chartdatalabel/\#getShowDataLabelsRange) / [ChartDataLabel.setShowDataLabelsRange(boolean)](../../com.aspose.words/chartdatalabel/\#setShowDataLabelsRange-boolean).

 **Examples:** 

Mostra come applicare etichette ai punti dati in un grafico a linee.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getShowLeaderLines() {#getShowLeaderLines}
```
public boolean getShowLeaderLines()
```


Consente di specificare se le linee guida delle etichette dati devono essere visualizzate per le etichette dati dell'intera serie. Il valore predefinito è false.

 **Remarks:** 

Si applica solo ai grafici a torta. Le linee guida creano una connessione visiva tra un'etichetta dati e il relativo punto dati.

Il valore definito per questa proprietà può essere sovrascritto per un'etichetta dati individuale utilizzando la proprietà [ChartDataLabel.getShowLeaderLines()](../../com.aspose.words/chartdatalabel/\#getShowLeaderLines) / [ChartDataLabel.setShowLeaderLines(boolean)](../../com.aspose.words/chartdatalabel/\#setShowLeaderLines-boolean).

 **Examples:** 

Mostra come lavorare con le etichette dei dati di un grafico a torta.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getShowLegendKey() {#getShowLegendKey}
```
public boolean getShowLegendKey()
```


Consente di specificare se la chiave della legenda deve essere visualizzata per le etichette dati dell'intera serie. Il valore predefinito è false.

 **Remarks:** 

Il valore definito per questa proprietà può essere sovrascritto per un'etichetta dati individuale utilizzando la proprietà [ChartDataLabel.getShowLegendKey()](../../com.aspose.words/chartdatalabel/\#getShowLegendKey) / [ChartDataLabel.setShowLegendKey(boolean)](../../com.aspose.words/chartdatalabel/\#setShowLegendKey-boolean).

 **Examples:** 

Mostra come lavorare con le etichette dei dati di un grafico a torta.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getShowPercentage() {#getShowPercentage}
```
public boolean getShowPercentage()
```


Consente di specificare se il valore percentuale deve essere visualizzato per le etichette dati dell'intera serie. Il valore predefinito è false. Si applica solo ai grafici a torta.

 **Remarks:** 

Il valore definito per questa proprietà può essere sovrascritto per un'etichetta dati individuale utilizzando la proprietà [ChartDataLabel.getShowPercentage()](../../com.aspose.words/chartdatalabel/\#getShowPercentage) / [ChartDataLabel.setShowPercentage(boolean)](../../com.aspose.words/chartdatalabel/\#setShowPercentage-boolean).

 **Examples:** 

Mostra come lavorare con le etichette dei dati di un grafico a torta.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getShowSeriesName() {#getShowSeriesName}
```
public boolean getShowSeriesName()
```


Restituisce un Boolean per indicare il comportamento di visualizzazione del nome della serie per le etichette dati dell'intera serie. true per mostrare il nome della serie; false per nasconderlo. Per impostazione predefinita false.

 **Remarks:** 

Il valore definito per questa proprietà può essere sovrascritto per un'etichetta dati individuale utilizzando la proprietà [ChartDataLabel.getShowSeriesName()](../../com.aspose.words/chartdatalabel/\#getShowSeriesName) / [ChartDataLabel.setShowSeriesName(boolean)](../../com.aspose.words/chartdatalabel/\#setShowSeriesName-boolean).

 **Examples:** 

Mostra come lavorare con le etichette dei dati di un grafico a bolle.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

**Returns:**
boolean - Un Boolean per indicare il comportamento di visualizzazione del nome della serie per le etichette dati dell'intera serie.
### getShowValue() {#getShowValue}
```
public boolean getShowValue()
```


Consente di specificare se i valori devono essere visualizzati nelle etichette dati dell'intera serie. Il valore predefinito è false.

 **Remarks:** 

Il valore definito per questa proprietà può essere sovrascritto per un'etichetta dati individuale utilizzando la proprietà [ChartDataLabel.getShowValue()](../../com.aspose.words/chartdatalabel/\#getShowValue) / [ChartDataLabel.setShowValue(boolean)](../../com.aspose.words/chartdatalabel/\#setShowValue-boolean).

 **Examples:** 

Mostra come lavorare con le etichette dei dati di un grafico a torta.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### isFillSupported() {#isFillSupported}
```
public boolean isFillSupported()
```




**Returns:**
boolean
### isFormatDefined() {#isFormatDefined}
```
public boolean isFormatDefined()
```




**Returns:**
boolean
### isInherited() {#isInherited}
```
public boolean isInherited()
```




**Returns:**
boolean
### iterator() {#iterator}
```
public Iterator iterator()
```


Restituisce un oggetto enumeratore.

 **Examples:** 

Mostra come applicare etichette ai punti dati in un grafico a linee.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Returns:**
java.util.Iterator
### materializeSpPr() {#materializeSpPr}
```
public void materializeSpPr()
```




### setOrientation(int value) {#setOrientation-int}
```
public void setOrientation(int value)
```


Imposta l'orientamento del testo delle etichette dati dell'intera serie.

 **Remarks:** 

Il valore predefinito è [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL).

 **Examples:** 

Mostra come modificare l'orientamento e la rotazione delle etichette dati.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 ChartSeries series = shape.getChart().getSeries().get(0);
 ChartDataLabelCollection dataLabels = series.getDataLabels();

 // Show data labels.
 series.hasDataLabels(true);
 dataLabels.setShowValue(true);
 dataLabels.setShowCategoryName(true);

 // Define data label shape.
 dataLabels.getFormat().setShapeType(ChartShapeType.UP_ARROW);
 dataLabels.getFormat().getStroke().getFill().solid(Color.blue);

 // Set data label orientation and rotation for the entire series.
 dataLabels.setOrientation(ShapeTextOrientation.VERTICAL_FAR_EAST);
 dataLabels.setRotation(-45);

 // Change orientation and rotation of the first data label.
 dataLabels.get(0).setOrientation(ShapeTextOrientation.HORIZONTAL);
 dataLabels.get(0).setRotation(45);

 doc.save(getArtifactsDir() + "Charts.LabelOrientationRotation.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | L'orientamento del testo delle etichette dati dell'intera serie. Il valore deve essere una delle costanti [ShapeTextOrientation](../../com.aspose.words/shapetextorientation/). |

### setPosition(int value) {#setPosition-int}
```
public void setPosition(int value)
```


Imposta la posizione delle etichette dati.

 **Remarks:** 

La posizione può essere impostata per le etichette dati dei seguenti tipi di serie di grafico:

\- [ChartSeriesType.BAR](../../com.aspose.words/chartseriestype/\#BAR), [ChartSeriesType.COLUMN](../../com.aspose.words/chartseriestype/\#COLUMN), [ChartSeriesType.HISTOGRAM](../../com.aspose.words/chartseriestype/\#HISTOGRAM), [ChartSeriesType.PARETO](../../com.aspose.words/chartseriestype/\#PARETO), [ChartSeriesType.WATERFALL](../../com.aspose.words/chartseriestype/\#WATERFALL); valori consentiti: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END) e [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END);

\- [ChartSeriesType.BAR\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-STACKED), [ChartSeriesType.BAR\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-PERCENT-STACKED), [ChartSeriesType.COLUMN\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-STACKED), [ChartSeriesType.COLUMN\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-PERCENT-STACKED); valori consentiti: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE) e [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END);

\- [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE), [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D), [ChartSeriesType.LINE](../../com.aspose.words/chartseriestype/\#LINE), [ChartSeriesType.LINE\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-STACKED), [ChartSeriesType.LINE\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-PERCENT-STACKED), [ChartSeriesType.SCATTER](../../com.aspose.words/chartseriestype/\#SCATTER), [ChartSeriesType.STOCK](../../com.aspose.words/chartseriestype/\#STOCK); valori consentiti: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) e [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW);

- [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D), [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR), [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE); valori consentiti: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END), [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END) e [ChartDataLabelPosition.BEST\_FIT](../../com.aspose.words/chartdatalabelposition/\#BEST-FIT);

- [ChartSeriesType.BOX\_AND\_WHISKER](../../com.aspose.words/chartseriestype/\#BOX-AND-WHISKER); valori consentiti: [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) e [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW).

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

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | La posizione delle etichette dati. Il valore deve essere una delle costanti [ChartDataLabelPosition](../../com.aspose.words/chartdatalabelposition/). |

### setRotation(int value) {#setRotation-int}
```
public void setRotation(int value)
```


Imposta la rotazione delle etichette dati dell'intera serie in gradi.

 **Remarks:** 

L'intervallo dei valori accettabili è da -180 a 180 inclusi. Il valore predefinito è 0.

Se il valore [getOrientation()](../../com.aspose.words/chartdatalabelcollection/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/chartdatalabelcollection/\#setOrientation-int) è [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL), le forme delle etichette, se esistono, vengono ruotate insieme al testo dell'etichetta. Altrimenti, solo il testo dell'etichetta viene ruotato.

 **Examples:** 

Mostra come modificare l'orientamento e la rotazione delle etichette dati.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 ChartSeries series = shape.getChart().getSeries().get(0);
 ChartDataLabelCollection dataLabels = series.getDataLabels();

 // Show data labels.
 series.hasDataLabels(true);
 dataLabels.setShowValue(true);
 dataLabels.setShowCategoryName(true);

 // Define data label shape.
 dataLabels.getFormat().setShapeType(ChartShapeType.UP_ARROW);
 dataLabels.getFormat().getStroke().getFill().solid(Color.blue);

 // Set data label orientation and rotation for the entire series.
 dataLabels.setOrientation(ShapeTextOrientation.VERTICAL_FAR_EAST);
 dataLabels.setRotation(-45);

 // Change orientation and rotation of the first data label.
 dataLabels.get(0).setOrientation(ShapeTextOrientation.HORIZONTAL);
 dataLabels.get(0).setRotation(45);

 doc.save(getArtifactsDir() + "Charts.LabelOrientationRotation.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | La rotazione delle etichette dati dell'intera serie in gradi. |

### setSeparator(String value) {#setSeparator-java.lang.String}
```
public void setSeparator(String value)
```


Imposta il separatore di stringa utilizzato per le etichette dati dell'intera serie. Il valore predefinito è una virgola, eccetto per i grafici a torta che mostrano solo il nome della categoria e la percentuale, dove viene utilizzato un ritorno a capo.

 **Remarks:** 

Il valore definito per questa proprietà può essere sovrascritto per un'etichetta dati individuale utilizzando la proprietà [ChartDataLabel.getSeparator()](../../com.aspose.words/chartdatalabel/\#getSeparator) / [ChartDataLabel.setSeparator(java.lang.String)](../../com.aspose.words/chartdatalabel/\#setSeparator-java.lang.String).

 **Examples:** 

Mostra come lavorare con le etichette dei dati di un grafico a bolle.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

Mostra come lavorare con le etichette dei dati di un grafico a torta.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Separatore di stringa utilizzato per le etichette dati dell'intera serie. |

### setShapeType(int value) {#setShapeType-int}
```
public void setShapeType(int value)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int |  |

### setShowBubbleSize(boolean value) {#setShowBubbleSize-boolean}
```
public void setShowBubbleSize(boolean value)
```


Consente di specificare se la dimensione della bolla deve essere visualizzata per le etichette dei dati dell'intera serie. Si applica solo ai grafici a bolle. Il valore predefinito è false.

 **Remarks:** 

Il valore definito per questa proprietà può essere sovrascritto per un'etichetta dati individuale utilizzando la proprietà [ChartDataLabel.getShowBubbleSize()](../../com.aspose.words/chartdatalabel/\#getShowBubbleSize) / [ChartDataLabel.setShowBubbleSize(boolean)](../../com.aspose.words/chartdatalabel/\#setShowBubbleSize-boolean).

 **Examples:** 

Mostra come lavorare con le etichette dei dati di un grafico a bolle.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setShowCategoryName(boolean value) {#setShowCategoryName-boolean}
```
public void setShowCategoryName(boolean value)
```


Consente di specificare se il nome della categoria deve essere visualizzato per le etichette dei dati dell'intera serie. Il valore predefinito è false.

 **Remarks:** 

Il valore definito per questa proprietà può essere sovrascritto per un'etichetta dati individuale utilizzando la proprietà [ChartDataLabel.getShowCategoryName()](../../com.aspose.words/chartdatalabel/\#getShowCategoryName) / [ChartDataLabel.setShowCategoryName(boolean)](../../com.aspose.words/chartdatalabel/\#setShowCategoryName-boolean).

 **Examples:** 

Mostra come lavorare con le etichette dei dati di un grafico a bolle.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setShowDataLabelsRange(boolean value) {#setShowDataLabelsRange-boolean}
```
public void setShowDataLabelsRange(boolean value)
```


Consente di specificare se i valori dell'intervallo delle etichette dei dati devono essere visualizzati nelle etichette dei dati dell'intera serie. Il valore predefinito è false.

 **Remarks:** 

Il valore definito per questa proprietà può essere sovrascritto per un'etichetta dati individuale utilizzando la proprietà [ChartDataLabel.getShowDataLabelsRange()](../../com.aspose.words/chartdatalabel/\#getShowDataLabelsRange) / [ChartDataLabel.setShowDataLabelsRange(boolean)](../../com.aspose.words/chartdatalabel/\#setShowDataLabelsRange-boolean).

 **Examples:** 

Mostra come applicare etichette ai punti dati in un grafico a linee.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setShowLeaderLines(boolean value) {#setShowLeaderLines-boolean}
```
public void setShowLeaderLines(boolean value)
```


Consente di specificare se le linee guida delle etichette dati devono essere visualizzate per le etichette dati dell'intera serie. Il valore predefinito è false.

 **Remarks:** 

Si applica solo ai grafici a torta. Le linee guida creano una connessione visiva tra un'etichetta dati e il relativo punto dati.

Il valore definito per questa proprietà può essere sovrascritto per un'etichetta dati individuale utilizzando la proprietà [ChartDataLabel.getShowLeaderLines()](../../com.aspose.words/chartdatalabel/\#getShowLeaderLines) / [ChartDataLabel.setShowLeaderLines(boolean)](../../com.aspose.words/chartdatalabel/\#setShowLeaderLines-boolean).

 **Examples:** 

Mostra come lavorare con le etichette dei dati di un grafico a torta.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setShowLegendKey(boolean value) {#setShowLegendKey-boolean}
```
public void setShowLegendKey(boolean value)
```


Consente di specificare se la chiave della legenda deve essere visualizzata per le etichette dati dell'intera serie. Il valore predefinito è false.

 **Remarks:** 

Il valore definito per questa proprietà può essere sovrascritto per un'etichetta dati individuale utilizzando la proprietà [ChartDataLabel.getShowLegendKey()](../../com.aspose.words/chartdatalabel/\#getShowLegendKey) / [ChartDataLabel.setShowLegendKey(boolean)](../../com.aspose.words/chartdatalabel/\#setShowLegendKey-boolean).

 **Examples:** 

Mostra come lavorare con le etichette dei dati di un grafico a torta.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setShowPercentage(boolean value) {#setShowPercentage-boolean}
```
public void setShowPercentage(boolean value)
```


Consente di specificare se il valore percentuale deve essere visualizzato per le etichette dati dell'intera serie. Il valore predefinito è false. Si applica solo ai grafici a torta.

 **Remarks:** 

Il valore definito per questa proprietà può essere sovrascritto per un'etichetta dati individuale utilizzando la proprietà [ChartDataLabel.getShowPercentage()](../../com.aspose.words/chartdatalabel/\#getShowPercentage) / [ChartDataLabel.setShowPercentage(boolean)](../../com.aspose.words/chartdatalabel/\#setShowPercentage-boolean).

 **Examples:** 

Mostra come lavorare con le etichette dei dati di un grafico a torta.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setShowSeriesName(boolean value) {#setShowSeriesName-boolean}
```
public void setShowSeriesName(boolean value)
```


Imposta un Boolean per indicare il comportamento di visualizzazione del nome della serie per le etichette dati dell'intera serie. true per mostrare il nome della serie; false per nasconderlo. Per impostazione predefinita false.

 **Remarks:** 

Il valore definito per questa proprietà può essere sovrascritto per un'etichetta dati individuale utilizzando la proprietà [ChartDataLabel.getShowSeriesName()](../../com.aspose.words/chartdatalabel/\#getShowSeriesName) / [ChartDataLabel.setShowSeriesName(boolean)](../../com.aspose.words/chartdatalabel/\#setShowSeriesName-boolean).

 **Examples:** 

Mostra come lavorare con le etichette dei dati di un grafico a bolle.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un Boolean per indicare il comportamento di visualizzazione del nome della serie per le etichette dati dell'intera serie. |

### setShowValue(boolean value) {#setShowValue-boolean}
```
public void setShowValue(boolean value)
```


Consente di specificare se i valori devono essere visualizzati nelle etichette dati dell'intera serie. Il valore predefinito è false.

 **Remarks:** 

Il valore definito per questa proprietà può essere sovrascritto per un'etichetta dati individuale utilizzando la proprietà [ChartDataLabel.getShowValue()](../../com.aspose.words/chartdatalabel/\#getShowValue) / [ChartDataLabel.setShowValue(boolean)](../../com.aspose.words/chartdatalabel/\#setShowValue-boolean).

 **Examples:** 

Mostra come lavorare con le etichette dei dati di un grafico a torta.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

