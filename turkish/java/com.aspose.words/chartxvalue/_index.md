---
title: "ChartXValue"
linktitle: "ChartXValue"
second_title: "Aspose.Words Java için"
description: "Java'da bir grafik serisi için X değerini temsil eder."
type: docs
weight: 94
url: /tr/java/com.aspose.words/chartxvalue/
---

**Inheritance:**
java.lang.Object
```
public class ChartXValue
```

Bir grafik serisi için X değerini temsil eder.

 **Remarks:** 

Bu sınıf, belirli bir türde X değeri oluşturmak için bir dizi statik yöntem içerir. [getValueType()](../../com.aspose.words/chartxvalue/\#getValueType) özelliği, mevcut bir X değerinin türünü belirlemenizi sağlar.

Bir grafik serisinin tüm null olmayan X değerleri aynı [ChartXValueType](../../com.aspose.words/chartxvaluetype/) türünde olmalıdır.

 **Examples:** 

Grafik serisini veriyle nasıl doldurulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries series1 = chart.getSeries().get(0);

 // Clear X and Y values of the first series.
 series1.clearValues();

 // Populate the series with data.
 series1.add(ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0), 10.0);
 series1.add(ChartXValue.fromDouble(5.0), ChartYValue.fromDouble(5.0));
 series1.add(ChartXValue.fromDouble(7.0), ChartYValue.fromDouble(11.0));
 series1.add(ChartXValue.fromDouble(9.0));

 ChartSeries series2 = chart.getSeries().get(1);

 // Clear X and Y values of the second series.
 series2.clear();

 // Populate the series with data.
 series2.add(ChartXValue.fromDouble(2.0), ChartYValue.fromDouble(4.0));
 series2.add(ChartXValue.fromDouble(4.0), ChartYValue.fromDouble(7.0));
 series2.add(ChartXValue.fromDouble(6.0), ChartYValue.fromDouble(14.0));
 series2.add(ChartXValue.fromDouble(8.0), ChartYValue.fromDouble(7.0));

 doc.save(getArtifactsDir() + "Charts.PopulateChartWithData.docx");
 
