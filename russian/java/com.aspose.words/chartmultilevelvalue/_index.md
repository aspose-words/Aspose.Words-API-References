---
title: "ChartMultilevelValue"
linktitle: "ChartMultilevelValue"
second_title: "Aspose.Words для Java"
description: "Представляет значение для диаграмм, отображающих многоуровневые данные в Java."
type: docs
weight: 83
url: /ru/java/com.aspose.words/chartmultilevelvalue/
---

**Inheritance:**
java.lang.Object
```
public class ChartMultilevelValue
```

Представляет значение для диаграмм, отображающих многоуровневые данные.

 **Examples:** 

Показывает, как создать диаграмму treemap.

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
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [ChartMultilevelValue(String level1, String level2, String level3)](#ChartMultilevelValue-java.lang.String-java.lang.String-java.lang.String) | Инициализирует новый экземпляр этого класса, представляющий трехуровневое значение. |
| [ChartMultilevelValue(String level1, String level2)](#ChartMultilevelValue-java.lang.String-java.lang.String) | Инициализирует новый экземпляр этого класса, представляющий двухуровневое значение. |
| [ChartMultilevelValue(String level1)](#ChartMultilevelValue-java.lang.String) | Инициализирует новый экземпляр этого класса, представляющий одноуровневое значение. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Возвращает флаг, указывающий, равен ли указанный объект текущему объекту многоуровневых данных. |
| [getLevel1()](#getLevel1) | Возвращает название верхнего уровня диаграммы, к которому относится это значение. |
| [getLevel2()](#getLevel2) | Возвращает название промежуточного уровня диаграммы, к которому относится это значение. |
| [getLevel3()](#getLevel3) | Возвращает название нижнего уровня диаграммы, к которому относится это значение. |
| [hashCode()](#hashCode) |  |
### ChartMultilevelValue(String level1, String level2, String level3) {#ChartMultilevelValue-java.lang.String-java.lang.String-java.lang.String}
```
public ChartMultilevelValue(String level1, String level2, String level3)
```


Инициализирует новый экземпляр этого класса, представляющий трехуровневое значение.

 **Examples:** 

Показывает, как создать диаграмму treemap.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| level1 | java.lang.String |  |
| level2 | java.lang.String |  |
| level3 | java.lang.String |  |

### ChartMultilevelValue(String level1, String level2) {#ChartMultilevelValue-java.lang.String-java.lang.String}
```
public ChartMultilevelValue(String level1, String level2)
```


Инициализирует новый экземпляр этого класса, представляющий двухуровневое значение.

 **Examples:** 

Показывает, как создать диаграмму treemap.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| level1 | java.lang.String |  |
| level2 | java.lang.String |  |

### ChartMultilevelValue(String level1) {#ChartMultilevelValue-java.lang.String}
```
public ChartMultilevelValue(String level1)
```


Инициализирует новый экземпляр этого класса, представляющий одноуровневое значение.

 **Examples:** 

Показывает, как создать диаграмму treemap.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| level1 | java.lang.String |  |

### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Возвращает флаг, указывающий, равен ли указанный объект текущему объекту многоуровневых данных.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getLevel1() {#getLevel1}
```
public String getLevel1()
```


Возвращает название верхнего уровня диаграммы, к которому относится это значение.

**Returns:**
java.lang.String - Имя верхнего уровня диаграммы, к которому относится это значение.
### getLevel2() {#getLevel2}
```
public String getLevel2()
```


Возвращает название промежуточного уровня диаграммы, к которому относится это значение.

**Returns:**
java.lang.String - Имя промежуточного уровня диаграммы, к которому относится это значение.
### getLevel3() {#getLevel3}
```
public String getLevel3()
```


Возвращает название нижнего уровня диаграммы, к которому относится это значение.

**Returns:**
java.lang.String - Имя нижнего уровня диаграммы, к которому относится это значение.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
