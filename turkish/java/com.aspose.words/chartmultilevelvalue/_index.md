---
title: "ChartMultilevelValue"
linktitle: "ChartMultilevelValue"
second_title: "Aspose.Words Java için"
description: "Java'da çok seviyeli verileri gösteren grafikler için bir değeri temsil eder."
type: docs
weight: 83
url: /tr/java/com.aspose.words/chartmultilevelvalue/
---

**Inheritance:**
java.lang.Object
```
public class ChartMultilevelValue
```

Çok seviyeli verileri gösteren grafikler için bir değeri temsil eder.

 **Examples:** 

Ağaç haritası grafiği oluşturmayı gösterir.

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
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [ChartMultilevelValue(String level1, String level2, String level3)](#ChartMultilevelValue-java.lang.String-java.lang.String-java.lang.String) | Üç seviyeli bir değeri temsil eden bu sınıfın yeni bir örneğini başlatır. |
| [ChartMultilevelValue(String level1, String level2)](#ChartMultilevelValue-java.lang.String-java.lang.String) | İki seviyeli bir değeri temsil eden bu sınıfın yeni bir örneğini başlatır. |
| [ChartMultilevelValue(String level1)](#ChartMultilevelValue-java.lang.String) | Tek seviyeli bir değeri temsil eden bu sınıfın yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Belirtilen nesnenin mevcut çok seviyeli veri nesnesine eşit olup olmadığını gösteren bir bayrağı alır. |
| [getLevel1()](#getLevel1) | Bu değerin referans verdiği grafiğin üst seviyesinin adını alır. |
| [getLevel2()](#getLevel2) | Bu değerin referans verdiği grafiğin ara seviyesinin adını alır. |
| [getLevel3()](#getLevel3) | Bu değerin referans verdiği grafiğin alt seviyesinin adını alır. |
| [hashCode()](#hashCode) |  |
### ChartMultilevelValue(String level1, String level2, String level3) {#ChartMultilevelValue-java.lang.String-java.lang.String-java.lang.String}
```
public ChartMultilevelValue(String level1, String level2, String level3)
```


Üç seviyeli bir değeri temsil eden bu sınıfın yeni bir örneğini başlatır.

 **Examples:** 

Ağaç haritası grafiği oluşturmayı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| level1 | java.lang.String |  |
| level2 | java.lang.String |  |
| level3 | java.lang.String |  |

### ChartMultilevelValue(String level1, String level2) {#ChartMultilevelValue-java.lang.String-java.lang.String}
```
public ChartMultilevelValue(String level1, String level2)
```


İki seviyeli bir değeri temsil eden bu sınıfın yeni bir örneğini başlatır.

 **Examples:** 

Ağaç haritası grafiği oluşturmayı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| level1 | java.lang.String |  |
| level2 | java.lang.String |  |

### ChartMultilevelValue(String level1) {#ChartMultilevelValue-java.lang.String}
```
public ChartMultilevelValue(String level1)
```


Tek seviyeli bir değeri temsil eden bu sınıfın yeni bir örneğini başlatır.

 **Examples:** 

Ağaç haritası grafiği oluşturmayı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| level1 | java.lang.String |  |

### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Belirtilen nesnenin mevcut çok seviyeli veri nesnesine eşit olup olmadığını gösteren bir bayrağı alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getLevel1() {#getLevel1}
```
public String getLevel1()
```


Bu değerin referans verdiği grafiğin üst seviyesinin adını alır.

**Returns:**
java.lang.String - Bu değerin referans verdiği grafik üst seviyesinin adı.
### getLevel2() {#getLevel2}
```
public String getLevel2()
```


Bu değerin referans verdiği grafiğin ara seviyesinin adını alır.

**Returns:**
java.lang.String - Bu değerin referans verdiği grafik ara seviyesinin adı.
### getLevel3() {#getLevel3}
```
public String getLevel3()
```


Bu değerin referans verdiği grafiğin alt seviyesinin adını alır.

**Returns:**
java.lang.String - Bu değerin referans verdiği grafik alt seviyesinin adı.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
