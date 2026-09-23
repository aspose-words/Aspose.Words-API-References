---
title: "ChartMultilevelValue"
linktitle: "ChartMultilevelValue"
second_title: "Aspose.Words pour Java"
description: "Représente une valeur pour les graphiques affichant des données multiniveaux en Java."
type: docs
weight: 83
url: /fr/java/com.aspose.words/chartmultilevelvalue/
---

**Inheritance:**
java.lang.Object
```
public class ChartMultilevelValue
```

Représente une valeur pour les graphiques affichant des données à plusieurs niveaux.

 **Examples:** 

Montre comment créer un graphique en arbre.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Treemap chart.
 Shape shape = builder.insertChart(ChartType.TREEMAP, 450.0, 280.0);
 Chart chart = shape.getChart();
 chart.getTitle().setText("World Population");

 // Delete default generated series.
 chart.getSeries().clear();

 // Add a series.
 ChartSeries series = chart.getSeries().add(
         "Population by Region",
         new ChartMultilevelValue[]
                 {
                         new ChartMultilevelValue("Asia", "China"),
                         new ChartMultilevelValue("Asia", "India"),
                         new ChartMultilevelValue("Asia", "Indonesia"),
                         new ChartMultilevelValue("Asia", "Pakistan"),
                         new ChartMultilevelValue("Asia", "Bangladesh"),
                         new ChartMultilevelValue("Asia", "Japan"),
                         new ChartMultilevelValue("Asia", "Philippines"),
                         new ChartMultilevelValue("Asia", "Other"),
                         new ChartMultilevelValue("Africa", "Nigeria"),
                         new ChartMultilevelValue("Africa", "Ethiopia"),
                         new ChartMultilevelValue("Africa", "Egypt"),
                         new ChartMultilevelValue("Africa", "Other"),
                         new ChartMultilevelValue("Europe", "Russia"),
                         new ChartMultilevelValue("Europe", "Germany"),
                         new ChartMultilevelValue("Europe", "Other"),
                         new ChartMultilevelValue("Latin America", "Brazil"),
                         new ChartMultilevelValue("Latin America", "Mexico"),
                         new ChartMultilevelValue("Latin America", "Other"),
                         new ChartMultilevelValue("Northern America", "United States", "Other"),
                         new ChartMultilevelValue("Northern America", "Other"),
                         new ChartMultilevelValue("Oceania")
                 },
         new double[]
                 {
                         1409670000.0, 1400744000.0, 279118866.0, 241499431.0, 169828911.0, 123930000.0, 112892781.0, 764000000.0,
                         223800000.0, 107334000.0, 105914499.0, 903000000.0,
                         146150789.0, 84607016.0, 516000000.0,
                         203080756.0, 129713690.0, 310000000.0,
                         335893238.0, 35000000.0,
                         42000000.0
                 });

 // Show data labels.
 series.hasDataLabels(true);
 series.getDataLabels().setShowValue(true);
 series.getDataLabels().setShowCategoryName(true);
 DecimalFormatSymbols symbols = new DecimalFormatSymbols(Locale.getDefault());
 String thousandSeparator = Character.toString(symbols.getGroupingSeparator());
 series.getDataLabels().getNumberFormat().setFormatCode(String.format("#{0}0", thousandSeparator));

 doc.save(getArtifactsDir() + "Charts.Treemap.docx");
 
