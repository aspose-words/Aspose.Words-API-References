---
title: "ChartYValue"
linktitle: "ChartYValue"
second_title: "Aspose.Words Java için"
description: "Java'da bir grafik serisi için Y değerini temsil eder."
type: docs
weight: 97
url: /tr/java/com.aspose.words/chartyvalue/
---

**Inheritance:**
java.lang.Object
```
public class ChartYValue
```

Bir grafik serisi için Y değerini temsil eder.

 **Remarks:** 

Bu sınıf, belirli bir tipte Y değeri oluşturmak için bir dizi statik yöntem içerir. [getValueType()](../../com.aspose.words/chartyvalue/\#getValueType) özelliği, mevcut bir Y değerinin tipini belirlemenizi sağlar.

Bir grafik serisinin tüm null olmayan Y değerleri aynı [ChartYValueType](../../com.aspose.words/chartyvaluetype/) tipinde olmalıdır.
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Belirtilen nesnenin mevcut Y değeri nesnesine eşit olup olmadığını gösteren bir bayrak döndürür. |
| [fromDateTime(Date value)](#fromDateTime-java.util.Date) | [ChartYValueType.DATE\_TIME](../../com.aspose.words/chartyvaluetype/\#DATE-TIME) tipinde bir [ChartYValue](../../com.aspose.words/chartyvalue/) örneği oluşturur. |
| [fromDouble(double value)](#fromDouble-double) | [ChartYValueType.DOUBLE](../../com.aspose.words/chartyvaluetype/\#DOUBLE) tipinde bir [ChartYValue](../../com.aspose.words/chartyvalue/) örneği oluşturur. |
| [fromTimeSpan(long value)](#fromTimeSpan-long) | [ChartYValueType.TIME](../../com.aspose.words/chartyvaluetype/\#TIME) tipinde bir [ChartYValue](../../com.aspose.words/chartyvalue/) örneği oluşturur. |
| [getDateTimeValue()](#getDateTimeValue) | Depolanan datetime değerini alır. |
| [getDoubleValue()](#getDoubleValue) | Depolanan sayısal değeri alır. |
| [getTimeValue()](#getTimeValue) | Depolanan zaman değerini alır. |
| [getValueType()](#getValueType) | Nesnede depolanan Y değerinin tipini alır. |
| [hashCode()](#hashCode) |  |
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Belirtilen nesnenin mevcut Y değeri nesnesine eşit olup olmadığını gösteren bir bayrak döndürür.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### fromDateTime(Date value) {#fromDateTime-java.util.Date}
```
public static ChartYValue fromDateTime(Date value)
```


[ChartYValueType.DATE\_TIME](../../com.aspose.words/chartyvaluetype/\#DATE-TIME) tipinde bir [ChartYValue](../../com.aspose.words/chartyvalue/) örneği oluşturur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.util.Date |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/)
### fromDouble(double value) {#fromDouble-double}
```
public static ChartYValue fromDouble(double value)
```


[ChartYValueType.DOUBLE](../../com.aspose.words/chartyvaluetype/\#DOUBLE) tipinde bir [ChartYValue](../../com.aspose.words/chartyvalue/) örneği oluşturur.

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
[ChartYValue](../../com.aspose.words/chartyvalue/)
### fromTimeSpan(long value) {#fromTimeSpan-long}
```
public static ChartYValue fromTimeSpan(long value)
```


[ChartYValueType.TIME](../../com.aspose.words/chartyvaluetype/\#TIME) tipinde bir [ChartYValue](../../com.aspose.words/chartyvalue/) örneği oluşturur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | long |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/)
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


Nesnede depolanan Y değerinin tipini alır.

**Returns:**
int - Nesnede depolanan Y değerinin tipi. Döndürülen değer, [ChartYValueType](../../com.aspose.words/chartyvaluetype/) sabitlerinden biridir.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
