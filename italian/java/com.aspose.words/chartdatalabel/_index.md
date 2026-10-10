---
title: "ChartDataLabel"
linktitle: "ChartDataLabel"
second_title: "Aspose.Words per Java"
description: "Rappresenta l'etichetta dati su un punto o una linea di tendenza di un grafico in Java."
type: docs
weight: 71
url: /it/java/com.aspose.words/chartdatalabel/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ChartDataLabel implements Cloneable
```

Rappresenta l'etichetta dati su un punto o una linea di tendenza del grafico.

Per saperne di più, visita l'articolo di documentazione [ Working with Charts ][Working with Charts].

 **Remarks:** 

In una serie, l'oggetto [ChartDataLabel](../../com.aspose.words/chartdatalabel/) è un membro della [ChartDataLabelCollection](../../com.aspose.words/chartdatalabelcollection/). La [ChartDataLabelCollection](../../com.aspose.words/chartdatalabelcollection/) contiene un oggetto [ChartDataLabel](../../com.aspose.words/chartdatalabel/) per ogni punto.

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
| [clearFormat()](#clearFormat) | Cancella il formato di questa etichetta dati. |
| [fetchSpecialDefaultRunPropertyValue(int key)](#fetchSpecialDefaultRunPropertyValue-int) |  |
| [generateItemText()](#generateItemText) |  |
| [getFont()](#getFont) | Fornisce l'accesso alla formattazione del carattere di questa etichetta dati. |
| [getFormat()](#getFormat) | Fornisce l'accesso alla formattazione di riempimento e linea dell'etichetta dati. |
| [getIndex()](#getIndex) | Specifica l'indice dell'elemento contenitore. |
| [getLeft()](#getLeft) | Ottiene la distanza dell'etichetta dati in punti dal bordo sinistro del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/\\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\\#setPosition-int), a seconda del valore della proprietà [getLeftMode()](../../com.aspose.words/chartdatalabel/\\#getLeftMode) / [setLeftMode(int)](../../com.aspose.words/chartdatalabel/\\#setLeftMode-int). |
| [getLeftMode()](#getLeftMode) | Ottiene la modalità di interpretazione del valore della proprietà [getLeft()](../../com.aspose.words/chartdatalabel/\\#getLeft) / [setLeft(double)](../../com.aspose.words/chartdatalabel/\\#setLeft-double): se imposta la posizione dell'etichetta dati dal bordo sinistro del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/\\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\\#setPosition-int). |
| [getNumberFormat()](#getNumberFormat) | Restituisce il formato numerico dell'elemento padre. |
| [getOrientation()](#getOrientation) | Ottiene l'orientamento del testo dell'etichetta. |
| [getPosition()](#getPosition) | Ottiene la posizione dell'etichetta dati. |
| [getRelativePropertyValue(int key, Object value)](#getRelativePropertyValue-int-java.lang.Object) |  |
| [getRotation()](#getRotation) | Ottiene la rotazione dell'etichetta in gradi. |
| [getSeparator()](#getSeparator) | Ottiene il separatore di stringa utilizzato per le etichette dati su un grafico. |
| [getShapeType()](#getShapeType) |  |
| [getShowBubbleSize()](#getShowBubbleSize) | Consente di specificare se la dimensione della bolla deve essere visualizzata per le etichette dati in un grafico. |
| [getShowCategoryName()](#getShowCategoryName) | Consente di specificare se il nome della categoria deve essere visualizzato per le etichette dati in un grafico. |
| [getShowDataLabelsRange()](#getShowDataLabelsRange) | Consente di specificare se i valori dell'intervallo delle etichette dati devono essere visualizzati nelle etichette dati. |
| [getShowLeaderLines()](#getShowLeaderLines) | Consente di specificare se le linee guida dell'etichetta dati devono essere mostrate. |
| [getShowLegendKey()](#getShowLegendKey) | Consente di specificare se la chiave della legenda deve essere visualizzata per le etichette dati in un grafico. |
| [getShowPercentage()](#getShowPercentage) | Consente di specificare se il valore percentuale deve essere visualizzato per le etichette dati in un grafico. |
| [getShowSeriesName()](#getShowSeriesName) | Ottiene un Boolean per indicare il comportamento di visualizzazione del nome della serie per le etichette dati in un grafico. |
| [getShowValue()](#getShowValue) | Consente di specificare se i valori devono essere visualizzati nelle etichette dati. |
| [getTop()](#getTop) | Ottiene la distanza dell'etichetta dati in punti dal bordo superiore del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int), a seconda del valore della proprietà [getTopMode()](../../com.aspose.words/chartdatalabel/#getTopMode) / [setTopMode(int)](../../com.aspose.words/chartdatalabel/#setTopMode-int). |
| [getTopMode()](#getTopMode) | Ottiene la modalità di interpretazione del valore della proprietà [getTop()](../../com.aspose.words/chartdatalabel/#getTop) / [setTop(double)](../../com.aspose.words/chartdatalabel/#setTop-double) : se imposta la posizione dell'etichetta dati dal bordo superiore del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int). |
| [isFillSupported()](#isFillSupported) |  |
| [isFormatDefined()](#isFormatDefined) |  |
| [isHidden()](#isHidden) | Ottiene/imposta un flag che indica se questa etichetta è nascosta. |
| [isHidden(boolean value)](#isHidden-boolean) | Ottiene/imposta un flag che indica se questa etichetta è nascosta. |
| [isInherited()](#isInherited) |  |
| [isVisible()](#isVisible) | Restituisce  true  se questa etichetta dati ha qualcosa da visualizzare. |
| [materializeSpPr()](#materializeSpPr) |  |
| [setLeft(double value)](#setLeft-double) | Imposta la distanza dell'etichetta dati in punti dal bordo sinistro del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int), a seconda del valore della proprietà [getLeftMode()](../../com.aspose.words/chartdatalabel/#getLeftMode) / [setLeftMode(int)](../../com.aspose.words/chartdatalabel/#setLeftMode-int). |
| [setLeftMode(int value)](#setLeftMode-int) | Imposta la modalità di interpretazione del valore della proprietà [getLeft()](../../com.aspose.words/chartdatalabel/#getLeft) / [setLeft(double)](../../com.aspose.words/chartdatalabel/#setLeft-double) : se imposta la posizione dell'etichetta dati dal bordo sinistro del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int). |
| [setOrientation(int value)](#setOrientation-int) | Imposta l'orientamento del testo dell'etichetta. |
| [setPosition(int value)](#setPosition-int) | Imposta la posizione dell'etichetta dati. |
| [setRotation(int value)](#setRotation-int) | Imposta la rotazione dell'etichetta in gradi. |
| [setSeparator(String value)](#setSeparator-java.lang.String) | Imposta il separatore di stringa utilizzato per le etichette dati in un grafico. |
| [setShapeType(int value)](#setShapeType-int) |  |
| [setShowBubbleSize(boolean value)](#setShowBubbleSize-boolean) | Consente di specificare se la dimensione della bolla deve essere visualizzata per le etichette dati in un grafico. |
| [setShowCategoryName(boolean value)](#setShowCategoryName-boolean) | Consente di specificare se il nome della categoria deve essere visualizzato per le etichette dati in un grafico. |
| [setShowDataLabelsRange(boolean value)](#setShowDataLabelsRange-boolean) | Consente di specificare se i valori dell'intervallo delle etichette dati devono essere visualizzati nelle etichette dati. |
| [setShowLeaderLines(boolean value)](#setShowLeaderLines-boolean) | Consente di specificare se le linee guida dell'etichetta dati devono essere mostrate. |
| [setShowLegendKey(boolean value)](#setShowLegendKey-boolean) | Consente di specificare se la chiave della legenda deve essere visualizzata per le etichette dati in un grafico. |
| [setShowPercentage(boolean value)](#setShowPercentage-boolean) | Consente di specificare se il valore percentuale deve essere visualizzato per le etichette dati in un grafico. |
| [setShowSeriesName(boolean value)](#setShowSeriesName-boolean) | Imposta un Boolean per indicare il comportamento di visualizzazione del nome della serie per le etichette dati in un grafico. |
| [setShowValue(boolean value)](#setShowValue-boolean) | Consente di specificare se i valori devono essere visualizzati nelle etichette dati. |
| [setTop(double value)](#setTop-double) | Imposta la distanza dell'etichetta dati in punti dal bordo superiore del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int), a seconda del valore della proprietà [getTopMode()](../../com.aspose.words/chartdatalabel/#getTopMode) / [setTopMode(int)](../../com.aspose.words/chartdatalabel/#setTopMode-int). |
| [setTopMode(int value)](#setTopMode-int) | Imposta la modalità di interpretazione del valore della proprietà [getTop()](../../com.aspose.words/chartdatalabel/#getTop) / [setTop(double)](../../com.aspose.words/chartdatalabel/#setTop-double) : se imposta la posizione dell'etichetta dati dal bordo superiore del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int). |
### clearFormat() {#clearFormat}
```
public void clearFormat()
```


Cancella il formato di questa etichetta dati. Le proprietà sono impostate ai valori predefiniti definiti nella collezione di etichette dati padre.

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

### fetchSpecialDefaultRunPropertyValue(int key) {#fetchSpecialDefaultRunPropertyValue-int}
```
public Object fetchSpecialDefaultRunPropertyValue(int key)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### generateItemText() {#generateItemText}
```
public String generateItemText()
```




