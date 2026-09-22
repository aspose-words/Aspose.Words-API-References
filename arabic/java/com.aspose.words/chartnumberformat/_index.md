---
title: "ChartNumberFormat"
linktitle: "ChartNumberFormat"
second_title: "Aspose.Words لـ Java"
description: "يمثل تنسيق الأرقام للعنصر الأب في Java."
type: docs
weight: 84
url: /ar/java/com.aspose.words/chartnumberformat/
---

**Inheritance:**
java.lang.Object
```
public class ChartNumberFormat
```

يمثل تنسيق الأرقام للعنصر الأب.

للتعرف على المزيد، زر مقالة توثيق [ Working with Charts ][Working with Charts].

 **Examples:** 

يوضح كيفية تعيين التنسيق لقيم المخطط.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getFormatCode()](#getFormatCode) | يحصل على رمز التنسيق المطبق على تسمية البيانات. |
| [isLinkedToSource()](#isLinkedToSource) | يحدد ما إذا كان رمز التنسيق مرتبطًا بخلية المصدر. |
| [isLinkedToSource(boolean value)](#isLinkedToSource-boolean) | يحدد ما إذا كان رمز التنسيق مرتبطًا بخلية المصدر. |
| [setFormatCode(String value)](#setFormatCode-java.lang.String) | يضبط رمز التنسيق المطبق على تسمية البيانات. |
### getFormatCode() {#getFormatCode}
```
public String getFormatCode()
```


يحصل على رمز التنسيق المطبق على تسمية البيانات.

 **Remarks:** 

يُستخدم تنسيق الأرقام لتغيير طريقة ظهور القيمة في تسمية البيانات ويمكن استخدامه بطرق إبداعية جدًا. أمثلة تنسيقات الأرقام:

Number - "\#,\#\#0.00"

Currency - "\\"$\\"\#,\#\#0.00"

Time - "[$-x-systime]h:mm:ss AM/PM"

Date - "d/mm/yyyy"

Percentage - "0.00%"

كسر - "\# ?/?"

علمي - "0.00E+00"

نص - "@"

محاسبة - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

مخصص مع اللون - "[Red]-\#,\#\#0.0"

 **Examples:** 

يعرض كيفية تمكين وتكوين علامات البيانات لسلسلة مخطط.

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

يوضح كيفية تعيين التنسيق لقيم المخطط.

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
java.lang.String - رمز التنسيق المطبق على تسمية البيانات.
### isLinkedToSource() {#isLinkedToSource}
```
public boolean isLinkedToSource()
```


يحدد ما إذا كان رمز التنسيق مرتبطًا بخلية المصدر. القيمة الافتراضية هي true.

 **Remarks:** 

سيتم إعادة ضبط NumberFormat إلى عام إذا كان رمز التنسيق مرتبطًا بالمصدر.

 **Examples:** 

يوضح كيفية تعيين التنسيق لقيم المخطط.

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
boolean - القيمة المنطقية المقابلة.
### isLinkedToSource(boolean value) {#isLinkedToSource-boolean}
```
public void isLinkedToSource(boolean value)
```


يحدد ما إذا كان رمز التنسيق مرتبطًا بخلية المصدر. القيمة الافتراضية هي true.

 **Remarks:** 

سيتم إعادة ضبط NumberFormat إلى عام إذا كان رمز التنسيق مرتبطًا بالمصدر.

 **Examples:** 

يوضح كيفية تعيين التنسيق لقيم المخطط.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setFormatCode(String value) {#setFormatCode-java.lang.String}
```
public void setFormatCode(String value)
```


يضبط رمز التنسيق المطبق على تسمية البيانات.

 **Remarks:** 

يُستخدم تنسيق الأرقام لتغيير طريقة ظهور القيمة في تسمية البيانات ويمكن استخدامه بطرق إبداعية جدًا. أمثلة تنسيقات الأرقام:

Number - "\#,\#\#0.00"

Currency - "\\"$\\"\#,\#\#0.00"

Time - "[$-x-systime]h:mm:ss AM/PM"

Date - "d/mm/yyyy"

Percentage - "0.00%"

كسر - "\# ?/?"

علمي - "0.00E+00"

نص - "@"

محاسبة - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

مخصص مع اللون - "[Red]-\#,\#\#0.0"

 **Examples:** 

يعرض كيفية تمكين وتكوين علامات البيانات لسلسلة مخطط.

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

يوضح كيفية تعيين التنسيق لقيم المخطط.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | رمز التنسيق المطبق على تسمية البيانات. |

