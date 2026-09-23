---
title: "BubbleSizeCollection"
linktitle: "BubbleSizeCollection"
second_title: "Aspose.Words pour Java"
description: "Représente une collection de tailles de bulles pour une série de graphique en Java."
type: docs
weight: 50
url: /fr/java/com.aspose.words/bubblesizecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class BubbleSizeCollection implements Iterable
```

Représente une collection de tailles de bulles pour une série de graphique.

 **Remarks:** 

La collection ne permet que de modifier les tailles de bulles. Pour ajouter ou insérer de nouvelles valeurs à une série de graphique, ou supprimer des valeurs, les méthodes appropriées de la classe [ChartSeries](../../com.aspose.words/chartseries/) peuvent être utilisées.

Les valeurs de taille de bulle vides sont représentées par double\#NA\_N.NA\_N.
## Méthodes

| Méthode | Description |
| --- | --- |
| [get(int index)](#get-int) | Obtient la valeur de taille de bulle à l'index spécifié. |
| [getCount()](#getCount) | Obtient le nombre d'éléments dans cette collection. |
| [getFormatCode()](#getFormatCode) | Obtient le code de format appliqué aux tailles de bulles. |
| [iterator()](#iterator) | Renvoie un objet énumérateur. |
| [set(int index, double value)](#set-int-double) | Définit la valeur de taille de bulle à l'index spécifié. |
| [setFormatCode(String value)](#setFormatCode-java.lang.String) | Définit le code de format appliqué aux tailles de bulles. |
### get(int index) {#get-int}
```
public double get(int index)
```


Obtient la valeur de taille de bulle à l'index spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
double - La valeur de taille de bulle à l'index spécifié.
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


Obtient le code de format appliqué aux tailles de bulles.

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
java.lang.String - Le code de format appliqué aux tailles de bulles.
### iterator() {#iterator}
```
public Iterator iterator()
```


Renvoie un objet énumérateur.

**Returns:**
java.util.Iterator
### set(int index, double value) {#set-int-double}
```
public void set(int index, double value)
```


Définit la valeur de taille de bulle à l'index spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int |  |
| valeur | double | La valeur de taille de bulle à l'index spécifié. |

### setFormatCode(String value) {#setFormatCode-java.lang.String}
```
public void setFormatCode(String value)
```


Définit le code de format appliqué aux tailles de bulles.

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
| valeur | java.lang.String | Le code de format appliqué aux tailles de bulles. |