```
## Constructors

| Constructor | Description |
| --- | --- |
| [ChartMultilevelValue(String level1, String level2, String level3)](#ChartMultilevelValue-java.lang.String-java.lang.String-java.lang.String) | Initialise une nouvelle instance de cette classe qui représente une valeur à trois niveaux. |
| [ChartMultilevelValue(String level1, String level2)](#ChartMultilevelValue-java.lang.String-java.lang.String) | Initialise une nouvelle instance de cette classe qui représente une valeur à deux niveaux. |
| [ChartMultilevelValue(String level1)](#ChartMultilevelValue-java.lang.String) | Initialise une nouvelle instance de cette classe qui représente une valeur à un seul niveau. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Obtient un indicateur indiquant si l'objet spécifié est égal à l'objet de données multiniveaux actuel. |
| [getLevel1()](#getLevel1) | Obtient le nom du niveau supérieur du graphique auquel cette valeur se réfère. |
| [getLevel2()](#getLevel2) | Obtient le nom du niveau intermédiaire du graphique auquel cette valeur se réfère. |
| [getLevel3()](#getLevel3) | Obtient le nom du niveau inférieur du graphique auquel cette valeur se réfère. |
| [hashCode()](#hashCode) |  |
### ChartMultilevelValue(String level1, String level2, String level3) {#ChartMultilevelValue-java.lang.String-java.lang.String-java.lang.String}
```
public ChartMultilevelValue(String level1, String level2, String level3)
```


Initialise une nouvelle instance de cette classe qui représente une valeur à trois niveaux.

 **Examples:** 

Montre comment créer un graphique en arbre.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Treemap chart.
 Shape shape = builder.insertChart(ChartType.TREEMAP, 450.0, 280.0);
 Chart chart = shape.getChart();
 chart.getTitle().setText("World Population");

 // Delete default generated series.
 chart.getSeries().clear();

 // Add a series.
 ChartSeries series = chart.getSeries().add(
         "Population by Region",
         new ChartMultilevelValue[]
                 {
                         new ChartMultilevelValue("Asia", "China"),
                         new ChartMultilevelValue("Asia", "India"),
                         new ChartMultilevelValue("Asia", "Indonesia"),
                         new ChartMultilevelValue("Asia", "Pakistan"),
                         new ChartMultilevelValue("Asia", "Bangladesh"),
                         new ChartMultilevelValue("Asia", "Japan"),
                         new ChartMultilevelValue("Asia", "Philippines"),
                         new ChartMultilevelValue("Asia", "Other"),
                         new ChartMultilevelValue("Africa", "Nigeria"),
                         new ChartMultilevelValue("Africa", "Ethiopia"),
                         new ChartMultilevelValue("Africa", "Egypt"),
                         new ChartMultilevelValue("Africa", "Other"),
                         new ChartMultilevelValue("Europe", "Russia"),
                         new ChartMultilevelValue("Europe", "Germany"),
                         new ChartMultilevelValue("Europe", "Other"),
                         new ChartMultilevelValue("Latin America", "Brazil"),
                         new ChartMultilevelValue("Latin America", "Mexico"),
                         new ChartMultilevelValue("Latin America", "Other"),
                         new ChartMultilevelValue("Northern America", "United States", "Other"),
                         new ChartMultilevelValue("Northern America", "Other"),
                         new ChartMultilevelValue("Oceania")
                 },
         new double[]
                 {
                         1409670000.0, 1400744000.0, 279118866.0, 241499431.0, 169828911.0, 123930000.0, 112892781.0, 764000000.0,
                         223800000.0, 107334000.0, 105914499.0, 903000000.0,
                         146150789.0, 84607016.0, 516000000.0,
                         203080756.0, 129713690.0, 310000000.0,
                         335893238.0, 35000000.0,
                         42000000.0
                 });

 // Show data labels.
 series.hasDataLabels(true);
 series.getDataLabels().setShowValue(true);
 series.getDataLabels().setShowCategoryName(true);
 DecimalFormatSymbols symbols = new DecimalFormatSymbols(Locale.getDefault());
 String thousandSeparator = Character.toString(symbols.getGroupingSeparator());
 series.getDataLabels().getNumberFormat().setFormatCode(String.format("#{0}0", thousandSeparator));

 doc.save(getArtifactsDir() + "Charts.Treemap.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| level1 | java.lang.String |  |
| level2 | java.lang.String |  |
| level3 | java.lang.String |  |

### ChartMultilevelValue(String level1, String level2) {#ChartMultilevelValue-java.lang.String-java.lang.String}
```
public ChartMultilevelValue(String level1, String level2)
```


Initialise une nouvelle instance de cette classe qui représente une valeur à deux niveaux.

 **Examples:** 

Montre comment créer un graphique en arbre.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Treemap chart.
 Shape shape = builder.insertChart(ChartType.TREEMAP, 450.0, 280.0);
 Chart chart = shape.getChart();
 chart.getTitle().setText("World Population");

 // Delete default generated series.
 chart.getSeries().clear();

 // Add a series.
 ChartSeries series = chart.getSeries().add(
         "Population by Region",
         new ChartMultilevelValue[]
                 {
                         new ChartMultilevelValue("Asia", "China"),
                         new ChartMultilevelValue("Asia", "India"),
                         new ChartMultilevelValue("Asia", "Indonesia"),
                         new ChartMultilevelValue("Asia", "Pakistan"),
                         new ChartMultilevelValue("Asia", "Bangladesh"),
                         new ChartMultilevelValue("Asia", "Japan"),
                         new ChartMultilevelValue("Asia", "Philippines"),
                         new ChartMultilevelValue("Asia", "Other"),
                         new ChartMultilevelValue("Africa", "Nigeria"),
                         new ChartMultilevelValue("Africa", "Ethiopia"),
                         new ChartMultilevelValue("Africa", "Egypt"),
                         new ChartMultilevelValue("Africa", "Other"),
                         new ChartMultilevelValue("Europe", "Russia"),
                         new ChartMultilevelValue("Europe", "Germany"),
                         new ChartMultilevelValue("Europe", "Other"),
                         new ChartMultilevelValue("Latin America", "Brazil"),
                         new ChartMultilevelValue("Latin America", "Mexico"),
                         new ChartMultilevelValue("Latin America", "Other"),
                         new ChartMultilevelValue("Northern America", "United States", "Other"),
                         new ChartMultilevelValue("Northern America", "Other"),
                         new ChartMultilevelValue("Oceania")
                 },
         new double[]
                 {
                         1409670000.0, 1400744000.0, 279118866.0, 241499431.0, 169828911.0, 123930000.0, 112892781.0, 764000000.0,
                         223800000.0, 107334000.0, 105914499.0, 903000000.0,
                         146150789.0, 84607016.0, 516000000.0,
                         203080756.0, 129713690.0, 310000000.0,
                         335893238.0, 35000000.0,
                         42000000.0
                 });

 // Show data labels.
 series.hasDataLabels(true);
 series.getDataLabels().setShowValue(true);
 series.getDataLabels().setShowCategoryName(true);
 DecimalFormatSymbols symbols = new DecimalFormatSymbols(Locale.getDefault());
 String thousandSeparator = Character.toString(symbols.getGroupingSeparator());
 series.getDataLabels().getNumberFormat().setFormatCode(String.format("#{0}0", thousandSeparator));

 doc.save(getArtifactsDir() + "Charts.Treemap.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| level1 | java.lang.String |  |
| level2 | java.lang.String |  |

### ChartMultilevelValue(String level1) {#ChartMultilevelValue-java.lang.String}
```
public ChartMultilevelValue(String level1)
```


Initialise une nouvelle instance de cette classe qui représente une valeur à un seul niveau.

 **Examples:** 

Montre comment créer un graphique en arbre.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Treemap chart.
 Shape shape = builder.insertChart(ChartType.TREEMAP, 450.0, 280.0);
 Chart chart = shape.getChart();
 chart.getTitle().setText("World Population");

 // Delete default generated series.
 chart.getSeries().clear();

 // Add a series.
 ChartSeries series = chart.getSeries().add(
         "Population by Region",
         new ChartMultilevelValue[]
                 {
                         new ChartMultilevelValue("Asia", "China"),
                         new ChartMultilevelValue("Asia", "India"),
                         new ChartMultilevelValue("Asia", "Indonesia"),
                         new ChartMultilevelValue("Asia", "Pakistan"),
                         new ChartMultilevelValue("Asia", "Bangladesh"),
                         new ChartMultilevelValue("Asia", "Japan"),
                         new ChartMultilevelValue("Asia", "Philippines"),
                         new ChartMultilevelValue("Asia", "Other"),
                         new ChartMultilevelValue("Africa", "Nigeria"),
                         new ChartMultilevelValue("Africa", "Ethiopia"),
                         new ChartMultilevelValue("Africa", "Egypt"),
                         new ChartMultilevelValue("Africa", "Other"),
                         new ChartMultilevelValue("Europe", "Russia"),
                         new ChartMultilevelValue("Europe", "Germany"),
                         new ChartMultilevelValue("Europe", "Other"),
                         new ChartMultilevelValue("Latin America", "Brazil"),
                         new ChartMultilevelValue("Latin America", "Mexico"),
                         new ChartMultilevelValue("Latin America", "Other"),
                         new ChartMultilevelValue("Northern America", "United States", "Other"),
                         new ChartMultilevelValue("Northern America", "Other"),
                         new ChartMultilevelValue("Oceania")
                 },
         new double[]
                 {
                         1409670000.0, 1400744000.0, 279118866.0, 241499431.0, 169828911.0, 123930000.0, 112892781.0, 764000000.0,
                         223800000.0, 107334000.0, 105914499.0, 903000000.0,
                         146150789.0, 84607016.0, 516000000.0,
                         203080756.0, 129713690.0, 310000000.0,
                         335893238.0, 35000000.0,
                         42000000.0
                 });

 // Show data labels.
 series.hasDataLabels(true);
 series.getDataLabels().setShowValue(true);
 series.getDataLabels().setShowCategoryName(true);
 DecimalFormatSymbols symbols = new DecimalFormatSymbols(Locale.getDefault());
 String thousandSeparator = Character.toString(symbols.getGroupingSeparator());
 series.getDataLabels().getNumberFormat().setFormatCode(String.format("#{0}0", thousandSeparator));

 doc.save(getArtifactsDir() + "Charts.Treemap.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| level1 | java.lang.String |  |

### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Obtient un indicateur indiquant si l'objet spécifié est égal à l'objet de données multiniveaux actuel.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getLevel1() {#getLevel1}
```
public String getLevel1()
```


Obtient le nom du niveau supérieur du graphique auquel cette valeur se réfère.

**Returns:**
java.lang.String - Le nom du niveau supérieur du graphique auquel cette valeur fait référence.
### getLevel2() {#getLevel2}
```
public String getLevel2()
```


Obtient le nom du niveau intermédiaire du graphique auquel cette valeur se réfère.

**Returns:**
java.lang.String - Le nom du niveau intermédiaire du graphique auquel cette valeur fait référence.
### getLevel3() {#getLevel3}
```
public String getLevel3()
```


Obtient le nom du niveau inférieur du graphique auquel cette valeur se réfère.

**Returns:**
java.lang.String - Le nom du niveau inférieur du graphique auquel cette valeur fait référence.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
