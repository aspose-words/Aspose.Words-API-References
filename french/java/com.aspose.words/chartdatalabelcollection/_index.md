---
title: "ChartDataLabelCollection"
linktitle: "ChartDataLabelCollection"
second_title: "Aspose.Words pour Java"
description: "Représente une collection de ChartDataLabel en Java."
type: docs
weight: 72
url: /fr/java/com.aspose.words/chartdatalabelcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartDataLabelCollection implements Iterable
```

Représente une collection de [ChartDataLabel](../../com.aspose.words/chartdatalabel/).

Pour en savoir plus, consultez l'article de documentation [ Working with Charts ][Working with Charts].

 **Examples:** 

Montre comment appliquer des étiquettes aux points de données dans un graphique en courbes.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [clearFormat()](#clearFormat) | Efface le format de tous les [ChartDataLabel](../../com.aspose.words/chartdatalabel/) de cette collection. |
| [get(int index)](#get-int) | Renvoie le [ChartDataLabel](../../com.aspose.words/chartdatalabel/) pour l'index spécifié. |
| [getCount()](#getCount) | Renvoie le nombre de [ChartDataLabel](../../com.aspose.words/chartdatalabel/) dans cette collection. |
| [getFont()](#getFont) | Fournit l'accès au formatage de police des étiquettes de données de la série entière. |
| [getFormat()](#getFormat) | Fournit l'accès au formatage du remplissage et des lignes des étiquettes de données. |
| [getNumberFormat()](#getNumberFormat) | Obtient une instance de [ChartNumberFormat](../../com.aspose.words/chartnumberformat/) permettant de définir le format numérique pour les étiquettes de données de la série entière. |
| [getOrientation()](#getOrientation) | Obtient l'orientation du texte des étiquettes de données de la série entière. |
| [getPosition()](#getPosition) | Obtient la position des étiquettes de données. |
| [getRotation()](#getRotation) | Obtient la rotation des étiquettes de données de la série entière en degrés. |
| [getSeparator()](#getSeparator) | Obtient le séparateur de chaîne utilisé pour les étiquettes de données de la série entière. |
| [getShapeType()](#getShapeType) |  |
| [getShowBubbleSize()](#getShowBubbleSize) | Permet de spécifier si la taille des bulles doit être affichée pour les étiquettes de données de la série entière. |
| [getShowCategoryName()](#getShowCategoryName) | Permet de spécifier si le nom de catégorie doit être affiché pour les étiquettes de données de la série entière. |
| [getShowDataLabelsRange()](#getShowDataLabelsRange) | Permet de spécifier si les valeurs de la plage des étiquettes de données doivent être affichées dans les étiquettes de données de la série entière. |
| [getShowLeaderLines()](#getShowLeaderLines) | Permet de spécifier si les lignes de liaison des étiquettes de données doivent être affichées pour les étiquettes de données de la série entière. |
| [getShowLegendKey()](#getShowLegendKey) | Permet de spécifier si la clé de légende doit être affichée pour les étiquettes de données de la série entière. |
| [getShowPercentage()](#getShowPercentage) | Permet de spécifier si la valeur en pourcentage doit être affichée pour les étiquettes de données de la série entière. |
| [getShowSeriesName()](#getShowSeriesName) | Obtient un booléen indiquant le comportement d'affichage du nom de la série pour les étiquettes de données de la série entière. |
| [getShowValue()](#getShowValue) | Permet de spécifier si les valeurs doivent être affichées dans les étiquettes de données de la série entière. |
| [isFillSupported()](#isFillSupported) |  |
| [isFormatDefined()](#isFormatDefined) |  |
| [isInherited()](#isInherited) |  |
| [iterator()](#iterator) | Renvoie un objet énumérateur. |
| [materializeSpPr()](#materializeSpPr) |  |
| [setOrientation(int value)](#setOrientation-int) | Définit l'orientation du texte des étiquettes de données de toute la série. |
| [setPosition(int value)](#setPosition-int) | Définit la position des étiquettes de données. |
| [setRotation(int value)](#setRotation-int) | Définit la rotation des étiquettes de données de toute la série en degrés. |
| [setSeparator(String value)](#setSeparator-java.lang.String) | Définit le séparateur de chaîne utilisé pour les étiquettes de données de toute la série. |
| [setShapeType(int value)](#setShapeType-int) |  |
| [setShowBubbleSize(boolean value)](#setShowBubbleSize-boolean) | Permet de spécifier si la taille des bulles doit être affichée pour les étiquettes de données de la série entière. |
| [setShowCategoryName(boolean value)](#setShowCategoryName-boolean) | Permet de spécifier si le nom de catégorie doit être affiché pour les étiquettes de données de la série entière. |
| [setShowDataLabelsRange(boolean value)](#setShowDataLabelsRange-boolean) | Permet de spécifier si les valeurs de la plage des étiquettes de données doivent être affichées dans les étiquettes de données de la série entière. |
| [setShowLeaderLines(boolean value)](#setShowLeaderLines-boolean) | Permet de spécifier si les lignes de liaison des étiquettes de données doivent être affichées pour les étiquettes de données de la série entière. |
| [setShowLegendKey(boolean value)](#setShowLegendKey-boolean) | Permet de spécifier si la clé de légende doit être affichée pour les étiquettes de données de la série entière. |
| [setShowPercentage(boolean value)](#setShowPercentage-boolean) | Permet de spécifier si la valeur en pourcentage doit être affichée pour les étiquettes de données de la série entière. |
| [setShowSeriesName(boolean value)](#setShowSeriesName-boolean) | Définit un booléen pour indiquer le comportement d'affichage du nom de la série pour les étiquettes de données de toute la série. |
| [setShowValue(boolean value)](#setShowValue-boolean) | Permet de spécifier si les valeurs doivent être affichées dans les étiquettes de données de la série entière. |
### clearFormat() {#clearFormat}
```
public void clearFormat()
```


Efface le format de tous les [ChartDataLabel](../../com.aspose.words/chartdatalabel/) de cette collection.

 **Examples:** 

Montre comment appliquer des étiquettes aux points de données dans un graphique en courbes.

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


Renvoie le [ChartDataLabel](../../com.aspose.words/chartdatalabel/) pour l'index spécifié.

 **Examples:** 

Montre comment appliquer des étiquettes aux points de données dans un graphique en courbes.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
[ChartDataLabel](../../com.aspose.words/chartdatalabel/) - [ChartDataLabel](../../com.aspose.words/chartdatalabel/) for the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Renvoie le nombre de [ChartDataLabel](../../com.aspose.words/chartdatalabel/) dans cette collection.

 **Examples:** 

Montre comment appliquer des étiquettes aux points de données dans un graphique en courbes.

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
int - Le nombre de [ChartDataLabel](../../com.aspose.words/chartdatalabel/) dans cette collection.
### getFont() {#getFont}
```
public Font getFont()
```


Fournit l'accès au formatage de police des étiquettes de données de la série entière.

 **Remarks:** 

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant la propriété [ChartDataLabel.getFont()](../../com.aspose.words/chartdatalabel/\#getFont).

 **Examples:** 

Montre comment activer et configurer les étiquettes de données pour une série de graphique.

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


Fournit l'accès au formatage du remplissage et des lignes des étiquettes de données.

 **Examples:** 

Montre comment définir le remplissage, le trait et le formatage des infobulles pour les étiquettes de données du graphique.

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


Obtient une instance de [ChartNumberFormat](../../com.aspose.words/chartnumberformat/) permettant de définir le format numérique pour les étiquettes de données de la série entière.

 **Examples:** 

Montre comment activer et configurer les étiquettes de données pour une série de graphique.

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


Obtient l'orientation du texte des étiquettes de données de la série entière.

 **Remarks:** 

La valeur par défaut est [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL).

 **Examples:** 

Montre comment modifier l'orientation et la rotation des étiquettes de données.

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
int - L'orientation du texte des étiquettes de données de toute la série. La valeur renvoyée est l'une des constantes [ShapeTextOrientation](../../com.aspose.words/shapetextorientation/).
### getPosition() {#getPosition}
```
public int getPosition()
```


Obtient la position des étiquettes de données.

 **Remarks:** 

La position peut être définie pour les étiquettes de données des types de séries de graphiques suivants :

\- [ChartSeriesType.BAR](../../com.aspose.words/chartseriestype/\#BAR), [ChartSeriesType.COLUMN](../../com.aspose.words/chartseriestype/\#COLUMN), [ChartSeriesType.HISTOGRAM](../../com.aspose.words/chartseriestype/\#HISTOGRAM), [ChartSeriesType.PARETO](../../com.aspose.words/chartseriestype/\#PARETO), [ChartSeriesType.WATERFALL](../../com.aspose.words/chartseriestype/\#WATERFALL); valeurs autorisées : [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END) et [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END);

\- [ChartSeriesType.BAR\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-STACKED), [ChartSeriesType.BAR\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-PERCENT-STACKED), [ChartSeriesType.COLUMN\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-STACKED), [ChartSeriesType.COLUMN\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-PERCENT-STACKED); valeurs autorisées : [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE) et [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END);

\- [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE), [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D), [ChartSeriesType.LINE](../../com.aspose.words/chartseriestype/\#LINE), [ChartSeriesType.LINE\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-STACKED), [ChartSeriesType.LINE\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-PERCENT-STACKED), [ChartSeriesType.SCATTER](../../com.aspose.words/chartseriestype/\#SCATTER), [ChartSeriesType.STOCK](../../com.aspose.words/chartseriestype/\#STOCK); valeurs autorisées : [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) et [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW);

\- [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D), [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR), [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE); valeurs autorisées : [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END), [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END) et [ChartDataLabelPosition.BEST\_FIT](../../com.aspose.words/chartdatalabelposition/\#BEST-FIT);

\- [ChartSeriesType.BOX\_AND\_WHISKER](../../com.aspose.words/chartseriestype/\#BOX-AND-WHISKER); valeurs autorisées : [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) et [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW).

 **Examples:** 

Montre comment définir la position de l'étiquette de données.

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
int - La position des étiquettes de données. La valeur renvoyée est l'une des constantes [ChartDataLabelPosition](../../com.aspose.words/chartdatalabelposition/).
### getRotation() {#getRotation}
```
public int getRotation()
```


Obtient la rotation des étiquettes de données de la série entière en degrés.

 **Remarks:** 

La plage des valeurs acceptables va de -180 à 180 inclus. La valeur par défaut est 0.

Si la valeur de [getOrientation()](../../com.aspose.words/chartdatalabelcollection/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/chartdatalabelcollection/\#setOrientation-int) est [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL), les formes d'étiquette, si elles existent, sont tournées avec le texte de l'étiquette. Sinon, seul le texte de l'étiquette est tourné.

 **Examples:** 

Montre comment modifier l'orientation et la rotation des étiquettes de données.

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
int - La rotation des étiquettes de données de la série entière en degrés.
### getSeparator() {#getSeparator}
```
public String getSeparator()
```


Obtient le séparateur de chaîne utilisé pour les étiquettes de données de la série entière. La valeur par défaut est une virgule, sauf pour les graphiques circulaires affichant uniquement le nom de catégorie et le pourcentage, où un saut de ligne doit être utilisé à la place.

 **Remarks:** 

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant la propriété [ChartDataLabel.getSeparator()](../../com.aspose.words/chartdatalabel/\#getSeparator) / [ChartDataLabel.setSeparator(java.lang.String)](../../com.aspose.words/chartdatalabel/\#setSeparator-java.lang.String).

 **Examples:** 

Montre comment travailler avec les étiquettes de données d'un graphique à bulles.

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

Montre comment travailler avec les étiquettes de données d'un graphique circulaire.

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
java.lang.String - Séparateur de chaîne utilisé pour les étiquettes de données de la série entière.
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


Permet de spécifier si la taille de la bulle doit être affichée pour les étiquettes de données de la série entière. S'applique uniquement aux graphiques à bulles. La valeur par défaut est false.

 **Remarks:** 

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant la propriété [ChartDataLabel.getShowBubbleSize()](../../com.aspose.words/chartdatalabel/\#getShowBubbleSize) / [ChartDataLabel.setShowBubbleSize(boolean)](../../com.aspose.words/chartdatalabel/\#setShowBubbleSize-boolean).

 **Examples:** 

Montre comment travailler avec les étiquettes de données d'un graphique à bulles.

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
boolean - La valeur  boolean  correspondante.
### getShowCategoryName() {#getShowCategoryName}
```
public boolean getShowCategoryName()
```


Permet de spécifier si le nom de catégorie doit être affiché pour les étiquettes de données de la série entière. La valeur par défaut est false.

 **Remarks:** 

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant la propriété [ChartDataLabel.getShowCategoryName()](../../com.aspose.words/chartdatalabel/\#getShowCategoryName) / [ChartDataLabel.setShowCategoryName(boolean)](../../com.aspose.words/chartdatalabel/\#setShowCategoryName-boolean).

 **Examples:** 

Montre comment travailler avec les étiquettes de données d'un graphique à bulles.

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
boolean - La valeur  boolean  correspondante.
### getShowDataLabelsRange() {#getShowDataLabelsRange}
```
public boolean getShowDataLabelsRange()
```


Permet de spécifier si les valeurs de la plage des étiquettes de données doivent être affichées dans les étiquettes de données de la série entière. La valeur par défaut est false.

 **Remarks:** 

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant la propriété [ChartDataLabel.getShowDataLabelsRange()](../../com.aspose.words/chartdatalabel/\#getShowDataLabelsRange) / [ChartDataLabel.setShowDataLabelsRange(boolean)](../../com.aspose.words/chartdatalabel/\#setShowDataLabelsRange-boolean).

 **Examples:** 

Montre comment appliquer des étiquettes aux points de données dans un graphique en courbes.

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
boolean - La valeur  boolean  correspondante.
### getShowLeaderLines() {#getShowLeaderLines}
```
public boolean getShowLeaderLines()
```


Permet de spécifier si les lignes de repère des étiquettes de données doivent être affichées pour les étiquettes de données de toute la série. La valeur par défaut est false.

 **Remarks:** 

S'applique uniquement aux graphiques en secteurs. Les lignes de repère créent une connexion visuelle entre une étiquette de données et son point de données correspondant.

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant la propriété [ChartDataLabel.getShowLeaderLines()](../../com.aspose.words/chartdatalabel/\#getShowLeaderLines) / [ChartDataLabel.setShowLeaderLines(boolean)](../../com.aspose.words/chartdatalabel/\#setShowLeaderLines-boolean).

 **Examples:** 

Montre comment travailler avec les étiquettes de données d'un graphique circulaire.

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
boolean - La valeur  boolean  correspondante.
### getShowLegendKey() {#getShowLegendKey}
```
public boolean getShowLegendKey()
```


Permet de spécifier si la clé de légende doit être affichée pour les étiquettes de données de toute la série. La valeur par défaut est false.

 **Remarks:** 

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant la propriété [ChartDataLabel.getShowLegendKey()](../../com.aspose.words/chartdatalabel/\#getShowLegendKey) / [ChartDataLabel.setShowLegendKey(boolean)](../../com.aspose.words/chartdatalabel/\#setShowLegendKey-boolean).

 **Examples:** 

Montre comment travailler avec les étiquettes de données d'un graphique circulaire.

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
boolean - La valeur  boolean  correspondante.
### getShowPercentage() {#getShowPercentage}
```
public boolean getShowPercentage()
```


Permet de spécifier si la valeur en pourcentage doit être affichée pour les étiquettes de données de toute la série. La valeur par défaut est false. S'applique uniquement aux graphiques en secteurs.

 **Remarks:** 

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant la propriété [ChartDataLabel.getShowPercentage()](../../com.aspose.words/chartdatalabel/\#getShowPercentage) / [ChartDataLabel.setShowPercentage(boolean)](../../com.aspose.words/chartdatalabel/\#setShowPercentage-boolean).

 **Examples:** 

Montre comment travailler avec les étiquettes de données d'un graphique circulaire.

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
boolean - La valeur  boolean  correspondante.
### getShowSeriesName() {#getShowSeriesName}
```
public boolean getShowSeriesName()
```


Obtient un booléen indiquant le comportement d'affichage du nom de la série pour les étiquettes de données de toute la série. true pour afficher le nom de la série ; false pour le masquer. Par défaut false.

 **Remarks:** 

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant la propriété [ChartDataLabel.getShowSeriesName()](../../com.aspose.words/chartdatalabel/\#getShowSeriesName) / [ChartDataLabel.setShowSeriesName(boolean)](../../com.aspose.words/chartdatalabel/\#setShowSeriesName-boolean).

 **Examples:** 

Montre comment travailler avec les étiquettes de données d'un graphique à bulles.

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
boolean - Un booléen indiquant le comportement d'affichage du nom de la série pour les étiquettes de données de toute la série.
### getShowValue() {#getShowValue}
```
public boolean getShowValue()
```


Permet de spécifier si les valeurs doivent être affichées dans les étiquettes de données de toute la série. La valeur par défaut est false.

 **Remarks:** 

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant la propriété [ChartDataLabel.getShowValue()](../../com.aspose.words/chartdatalabel/\#getShowValue) / [ChartDataLabel.setShowValue(boolean)](../../com.aspose.words/chartdatalabel/\#setShowValue-boolean).

 **Examples:** 

Montre comment travailler avec les étiquettes de données d'un graphique circulaire.

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
boolean - La valeur  boolean  correspondante.
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


Renvoie un objet énumérateur.

 **Examples:** 

Montre comment appliquer des étiquettes aux points de données dans un graphique en courbes.

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


Définit l'orientation du texte des étiquettes de données de toute la série.

 **Remarks:** 

La valeur par défaut est [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL).

 **Examples:** 

Montre comment modifier l'orientation et la rotation des étiquettes de données.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | L'orientation du texte des étiquettes de données de toute la série. La valeur doit être l'une des constantes [ShapeTextOrientation](../../com.aspose.words/shapetextorientation/). |

### setPosition(int value) {#setPosition-int}
```
public void setPosition(int value)
```


Définit la position des étiquettes de données.

 **Remarks:** 

La position peut être définie pour les étiquettes de données des types de séries de graphiques suivants :

\- [ChartSeriesType.BAR](../../com.aspose.words/chartseriestype/\#BAR), [ChartSeriesType.COLUMN](../../com.aspose.words/chartseriestype/\#COLUMN), [ChartSeriesType.HISTOGRAM](../../com.aspose.words/chartseriestype/\#HISTOGRAM), [ChartSeriesType.PARETO](../../com.aspose.words/chartseriestype/\#PARETO), [ChartSeriesType.WATERFALL](../../com.aspose.words/chartseriestype/\#WATERFALL); valeurs autorisées : [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END) et [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END);

\- [ChartSeriesType.BAR\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-STACKED), [ChartSeriesType.BAR\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-PERCENT-STACKED), [ChartSeriesType.COLUMN\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-STACKED), [ChartSeriesType.COLUMN\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-PERCENT-STACKED); valeurs autorisées : [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE) et [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END);

\- [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE), [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D), [ChartSeriesType.LINE](../../com.aspose.words/chartseriestype/\#LINE), [ChartSeriesType.LINE\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-STACKED), [ChartSeriesType.LINE\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-PERCENT-STACKED), [ChartSeriesType.SCATTER](../../com.aspose.words/chartseriestype/\#SCATTER), [ChartSeriesType.STOCK](../../com.aspose.words/chartseriestype/\#STOCK); valeurs autorisées : [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) et [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW);

\- [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D), [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR), [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE); valeurs autorisées : [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END), [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END) et [ChartDataLabelPosition.BEST\_FIT](../../com.aspose.words/chartdatalabelposition/\#BEST-FIT);

\- [ChartSeriesType.BOX\_AND\_WHISKER](../../com.aspose.words/chartseriestype/\#BOX-AND-WHISKER); valeurs autorisées : [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) et [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW).

 **Examples:** 

Montre comment définir la position de l'étiquette de données.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La position des étiquettes de données. La valeur doit être l'une des constantes [ChartDataLabelPosition](../../com.aspose.words/chartdatalabelposition/). |

### setRotation(int value) {#setRotation-int}
```
public void setRotation(int value)
```


Définit la rotation des étiquettes de données de toute la série en degrés.

 **Remarks:** 

La plage des valeurs acceptables va de -180 à 180 inclus. La valeur par défaut est 0.

Si la valeur de [getOrientation()](../../com.aspose.words/chartdatalabelcollection/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/chartdatalabelcollection/\#setOrientation-int) est [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL), les formes d'étiquette, si elles existent, sont tournées avec le texte de l'étiquette. Sinon, seul le texte de l'étiquette est tourné.

 **Examples:** 

Montre comment modifier l'orientation et la rotation des étiquettes de données.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La rotation des étiquettes de données de toute la série en degrés. |

### setSeparator(String value) {#setSeparator-java.lang.String}
```
public void setSeparator(String value)
```


Définit le séparateur de chaîne utilisé pour les étiquettes de données de toute la série. La valeur par défaut est une virgule, sauf pour les graphiques en secteurs affichant uniquement le nom de catégorie et le pourcentage, où un saut de ligne doit être utilisé à la place.

 **Remarks:** 

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant la propriété [ChartDataLabel.getSeparator()](../../com.aspose.words/chartdatalabel/\#getSeparator) / [ChartDataLabel.setSeparator(java.lang.String)](../../com.aspose.words/chartdatalabel/\#setSeparator-java.lang.String).

 **Examples:** 

Montre comment travailler avec les étiquettes de données d'un graphique à bulles.

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

Montre comment travailler avec les étiquettes de données d'un graphique circulaire.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Séparateur de chaîne utilisé pour les étiquettes de données de toute la série. |

### setShapeType(int value) {#setShapeType-int}
```
public void setShapeType(int value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int |  |

### setShowBubbleSize(boolean value) {#setShowBubbleSize-boolean}
```
public void setShowBubbleSize(boolean value)
```


Permet de spécifier si la taille de la bulle doit être affichée pour les étiquettes de données de la série entière. S'applique uniquement aux graphiques à bulles. La valeur par défaut est false.

 **Remarks:** 

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant la propriété [ChartDataLabel.getShowBubbleSize()](../../com.aspose.words/chartdatalabel/\#getShowBubbleSize) / [ChartDataLabel.setShowBubbleSize(boolean)](../../com.aspose.words/chartdatalabel/\#setShowBubbleSize-boolean).

 **Examples:** 

Montre comment travailler avec les étiquettes de données d'un graphique à bulles.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setShowCategoryName(boolean value) {#setShowCategoryName-boolean}
```
public void setShowCategoryName(boolean value)
```


Permet de spécifier si le nom de catégorie doit être affiché pour les étiquettes de données de la série entière. La valeur par défaut est false.

 **Remarks:** 

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant la propriété [ChartDataLabel.getShowCategoryName()](../../com.aspose.words/chartdatalabel/\#getShowCategoryName) / [ChartDataLabel.setShowCategoryName(boolean)](../../com.aspose.words/chartdatalabel/\#setShowCategoryName-boolean).

 **Examples:** 

Montre comment travailler avec les étiquettes de données d'un graphique à bulles.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setShowDataLabelsRange(boolean value) {#setShowDataLabelsRange-boolean}
```
public void setShowDataLabelsRange(boolean value)
```


Permet de spécifier si les valeurs de la plage des étiquettes de données doivent être affichées dans les étiquettes de données de la série entière. La valeur par défaut est false.

 **Remarks:** 

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant la propriété [ChartDataLabel.getShowDataLabelsRange()](../../com.aspose.words/chartdatalabel/\#getShowDataLabelsRange) / [ChartDataLabel.setShowDataLabelsRange(boolean)](../../com.aspose.words/chartdatalabel/\#setShowDataLabelsRange-boolean).

 **Examples:** 

Montre comment appliquer des étiquettes aux points de données dans un graphique en courbes.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setShowLeaderLines(boolean value) {#setShowLeaderLines-boolean}
```
public void setShowLeaderLines(boolean value)
```


Permet de spécifier si les lignes de repère des étiquettes de données doivent être affichées pour les étiquettes de données de toute la série. La valeur par défaut est false.

 **Remarks:** 

S'applique uniquement aux graphiques en secteurs. Les lignes de repère créent une connexion visuelle entre une étiquette de données et son point de données correspondant.

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant la propriété [ChartDataLabel.getShowLeaderLines()](../../com.aspose.words/chartdatalabel/\#getShowLeaderLines) / [ChartDataLabel.setShowLeaderLines(boolean)](../../com.aspose.words/chartdatalabel/\#setShowLeaderLines-boolean).

 **Examples:** 

Montre comment travailler avec les étiquettes de données d'un graphique circulaire.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setShowLegendKey(boolean value) {#setShowLegendKey-boolean}
```
public void setShowLegendKey(boolean value)
```


Permet de spécifier si la clé de légende doit être affichée pour les étiquettes de données de toute la série. La valeur par défaut est false.

 **Remarks:** 

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant la propriété [ChartDataLabel.getShowLegendKey()](../../com.aspose.words/chartdatalabel/\#getShowLegendKey) / [ChartDataLabel.setShowLegendKey(boolean)](../../com.aspose.words/chartdatalabel/\#setShowLegendKey-boolean).

 **Examples:** 

Montre comment travailler avec les étiquettes de données d'un graphique circulaire.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setShowPercentage(boolean value) {#setShowPercentage-boolean}
```
public void setShowPercentage(boolean value)
```


Permet de spécifier si la valeur en pourcentage doit être affichée pour les étiquettes de données de toute la série. La valeur par défaut est false. S'applique uniquement aux graphiques en secteurs.

 **Remarks:** 

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant la propriété [ChartDataLabel.getShowPercentage()](../../com.aspose.words/chartdatalabel/\#getShowPercentage) / [ChartDataLabel.setShowPercentage(boolean)](../../com.aspose.words/chartdatalabel/\#setShowPercentage-boolean).

 **Examples:** 

Montre comment travailler avec les étiquettes de données d'un graphique circulaire.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setShowSeriesName(boolean value) {#setShowSeriesName-boolean}
```
public void setShowSeriesName(boolean value)
```


Définit un booléen indiquant le comportement d'affichage du nom de la série pour les étiquettes de données de toute la série. true pour afficher le nom de la série ; false pour le masquer. Par défaut false.

 **Remarks:** 

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant la propriété [ChartDataLabel.getShowSeriesName()](../../com.aspose.words/chartdatalabel/\#getShowSeriesName) / [ChartDataLabel.setShowSeriesName(boolean)](../../com.aspose.words/chartdatalabel/\#setShowSeriesName-boolean).

 **Examples:** 

Montre comment travailler avec les étiquettes de données d'un graphique à bulles.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Un booléen indiquant le comportement d'affichage du nom de la série pour les étiquettes de données de toute la série. |

### setShowValue(boolean value) {#setShowValue-boolean}
```
public void setShowValue(boolean value)
```


Permet de spécifier si les valeurs doivent être affichées dans les étiquettes de données de toute la série. La valeur par défaut est false.

 **Remarks:** 

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant la propriété [ChartDataLabel.getShowValue()](../../com.aspose.words/chartdatalabel/\#getShowValue) / [ChartDataLabel.setShowValue(boolean)](../../com.aspose.words/chartdatalabel/\#setShowValue-boolean).

 **Examples:** 

Montre comment travailler avec les étiquettes de données d'un graphique circulaire.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

