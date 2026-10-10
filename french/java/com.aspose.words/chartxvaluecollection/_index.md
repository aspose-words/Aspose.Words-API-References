---
title: "ChartXValueCollection"
linktitle: "ChartXValueCollection"
second_title: "Aspose.Words pour Java"
description: "Représente une collection de valeurs X pour une série de graphique en Java."
type: docs
weight: 95
url: /fr/java/com.aspose.words/chartxvaluecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartXValueCollection implements Iterable
```

Représente une collection de valeurs X pour une série de graphique.

 **Remarks:** 

Tous les éléments de la collection, à l'exception de **null**, doivent avoir le même [ChartXValue.getValueType()](../../com.aspose.words/chartxvalue/\#getValueType).

La collection ne permet que la modification des valeurs X. Pour ajouter ou insérer de nouvelles valeurs dans une série de graphique, ou supprimer des valeurs, les méthodes appropriées de la classe [ChartSeries](../../com.aspose.words/chartseries/) peuvent être utilisées.

 **Examples:** 

Montre comment obtenir les données d'une série de graphique.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [get(int index)](#get-int) | Obtient la valeur X à l'index spécifié. |
| [getCount()](#getCount) | Obtient le nombre d'éléments dans cette collection. |
| [getFormatCode()](#getFormatCode) | Obtient le code de format appliqué aux valeurs X. |
| [iterator()](#iterator) | Renvoie un objet énumérateur. |
| [set(int index, ChartXValue value)](#set-int-com.aspose.words.ChartXValue) | Définit la valeur X à l'index spécifié. |
| [setFormatCode(String value)](#setFormatCode-java.lang.String) | Définit le code de format appliqué aux valeurs X. |
### get(int index) {#get-int}
```
public ChartXValue get(int index)
```


Obtient la valeur X à l'index spécifié.

 **Remarks:** 

Les valeurs vides sont représentées par **null**.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/) - The X value at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Obtient le nombre d'éléments dans cette collection.

**Returns:**
int - Le nombre d'éléments dans cette collection.
### getFormatCode() {#getFormatCode}
```
public String getFormatCode()
```


Obtient le code de format appliqué aux valeurs X.

 **Remarks:** 

Le formatage des nombres est utilisé pour modifier la façon dont les valeurs apparaissent dans le graphique. Voici des exemples de formats numériques :

Nombre - "\#,\#\#0.00"

Monnaie - "\\"$\\"\#,\#\#0.00"

Heure - "[$-x-systime]h:mm:ss AM/PM"

Date - "d/mm/yyyy"

Pourcentage - "0.00%"

Fraction - "\# ?/?"

Scientifique - "0.00E+00"

Comptable - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

Personnalisé avec couleur - "[Red]-\#,\#\#0.0"

 **Examples:** 

Montre comment travailler avec le code de format des données du graphique.

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
java.lang.String - Le code de format appliqué aux valeurs X.
### iterator() {#iterator}
```
public Iterator iterator()
```


Renvoie un objet énumérateur.

**Returns:**
java.util.Iterator
### set(int index, ChartXValue value) {#set-int-com.aspose.words.ChartXValue}
```
public void set(int index, ChartXValue value)
```


Définit la valeur X à l'index spécifié.

 **Remarks:** 

Les valeurs vides sont représentées par **null**.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int |  |
| value | [ChartXValue](../../com.aspose.words/chartxvalue/) | La valeur X à l'index spécifié. |

### setFormatCode(String value) {#setFormatCode-java.lang.String}
```
public void setFormatCode(String value)
```


Définit le code de format appliqué aux valeurs X.

 **Remarks:** 

Le formatage des nombres est utilisé pour modifier la façon dont les valeurs apparaissent dans le graphique. Voici des exemples de formats numériques :

Nombre - "\#,\#\#0.00"

Monnaie - "\\"$\\"\#,\#\#0.00"

Heure - "[$-x-systime]h:mm:ss AM/PM"

Date - "d/mm/yyyy"

Pourcentage - "0.00%"

Fraction - "\# ?/?"

Scientifique - "0.00E+00"

Comptable - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

Personnalisé avec couleur - "[Red]-\#,\#\#0.0"

 **Examples:** 

Montre comment travailler avec le code de format des données du graphique.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Le code de format appliqué aux valeurs X. |

