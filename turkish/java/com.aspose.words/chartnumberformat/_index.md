---
title: "ChartNumberFormat"
linktitle: "ChartNumberFormat"
second_title: "Aspose.Words Java için"
description: "Java'da üst öğenin sayı biçimlendirmesini temsil eder."
type: docs
weight: 84
url: /tr/java/com.aspose.words/chartnumberformat/
---

**Inheritance:**
java.lang.Object
```
public class ChartNumberFormat
```

Üst öğenin sayı biçimlendirmesini temsil eder.

Daha fazla bilgi için, [ Working with Charts ][Working with Charts] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Grafik değerleri için biçimlendirme nasıl ayarlanır gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series to the chart with categories for the X-axis,
 // and large respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{1900000.0, 850000.0, 2100000.0, 600000.0, 1500000.0});

 // Set the number format of the Y-axis tick labels to not group digits with commas.
 chart.getAxisY().getNumberFormat().setFormatCode("#,##0");

 // This flag can override the above value and draw the number format from the source cell.
 Assert.assertFalse(chart.getAxisY().getNumberFormat().isLinkedToSource());

 doc.save(getArtifactsDir() + "Charts.SetNumberFormatToChartAxis.docx");
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getFormatCode()](#getFormatCode) | Veri etiketine uygulanan format kodunu alır. |
| [isLinkedToSource()](#isLinkedToSource) | Format kodunun bir kaynak hücreye bağlı olup olmadığını belirtir. |
| [isLinkedToSource(boolean value)](#isLinkedToSource-boolean) | Format kodunun bir kaynak hücreye bağlı olup olmadığını belirtir. |
| [setFormatCode(String value)](#setFormatCode-java.lang.String) | Veri etiketine uygulanan format kodunu ayarlar. |
### getFormatCode() {#getFormatCode}
```
public String getFormatCode()
```


Veri etiketine uygulanan format kodunu alır.

 **Remarks:** 

Sayı biçimlendirme, bir değerin veri etiketinde nasıl göründüğünü değiştirmek için kullanılır ve bazı çok yaratıcı şekillerde kullanılabilir. Sayı biçimlendirme örnekleri:

Sayı - "\#,\#\#0.00"

Para birimi - "\\"$\\"\#,\#\#0.00"

Zaman - "[$-x-systime]h:mm:ss AM/PM"

Tarih - "d/mm/yyyy"

Yüzde - "0.00%"

Kesir - "\# ?/?"

Bilimsel - "0.00E+00"

Metin - "@"

Muhasebe - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

Renkli özel - "[Red]-\#,\#\#0.0"

 **Examples:** 

Grafik serisi için veri etiketlerini etkinleştirme ve yapılandırma yöntemlerini gösterir.

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

Grafik değerleri için biçimlendirme nasıl ayarlanır gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series to the chart with categories for the X-axis,
 // and large respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{1900000.0, 850000.0, 2100000.0, 600000.0, 1500000.0});

 // Set the number format of the Y-axis tick labels to not group digits with commas.
 chart.getAxisY().getNumberFormat().setFormatCode("#,##0");

 // This flag can override the above value and draw the number format from the source cell.
 Assert.assertFalse(chart.getAxisY().getNumberFormat().isLinkedToSource());

 doc.save(getArtifactsDir() + "Charts.SetNumberFormatToChartAxis.docx");
 
```

**Returns:**
java.lang.String - Veri etiketine uygulanan format kodu.
### isLinkedToSource() {#isLinkedToSource}
```
public boolean isLinkedToSource()
```


Format kodunun bir kaynak hücreye bağlı olup olmadığını belirtir. Varsayılan değer true'dur.

 **Remarks:** 

Format kodu kaynağa bağlıysa NumberFormat genel olarak sıfırlanacaktır.

 **Examples:** 

Grafik değerleri için biçimlendirme nasıl ayarlanır gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series to the chart with categories for the X-axis,
 // and large respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{1900000.0, 850000.0, 2100000.0, 600000.0, 1500000.0});

 // Set the number format of the Y-axis tick labels to not group digits with commas.
 chart.getAxisY().getNumberFormat().setFormatCode("#,##0");

 // This flag can override the above value and draw the number format from the source cell.
 Assert.assertFalse(chart.getAxisY().getNumberFormat().isLinkedToSource());

 doc.save(getArtifactsDir() + "Charts.SetNumberFormatToChartAxis.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### isLinkedToSource(boolean value) {#isLinkedToSource-boolean}
```
public void isLinkedToSource(boolean value)
```


Format kodunun bir kaynak hücreye bağlı olup olmadığını belirtir. Varsayılan değer true'dur.

 **Remarks:** 

Format kodu kaynağa bağlıysa NumberFormat genel olarak sıfırlanacaktır.

 **Examples:** 

Grafik değerleri için biçimlendirme nasıl ayarlanır gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series to the chart with categories for the X-axis,
 // and large respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{1900000.0, 850000.0, 2100000.0, 600000.0, 1500000.0});

 // Set the number format of the Y-axis tick labels to not group digits with commas.
 chart.getAxisY().getNumberFormat().setFormatCode("#,##0");

 // This flag can override the above value and draw the number format from the source cell.
 Assert.assertFalse(chart.getAxisY().getNumberFormat().isLinkedToSource());

 doc.save(getArtifactsDir() + "Charts.SetNumberFormatToChartAxis.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setFormatCode(String value) {#setFormatCode-java.lang.String}
```
public void setFormatCode(String value)
```


Veri etiketine uygulanan format kodunu ayarlar.

 **Remarks:** 

Sayı biçimlendirme, bir değerin veri etiketinde nasıl göründüğünü değiştirmek için kullanılır ve bazı çok yaratıcı şekillerde kullanılabilir. Sayı biçimlendirme örnekleri:

Sayı - "\#,\#\#0.00"

Para birimi - "\\"$\\"\#,\#\#0.00"

Zaman - "[$-x-systime]h:mm:ss AM/PM"

Tarih - "d/mm/yyyy"

Yüzde - "0.00%"

Kesir - "\# ?/?"

Bilimsel - "0.00E+00"

Metin - "@"

Muhasebe - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

Renkli özel - "[Red]-\#,\#\#0.0"

 **Examples:** 

Grafik serisi için veri etiketlerini etkinleştirme ve yapılandırma yöntemlerini gösterir.

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

Grafik değerleri için biçimlendirme nasıl ayarlanır gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series to the chart with categories for the X-axis,
 // and large respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{1900000.0, 850000.0, 2100000.0, 600000.0, 1500000.0});

 // Set the number format of the Y-axis tick labels to not group digits with commas.
 chart.getAxisY().getNumberFormat().setFormatCode("#,##0");

 // This flag can override the above value and draw the number format from the source cell.
 Assert.assertFalse(chart.getAxisY().getNumberFormat().isLinkedToSource());

 doc.save(getArtifactsDir() + "Charts.SetNumberFormatToChartAxis.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Veri etiketine uygulanan format kodu. |

