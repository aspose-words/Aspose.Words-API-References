---
title: "BubbleSizeCollection"
linktitle: "BubbleSizeCollection"
second_title: "Aspose.Words Java için"
description: "Java'da bir grafik serisi için balon boyutlarının bir koleksiyonunu temsil eder."
type: docs
weight: 50
url: /tr/java/com.aspose.words/bubblesizecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class BubbleSizeCollection implements Iterable
```

Bir grafik serisi için balon boyutlarının bir koleksiyonunu temsil eder.

 **Remarks:** 

Koleksiyon yalnızca balon boyutlarını değiştirmeye izin verir. Bir grafik serisine yeni değerler eklemek veya değerleri kaldırmak için, [ChartSeries](../../com.aspose.words/chartseries/) sınıfının uygun yöntemleri kullanılabilir.

Boş balon boyutu değerleri double\\#NA\\_N.NA\\_N olarak temsil edilir.
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get(int index)](#get-int) | Belirtilen indeksteki balon boyutu değerini alır. |
| [getCount()](#getCount) | Bu koleksiyondaki öğe sayısını alır. |
| [getFormatCode()](#getFormatCode) | Balon boyutlarına uygulanan biçim kodunu alır. |
| [iterator()](#iterator) | Bir enumerator nesnesi döndürür. |
| [set(int index, double value)](#set-int-double) | Belirtilen indeksteki balon boyutu değerini ayarlar. |
| [setFormatCode(String value)](#setFormatCode-java.lang.String) | Balon boyutlarına uygulanan biçim kodunu ayarlar. |
### get(int index) {#get-int}
```
public double get(int index)
```


Belirtilen indeksteki balon boyutu değerini alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int |  |

**Returns:**
double - Belirtilen indeksteki balon boyutu değeri.
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


Balon boyutlarına uygulanan biçim kodunu alır.

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
java.lang.String - Balon boyutlarına uygulanan biçim kodu.
### iterator() {#iterator}
```
public Iterator iterator()
```


Bir enumerator nesnesi döndürür.

**Returns:**
java.util.Iterator
### set(int index, double value) {#set-int-double}
```
public void set(int index, double value)
```


Belirtilen indeksteki balon boyutu değerini ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int |  |
| değer | double | Belirtilen indeksteki balon boyutu değeri. |

### setFormatCode(String value) {#setFormatCode-java.lang.String}
```
public void setFormatCode(String value)
```


Balon boyutlarına uygulanan biçim kodunu ayarlar.

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
| değer | java.lang.String | Balon boyutlarına uygulanan biçim kodu. |

