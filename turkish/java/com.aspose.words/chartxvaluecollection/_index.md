---
title: "ChartXValueCollection"
linktitle: "ChartXValueCollection"
second_title: "Aspose.Words Java için"
description: "Java'da bir grafik serisi için X değerlerinin bir koleksiyonunu temsil eder."
type: docs
weight: 95
url: /tr/java/com.aspose.words/chartxvaluecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartXValueCollection implements Iterable
```

Bir grafik serisi için X değerlerinin bir koleksiyonunu temsil eder.

 **Remarks:** 

Koleksiyondaki **null** dışındaki tüm öğeler aynı [ChartXValue.getValueType()](../../com.aspose.words/chartxvalue/\#getValueType) değerine sahip olmalıdır.

Koleksiyon yalnızca X değerlerini değiştirmeye izin verir. Bir grafik serisine yeni değerler eklemek veya eklemek, ya da değerleri kaldırmak için, [ChartSeries](../../com.aspose.words/chartseries/) sınıfının uygun yöntemleri kullanılabilir.

 **Examples:** 

Grafik serisi verilerinin nasıl alınacağını gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get(int index)](#get-int) | Belirtilen indeksteki X değerini alır. |
| [getCount()](#getCount) | Bu koleksiyondaki öğe sayısını alır. |
| [getFormatCode()](#getFormatCode) | X değerlerine uygulanan biçim kodunu alır. |
| [iterator()](#iterator) | Bir enumerator nesnesi döndürür. |
| [set(int index, ChartXValue value)](#set-int-com.aspose.words.ChartXValue) | Belirtilen indeksteki X değerini ayarlar. |
| [setFormatCode(String value)](#setFormatCode-java.lang.String) | X değerlerine uygulanan biçim kodunu ayarlar. |
### get(int index) {#get-int}
```
public ChartXValue get(int index)
```


Belirtilen indeksteki X değerini alır.

 **Remarks:** 

Boş değerler **null** olarak temsil edilir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/) - The X value at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Bu koleksiyondaki öğe sayısını alır.

**Returns:**
int - Bu koleksiyondaki öğe sayısı.
### getFormatCode() {#getFormatCode}
```
public String getFormatCode()
```


X değerlerine uygulanan biçim kodunu alır.

 **Remarks:** 

Sayı biçimlendirme, değerlerin grafikte görünüşünü değiştirmek için kullanılır. Sayı formatı örnekleri:

Sayı - "\#,\#\#0.00"

Para birimi - "\\"$\\"\#,\#\#0.00"

Zaman - "[$-x-systime]h:mm:ss AM/PM"

Tarih - "d/mm/yyyy"

Yüzde - "0.00%"

Kesir - "\# ?/?"

Bilimsel - "0.00E+00"

Muhasebe - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

Renkli özel - "[Red]-\#,\#\#0.0"

 **Examples:** 

Grafik verisinin biçim kodu ile nasıl çalışılacağını gösterir.

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
java.lang.String - X değerlerine uygulanan biçim kodu.
### iterator() {#iterator}
```
public Iterator iterator()
```


Bir enumerator nesnesi döndürür.

**Returns:**
java.util.Iterator
### set(int index, ChartXValue value) {#set-int-com.aspose.words.ChartXValue}
```
public void set(int index, ChartXValue value)
```


Belirtilen indeksteki X değerini ayarlar.

 **Remarks:** 

Boş değerler **null** olarak temsil edilir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int |  |
| value | [ChartXValue](../../com.aspose.words/chartxvalue/) | Belirtilen indeksteki X değeri. |

### setFormatCode(String value) {#setFormatCode-java.lang.String}
```
public void setFormatCode(String value)
```


X değerlerine uygulanan biçim kodunu ayarlar.

 **Remarks:** 

Sayı biçimlendirme, değerlerin grafikte görünüşünü değiştirmek için kullanılır. Sayı formatı örnekleri:

Sayı - "\#,\#\#0.00"

Para birimi - "\\"$\\"\#,\#\#0.00"

Zaman - "[$-x-systime]h:mm:ss AM/PM"

Tarih - "d/mm/yyyy"

Yüzde - "0.00%"

Kesir - "\# ?/?"

Bilimsel - "0.00E+00"

Muhasebe - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

Renkli özel - "[Red]-\#,\#\#0.0"

 **Examples:** 

Grafik verisinin biçim kodu ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | X değerlerine uygulanan biçim kodu. |