**Returns:**
java.lang.String
### getFont() {#getFont}
```
public Font getFont()
```


Fornisce l'accesso alla formattazione del carattere di questa etichetta dati.

 **Examples:** 

Mostra come utilizzare gli effetti 3D con i grafici a bolle.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.BUBBLE_3_D, 500.0, 350.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Y-Values", chart.getSeries().get(0).getName());
 Assert.assertTrue(chart.getSeries().get(0).getBubble3D());

 // Apply a data label to each bubble that displays its diameter.
 for (int i = 0; i < 3; i++) {
     chart.getSeries().get(0).hasDataLabels(true);
     ChartDataLabel cdl = chart.getSeries().get(0).getDataLabels().get(i);
     chart.getSeries().get(0).getDataLabels().get(i).getFont().setSize(12.0);
     cdl.setShowBubbleSize(true);
 }

 doc.save(getArtifactsDir() + "Charts.Bubble3D.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getFormat() {#getFormat}
```
public ChartFormat getFormat()
```


Fornisce l'accesso alla formattazione di riempimento e linea dell'etichetta dati.

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
[ChartFormat](../../com.aspose.words/chartformat/) - The corresponding [ChartFormat](../../com.aspose.words/chartformat/) value.
### getIndex() {#getIndex}
```
public int getIndex()
```


Specifica l'indice dell'elemento contenitore. Questo indice determinerà a quale collezione di figli del genitore si applica questo elemento. Il valore predefinito è 0.

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
int - Il valore  int  corrispondente.
### getLeft() {#getLeft}
```
public double getLeft()
```


Ottiene la distanza dell'etichetta dati in punti dal bordo sinistro del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/\\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\\#setPosition-int), a seconda del valore della proprietà [getLeftMode()](../../com.aspose.words/chartdatalabel/\\#getLeftMode) / [setLeftMode(int)](../../com.aspose.words/chartdatalabel/\\#setLeftMode-int).

 **Remarks:** 

Il valore della proprietà cambia proporzionalmente se la forma del grafico viene ridimensionata.

La proprietà non può essere impostata in un grafico di Word 2016.

 **Examples:** 

Mostra come posizionare le etichette dati di un grafico a ciambella all'esterno della ciambella.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth;
     if (value < 10)
         labelWidth = ONE_CHAR_LABEL_WIDTH;
     else
         labelWidth = TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         int factor;
         if (isOnTop)
             factor = 1;
         else
             factor = -1;

         labelLeft = previousLabel.getLeft() + labelWidth * factor + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Returns:**
double - La distanza dell'etichetta dati in punti dal bordo sinistro del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int), a seconda del valore della proprietà [getLeftMode()](../../com.aspose.words/chartdatalabel/\#getLeftMode) / [setLeftMode(int)](../../com.aspose.words/chartdatalabel/\#setLeftMode-int).
### getLeftMode() {#getLeftMode}
```
public int getLeftMode()
```


Ottiene la modalità di interpretazione del valore della proprietà [getLeft()](../../com.aspose.words/chartdatalabel/\\#getLeft) / [setLeft(double)](../../com.aspose.words/chartdatalabel/\\#setLeft-double): se imposta la posizione dell'etichetta dati dal bordo sinistro del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/\\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\\#setPosition-int).

 **Remarks:** 

La proprietà non può essere impostata in un grafico di Word 2016.

 **Examples:** 

Mostra come posizionare le etichette dati di un grafico a ciambella all'esterno della ciambella.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth;
     if (value < 10)
         labelWidth = ONE_CHAR_LABEL_WIDTH;
     else
         labelWidth = TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         int factor;
         if (isOnTop)
             factor = 1;
         else
             factor = -1;

         labelLeft = previousLabel.getLeft() + labelWidth * factor + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Returns:**
int - La modalità di interpretazione del valore della proprietà [getLeft()](../../com.aspose.words/chartdatalabel/\#getLeft) / [setLeft(double)](../../com.aspose.words/chartdatalabel/\#setLeft-double): se imposta la posizione dell'etichetta dati dal bordo sinistro del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int). Il valore restituito è una delle costanti [ChartDataLabelLocationMode](../../com.aspose.words/chartdatalabellocationmode/).
### getNumberFormat() {#getNumberFormat}
```
public ChartNumberFormat getNumberFormat()
```


Restituisce il formato numerico dell'elemento padre.

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
[ChartNumberFormat](../../com.aspose.words/chartnumberformat/) - Number format of the parent element.
### getOrientation() {#getOrientation}
```
public int getOrientation()
```


Ottiene l'orientamento del testo dell'etichetta.

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
int - L'orientamento del testo dell'etichetta. Il valore restituito è una delle costanti [ShapeTextOrientation](../../com.aspose.words/shapetextorientation/).
### getPosition() {#getPosition}
```
public int getPosition()
```


Ottiene la posizione dell'etichetta dati.

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
int - La posizione dell'etichetta dati. Il valore restituito è una delle costanti [ChartDataLabelPosition](../../com.aspose.words/chartdatalabelposition/).
### getRelativePropertyValue(int key, Object value) {#getRelativePropertyValue-int-java.lang.Object}
```
public Object getRelativePropertyValue(int key, Object value)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| key | int |  |
| valore | java.lang.Object |  |

**Returns:**
java.lang.Object
### getRotation() {#getRotation}
```
public int getRotation()
```


Ottiene la rotazione dell'etichetta in gradi.

 **Remarks:** 

L'intervallo dei valori accettabili è da -180 a 180 inclusi. Il valore predefinito è 0.

Se il valore di [getOrientation()](../../com.aspose.words/chartdatalabel/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/chartdatalabel/\#setOrientation-int) è [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL), la forma dell'etichetta, se esiste, viene ruotata insieme al testo dell'etichetta. Altrimenti, solo il testo dell'etichetta viene ruotato.

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
int - La rotazione dell'etichetta in gradi.
### getSeparator() {#getSeparator}
```
public String getSeparator()
```


Restituisce il separatore di stringa utilizzato per le etichette dati su un grafico. Il valore predefinito è una virgola, eccetto per i grafici a torta che mostrano solo il nome della categoria e la percentuale, dove viene utilizzato un ritorno a capo.

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
java.lang.String - Separatore di stringa utilizzato per le etichette dati su un grafico.
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


Consente di specificare se visualizzare la dimensione della bolla per le etichette dati su un grafico. Si applica solo ai grafici a bolle. Il valore predefinito è false.

 **Examples:** 

Mostra come utilizzare gli effetti 3D con i grafici a bolle.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.BUBBLE_3_D, 500.0, 350.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Y-Values", chart.getSeries().get(0).getName());
 Assert.assertTrue(chart.getSeries().get(0).getBubble3D());

 // Apply a data label to each bubble that displays its diameter.
 for (int i = 0; i < 3; i++) {
     chart.getSeries().get(0).hasDataLabels(true);
     ChartDataLabel cdl = chart.getSeries().get(0).getDataLabels().get(i);
     chart.getSeries().get(0).getDataLabels().get(i).getFont().setSize(12.0);
     cdl.setShowBubbleSize(true);
 }

 doc.save(getArtifactsDir() + "Charts.Bubble3D.docx");
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getShowCategoryName() {#getShowCategoryName}
```
public boolean getShowCategoryName()
```


Consente di specificare se visualizzare il nome della categoria per le etichette dati su un grafico. Il valore predefinito è false.

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
### getShowDataLabelsRange() {#getShowDataLabelsRange}
```
public boolean getShowDataLabelsRange()
```


Consente di specificare se visualizzare i valori dell'intervallo delle etichette dati nelle etichette dati. Il valore predefinito è false.

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


Consente di specificare se mostrare le linee guida dell'etichetta dati. Il valore predefinito è false.

 **Remarks:** 

Si applica solo ai grafici a torta. Le linee guida creano una connessione visiva tra un'etichetta dati e il relativo punto dati.

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
### getShowLegendKey() {#getShowLegendKey}
```
public boolean getShowLegendKey()
```


Consente di specificare se visualizzare la chiave della legenda per le etichette dati su un grafico. Il valore predefinito è false.

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
### getShowPercentage() {#getShowPercentage}
```
public boolean getShowPercentage()
```


Consente di specificare se visualizzare il valore percentuale per le etichette dati su un grafico. Il valore predefinito è false.

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
### getShowSeriesName() {#getShowSeriesName}
```
public boolean getShowSeriesName()
```


Restituisce un Booleano che indica il comportamento di visualizzazione del nome della serie per le etichette dati su un grafico. true per mostrare il nome della serie; false per nasconderlo. Per impostazione predefinita è false.

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
boolean - Un Booleano che indica il comportamento di visualizzazione del nome della serie per le etichette dati su un grafico.
### getShowValue() {#getShowValue}
```
public boolean getShowValue()
```


Consente di specificare se visualizzare i valori nelle etichette dati. Il valore predefinito è false.

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
### getTop() {#getTop}
```
public double getTop()
```


Ottiene la distanza dell'etichetta dati in punti dal bordo superiore del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int), a seconda del valore della proprietà [getTopMode()](../../com.aspose.words/chartdatalabel/#getTopMode) / [setTopMode(int)](../../com.aspose.words/chartdatalabel/#setTopMode-int).

 **Remarks:** 

Il valore della proprietà cambia proporzionalmente se la forma del grafico viene ridimensionata.

La proprietà non può essere impostata in un grafico di Word 2016.

 **Examples:** 

Mostra come posizionare le etichette dati di un grafico a ciambella all'esterno della ciambella.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth;
     if (value < 10)
         labelWidth = ONE_CHAR_LABEL_WIDTH;
     else
         labelWidth = TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         int factor;
         if (isOnTop)
             factor = 1;
         else
             factor = -1;

         labelLeft = previousLabel.getLeft() + labelWidth * factor + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Returns:**
double - La distanza dell'etichetta dati in punti dal bordo superiore del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int), a seconda del valore della proprietà [getTopMode()](../../com.aspose.words/chartdatalabel/\#getTopMode) / [setTopMode(int)](../../com.aspose.words/chartdatalabel/\#setTopMode-int).
### getTopMode() {#getTopMode}
```
public int getTopMode()
```


Ottiene la modalità di interpretazione del valore della proprietà [getTop()](../../com.aspose.words/chartdatalabel/#getTop) / [setTop(double)](../../com.aspose.words/chartdatalabel/#setTop-double) : se imposta la posizione dell'etichetta dati dal bordo superiore del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int).

 **Remarks:** 

La proprietà non può essere impostata in un grafico di Word 2016.

 **Examples:** 

Mostra come posizionare le etichette dati di un grafico a ciambella all'esterno della ciambella.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth;
     if (value < 10)
         labelWidth = ONE_CHAR_LABEL_WIDTH;
     else
         labelWidth = TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         int factor;
         if (isOnTop)
             factor = 1;
         else
             factor = -1;

         labelLeft = previousLabel.getLeft() + labelWidth * factor + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Returns:**
int - La modalità di interpretazione del valore della proprietà [getTop()](../../com.aspose.words/chartdatalabel/\#getTop) / [setTop(double)](../../com.aspose.words/chartdatalabel/\#setTop-double) : se imposta la posizione dell'etichetta dati dal bordo superiore del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) . Il valore restituito è uno dei costanti di [ChartDataLabelLocationMode](../../com.aspose.words/chartdatalabellocationmode/) .
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
### isHidden() {#isHidden}
```
public boolean isHidden()
```


Ottiene/imposta un flag che indica se questa etichetta è nascosta. Il valore predefinito è false.

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
### isHidden(boolean value) {#isHidden-boolean}
```
public void isHidden(boolean value)
```


Ottiene/imposta un flag che indica se questa etichetta è nascosta. Il valore predefinito è false.

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

### isInherited() {#isInherited}
```
public boolean isInherited()
```




**Returns:**
boolean
### isVisible() {#isVisible}
```
public boolean isVisible()
```


Restituisce  true  se questa etichetta dati ha qualcosa da visualizzare.

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
boolean - true se questa etichetta dati ha qualcosa da visualizzare.
### materializeSpPr() {#materializeSpPr}
```
public void materializeSpPr()
```




### setLeft(double value) {#setLeft-double}
```
public void setLeft(double value)
```


Imposta la distanza dell'etichetta dati in punti dal bordo sinistro del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int), a seconda del valore della proprietà [getLeftMode()](../../com.aspose.words/chartdatalabel/#getLeftMode) / [setLeftMode(int)](../../com.aspose.words/chartdatalabel/#setLeftMode-int).

 **Remarks:** 

Il valore della proprietà cambia proporzionalmente se la forma del grafico viene ridimensionata.

La proprietà non può essere impostata in un grafico di Word 2016.

 **Examples:** 

Mostra come posizionare le etichette dati di un grafico a ciambella all'esterno della ciambella.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth;
     if (value < 10)
         labelWidth = ONE_CHAR_LABEL_WIDTH;
     else
         labelWidth = TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         int factor;
         if (isOnTop)
             factor = 1;
         else
             factor = -1;

         labelLeft = previousLabel.getLeft() + labelWidth * factor + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | double | La distanza dell'etichetta dati in punti dal bordo sinistro del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) , a seconda del valore della proprietà [getLeftMode()](../../com.aspose.words/chartdatalabel/\#getLeftMode) / [setLeftMode(int)](../../com.aspose.words/chartdatalabel/\#setLeftMode-int) . |

### setLeftMode(int value) {#setLeftMode-int}
```
public void setLeftMode(int value)
```


Imposta la modalità di interpretazione del valore della proprietà [getLeft()](../../com.aspose.words/chartdatalabel/#getLeft) / [setLeft(double)](../../com.aspose.words/chartdatalabel/#setLeft-double) : se imposta la posizione dell'etichetta dati dal bordo sinistro del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int).

 **Remarks:** 

La proprietà non può essere impostata in un grafico di Word 2016.

 **Examples:** 

Mostra come posizionare le etichette dati di un grafico a ciambella all'esterno della ciambella.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth;
     if (value < 10)
         labelWidth = ONE_CHAR_LABEL_WIDTH;
     else
         labelWidth = TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         int factor;
         if (isOnTop)
             factor = 1;
         else
             factor = -1;

         labelLeft = previousLabel.getLeft() + labelWidth * factor + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | La modalità di interpretazione del valore della proprietà [getLeft()](../../com.aspose.words/chartdatalabel/\#getLeft) / [setLeft(double)](../../com.aspose.words/chartdatalabel/\#setLeft-double) : se imposta la posizione dell'etichetta dati dal bordo sinistro del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) . Il valore deve essere uno dei costanti di [ChartDataLabelLocationMode](../../com.aspose.words/chartdatalabellocationmode/) . |

### setOrientation(int value) {#setOrientation-int}
```
public void setOrientation(int value)
```


Imposta l'orientamento del testo dell'etichetta.

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
| value | int | L'orientamento del testo dell'etichetta. Il valore deve essere uno dei costanti di [ShapeTextOrientation](../../com.aspose.words/shapetextorientation/) . |

### setPosition(int value) {#setPosition-int}
```
public void setPosition(int value)
```


Imposta la posizione dell'etichetta dati.

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
| value | int | La posizione dell'etichetta dati. Il valore deve essere uno dei costanti di [ChartDataLabelPosition](../../com.aspose.words/chartdatalabelposition/) . |

### setRotation(int value) {#setRotation-int}
```
public void setRotation(int value)
```


Imposta la rotazione dell'etichetta in gradi.

 **Remarks:** 

L'intervallo dei valori accettabili è da -180 a 180 inclusi. Il valore predefinito è 0.

Se il valore di [getOrientation()](../../com.aspose.words/chartdatalabel/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/chartdatalabel/\#setOrientation-int) è [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL), la forma dell'etichetta, se esiste, viene ruotata insieme al testo dell'etichetta. Altrimenti, solo il testo dell'etichetta viene ruotato.

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
| valore | int | La rotazione dell'etichetta in gradi. |

### setSeparator(String value) {#setSeparator-java.lang.String}
```
public void setSeparator(String value)
```


Imposta il separatore di stringa utilizzato per le etichette dati su un grafico. Il valore predefinito è una virgola, eccetto per i grafici a torta che mostrano solo il nome della categoria e la percentuale, quando invece deve essere usata un'interruzione di riga.

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
| valore | java.lang.String | Separatore di stringa utilizzato per le etichette dati su un grafico. |

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


Consente di specificare se visualizzare la dimensione della bolla per le etichette dati su un grafico. Si applica solo ai grafici a bolle. Il valore predefinito è false.

 **Examples:** 

Mostra come utilizzare gli effetti 3D con i grafici a bolle.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.BUBBLE_3_D, 500.0, 350.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Y-Values", chart.getSeries().get(0).getName());
 Assert.assertTrue(chart.getSeries().get(0).getBubble3D());

 // Apply a data label to each bubble that displays its diameter.
 for (int i = 0; i < 3; i++) {
     chart.getSeries().get(0).hasDataLabels(true);
     ChartDataLabel cdl = chart.getSeries().get(0).getDataLabels().get(i);
     chart.getSeries().get(0).getDataLabels().get(i).getFont().setSize(12.0);
     cdl.setShowBubbleSize(true);
 }

 doc.save(getArtifactsDir() + "Charts.Bubble3D.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setShowCategoryName(boolean value) {#setShowCategoryName-boolean}
```
public void setShowCategoryName(boolean value)
```


Consente di specificare se visualizzare il nome della categoria per le etichette dati su un grafico. Il valore predefinito è false.

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

### setShowDataLabelsRange(boolean value) {#setShowDataLabelsRange-boolean}
```
public void setShowDataLabelsRange(boolean value)
```


Consente di specificare se visualizzare i valori dell'intervallo delle etichette dati nelle etichette dati. Il valore predefinito è false.

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


Consente di specificare se mostrare le linee guida dell'etichetta dati. Il valore predefinito è false.

 **Remarks:** 

Si applica solo ai grafici a torta. Le linee guida creano una connessione visiva tra un'etichetta dati e il relativo punto dati.

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

### setShowLegendKey(boolean value) {#setShowLegendKey-boolean}
```
public void setShowLegendKey(boolean value)
```


Consente di specificare se visualizzare la chiave della legenda per le etichette dati su un grafico. Il valore predefinito è false.

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

### setShowPercentage(boolean value) {#setShowPercentage-boolean}
```
public void setShowPercentage(boolean value)
```


Consente di specificare se visualizzare il valore percentuale per le etichette dati su un grafico. Il valore predefinito è false.

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

### setShowSeriesName(boolean value) {#setShowSeriesName-boolean}
```
public void setShowSeriesName(boolean value)
```


Imposta un Boolean per indicare il comportamento di visualizzazione del nome della serie per le etichette dati su un grafico. true per mostrare il nome della serie; false per nasconderlo. Per impostazione predefinita è false.

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
| valore | boolean | Un Boolean per indicare il comportamento di visualizzazione del nome della serie per le etichette dati su un grafico. |

### setShowValue(boolean value) {#setShowValue-boolean}
```
public void setShowValue(boolean value)
```


Consente di specificare se visualizzare i valori nelle etichette dati. Il valore predefinito è false.

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

### setTop(double value) {#setTop-double}
```
public void setTop(double value)
```


Imposta la distanza dell'etichetta dati in punti dal bordo superiore del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int), a seconda del valore della proprietà [getTopMode()](../../com.aspose.words/chartdatalabel/#getTopMode) / [setTopMode(int)](../../com.aspose.words/chartdatalabel/#setTopMode-int).

 **Remarks:** 

Il valore della proprietà cambia proporzionalmente se la forma del grafico viene ridimensionata.

La proprietà non può essere impostata in un grafico di Word 2016.

 **Examples:** 

Mostra come posizionare le etichette dati di un grafico a ciambella all'esterno della ciambella.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth;
     if (value < 10)
         labelWidth = ONE_CHAR_LABEL_WIDTH;
     else
         labelWidth = TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         int factor;
         if (isOnTop)
             factor = 1;
         else
             factor = -1;

         labelLeft = previousLabel.getLeft() + labelWidth * factor + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | double | La distanza dell'etichetta dati in punti dal bordo superiore del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) , a seconda del valore della proprietà [getTopMode()](../../com.aspose.words/chartdatalabel/\#getTopMode) / [setTopMode(int)](../../com.aspose.words/chartdatalabel/\#setTopMode-int) . |

### setTopMode(int value) {#setTopMode-int}
```
public void setTopMode(int value)
```


Imposta la modalità di interpretazione del valore della proprietà [getTop()](../../com.aspose.words/chartdatalabel/#getTop) / [setTop(double)](../../com.aspose.words/chartdatalabel/#setTop-double) : se imposta la posizione dell'etichetta dati dal bordo superiore del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int).

 **Remarks:** 

La proprietà non può essere impostata in un grafico di Word 2016.

 **Examples:** 

Mostra come posizionare le etichette dati di un grafico a ciambella all'esterno della ciambella.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth;
     if (value < 10)
         labelWidth = ONE_CHAR_LABEL_WIDTH;
     else
         labelWidth = TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         int factor;
         if (isOnTop)
             factor = 1;
         else
             factor = -1;

         labelLeft = previousLabel.getLeft() + labelWidth * factor + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | La modalità di interpretazione del valore della proprietà [getTop()](../../com.aspose.words/chartdatalabel/\#getTop) / [setTop(double)](../../com.aspose.words/chartdatalabel/\#setTop-double) : se imposta la posizione dell'etichetta dati dal bordo superiore del grafico o dalla posizione specificata dalla sua proprietà [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) . Il valore deve essere uno dei costanti di [ChartDataLabelLocationMode](../../com.aspose.words/chartdatalabellocationmode/) . |