```
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Belirtilen nesnenin mevcut X değeri nesnesine eşit olup olmadığını gösteren bir bayrak döndürür. |
| [fromDateTime(Date value)](#fromDateTime-java.util.Date) | [ChartXValueType.DATE\_TIME](../../com.aspose.words/chartxvaluetype/\#DATE-TIME) türünde bir [ChartXValue](../../com.aspose.words/chartxvalue/) örneği oluşturur. |
| [fromDouble(double value)](#fromDouble-double) | [ChartXValueType.DOUBLE](../../com.aspose.words/chartxvaluetype/\#DOUBLE) türünde bir [ChartXValue](../../com.aspose.words/chartxvalue/) örneği oluşturur. |
| [fromMultilevelValue(ChartMultilevelValue value)](#fromMultilevelValue-com.aspose.words.ChartMultilevelValue) | [ChartXValueType.MULTILEVEL](../../com.aspose.words/chartxvaluetype/\#MULTILEVEL) türünde bir [ChartXValue](../../com.aspose.words/chartxvalue/) örneği oluşturur. |
| [fromString(String value)](#fromString-java.lang.String) | [ChartXValueType.STRING](../../com.aspose.words/chartxvaluetype/\#STRING) türünde bir [ChartXValue](../../com.aspose.words/chartxvalue/) örneği oluşturur. |
| [fromTimeSpan(long value)](#fromTimeSpan-long) | [ChartXValueType.TIME](../../com.aspose.words/chartxvaluetype/\#TIME) türünde bir [ChartXValue](../../com.aspose.words/chartxvalue/) örneği oluşturur. |
| [getDateTimeValue()](#getDateTimeValue) | Depolanan datetime değerini alır. |
| [getDoubleValue()](#getDoubleValue) | Depolanan sayısal değeri alır. |
| [getMultilevelValue()](#getMultilevelValue) | Depolanan çok seviyeli değeri alır. |
| [getStringValue()](#getStringValue) | Depolanan dize değerini alır. |
| [getTimeValue()](#getTimeValue) | Depolanan zaman değerini alır. |
| [getValueType()](#getValueType) | Nesnede depolanan X değerinin türünü alır. |
| [hashCode()](#hashCode) |  |
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Belirtilen nesnenin mevcut X değeri nesnesine eşit olup olmadığını gösteren bir bayrak döndürür.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### fromDateTime(Date value) {#fromDateTime-java.util.Date}
```
public static ChartXValue fromDateTime(Date value)
```


[ChartXValueType.DATE\_TIME](../../com.aspose.words/chartxvaluetype/\#DATE-TIME) türünde bir [ChartXValue](../../com.aspose.words/chartxvalue/) örneği oluşturur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.util.Date |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromDouble(double value) {#fromDouble-double}
```
public static ChartXValue fromDouble(double value)
```


[ChartXValueType.DOUBLE](../../com.aspose.words/chartxvaluetype/\#DOUBLE) türünde bir [ChartXValue](../../com.aspose.words/chartxvalue/) örneği oluşturur.

 **Examples:** 

Grafik serisini veriyle nasıl doldurulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries series1 = chart.getSeries().get(0);

 // Clear X and Y values of the first series.
 series1.clearValues();

 // Populate the series with data.
 series1.add(ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0), 10.0);
 series1.add(ChartXValue.fromDouble(5.0), ChartYValue.fromDouble(5.0));
 series1.add(ChartXValue.fromDouble(7.0), ChartYValue.fromDouble(11.0));
 series1.add(ChartXValue.fromDouble(9.0));

 ChartSeries series2 = chart.getSeries().get(1);

 // Clear X and Y values of the second series.
 series2.clear();

 // Populate the series with data.
 series2.add(ChartXValue.fromDouble(2.0), ChartYValue.fromDouble(4.0));
 series2.add(ChartXValue.fromDouble(4.0), ChartYValue.fromDouble(7.0));
 series2.add(ChartXValue.fromDouble(6.0), ChartYValue.fromDouble(14.0));
 series2.add(ChartXValue.fromDouble(8.0), ChartYValue.fromDouble(7.0));

 doc.save(getArtifactsDir() + "Charts.PopulateChartWithData.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromMultilevelValue(ChartMultilevelValue value) {#fromMultilevelValue-com.aspose.words.ChartMultilevelValue}
```
public static ChartXValue fromMultilevelValue(ChartMultilevelValue value)
```


[ChartXValueType.MULTILEVEL](../../com.aspose.words/chartxvaluetype/\#MULTILEVEL) türünde bir [ChartXValue](../../com.aspose.words/chartxvalue/) örneği oluşturur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [ChartMultilevelValue](../../com.aspose.words/chartmultilevelvalue/) |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromString(String value) {#fromString-java.lang.String}
```
public static ChartXValue fromString(String value)
```


[ChartXValueType.STRING](../../com.aspose.words/chartxvaluetype/\#STRING) türünde bir [ChartXValue](../../com.aspose.words/chartxvalue/) örneği oluşturur.

 **Examples:** 

Grafik veri değerlerini ekleme/kaldırma işlemlerinin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder();

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries department1Series = chart.getSeries().get(0);
 ChartSeries department2Series = chart.getSeries().get(1);

 // Remove the first value in the both series.
 department1Series.remove(0);
 department2Series.remove(0);

 // Add new values to the both series.
 ChartXValue newXCategory = ChartXValue.fromString("Q1, 2023");
 department1Series.add(newXCategory, ChartYValue.fromDouble(10.3));
 department2Series.add(newXCategory, ChartYValue.fromDouble(5.7));

 doc.save(getArtifactsDir() + "Charts.ChartDataValues.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromTimeSpan(long value) {#fromTimeSpan-long}
```
public static ChartXValue fromTimeSpan(long value)
```


[ChartXValueType.TIME](../../com.aspose.words/chartxvaluetype/\#TIME) türünde bir [ChartXValue](../../com.aspose.words/chartxvalue/) örneği oluşturur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | long |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### getDateTimeValue() {#getDateTimeValue}
```
public Date getDateTimeValue()
```


Depolanan datetime değerini alır.

**Returns:**
java.util.Date - Depolanan tarih saat değeri.
### getDoubleValue() {#getDoubleValue}
```
public double getDoubleValue()
```


Depolanan sayısal değeri alır.

**Returns:**
double - Depolanan sayısal değer.
### getMultilevelValue() {#getMultilevelValue}
```
public ChartMultilevelValue getMultilevelValue()
```


Depolanan çok seviyeli değeri alır.

**Returns:**
[ChartMultilevelValue](../../com.aspose.words/chartmultilevelvalue/) - The stored multilevel value.
### getStringValue() {#getStringValue}
```
public String getStringValue()
```


Depolanan dize değerini alır.

**Returns:**
java.lang.String - Depolanan dize değeri.
### getTimeValue() {#getTimeValue}
```
public long getTimeValue()
```


Depolanan zaman değerini alır.

**Returns:**
long - Depolanan zaman değeri.
### getValueType() {#getValueType}
```
public int getValueType()
```


Nesnede depolanan X değerinin türünü alır.

**Returns:**
int - Nesnede depolanan X değerinin türü. Döndürülen değer, [ChartXValueType](../../com.aspose.words/chartxvaluetype/) sabitlerinden biridir.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
