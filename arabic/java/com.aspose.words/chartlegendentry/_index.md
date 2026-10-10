---
title: "ChartLegendEntry"
linktitle: "ChartLegendEntry"
second_title: "Aspose.Words لـ Java"
description: "يمثل إدخال أسطورة المخطط في Java."
type: docs
weight: 80
url: /ar/java/com.aspose.words/chartlegendentry/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ChartLegendEntry implements Cloneable
```

يمثل مدخلًا في وسيلة إيضاح المخطط.

للتعرف على المزيد، زر مقالة توثيق [ Working with Charts ][Working with Charts].

 **Remarks:** 

يتطابق إدخال الأسطورة مع سلسلة مخطط أو خط اتجاه محدد.

نص الإدخال هو اسم السلسلة أو خط الاتجاه. لا يمكن تغيير النص.

 **Examples:** 

يعرض كيفية التعامل مع خط التوضيح.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Chart series (Java).docx");
 Chart chart = ((Shape)doc.getChild(NodeType.SHAPE, 0, true)).getChart();

 ChartLegend chartLegend = chart.getLegend();
 // Set default font size all legend entries.
 chartLegend.getFont().setSize(14.0);
 // Change font for specific legend entry.
 chartLegend.getLegendEntries().get(1).getFont().setItalic(true);
 chartLegend.getLegendEntries().get(1).getFont().setSize(12.0);
 // Get legend entry for chart series.
 ChartLegendEntry legendEntry = chart.getSeries().get(0).getLegendEntry();

 doc.save(getArtifactsDir() + "Charts.LegendFont.docx");
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fetchSpecialDefaultRunPropertyValue(int key)](#fetchSpecialDefaultRunPropertyValue-int) |  |
| [generateItemText()](#generateItemText) |  |
| [getFont()](#getFont) | يوفر الوصول إلى تنسيق الخط لهذا الإدخال في الأسطورة. |
| [getRelativePropertyValue(int key, Object value)](#getRelativePropertyValue-int-java.lang.Object) |  |
| [isHidden()](#isHidden) | يحصل على قيمة تشير إلى ما إذا كان هذا الإدخال مخفيًا في أسطورة المخطط. |
| [isHidden(boolean value)](#isHidden-boolean) | يضبط قيمة تشير إلى ما إذا كان هذا الإدخال مخفيًا في أسطورة المخطط. |
### fetchSpecialDefaultRunPropertyValue(int key) {#fetchSpecialDefaultRunPropertyValue-int}
```
public Object fetchSpecialDefaultRunPropertyValue(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### generateItemText() {#generateItemText}
```
public String generateItemText()
```




**Returns:**
java.lang.String
### getFont() {#getFont}
```
public Font getFont()
```


يوفر الوصول إلى تنسيق الخط لهذا الإدخال في الأسطورة.

 **Examples:** 

يعرض كيفية التعامل مع خط التوضيح.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Chart series (Java).docx");
 Chart chart = ((Shape)doc.getChild(NodeType.SHAPE, 0, true)).getChart();

 ChartLegend chartLegend = chart.getLegend();
 // Set default font size all legend entries.
 chartLegend.getFont().setSize(14.0);
 // Change font for specific legend entry.
 chartLegend.getLegendEntries().get(1).getFont().setItalic(true);
 chartLegend.getLegendEntries().get(1).getFont().setSize(12.0);
 // Get legend entry for chart series.
 ChartLegendEntry legendEntry = chart.getSeries().get(0).getLegendEntry();

 doc.save(getArtifactsDir() + "Charts.LegendFont.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getRelativePropertyValue(int key, Object value) {#getRelativePropertyValue-int-java.lang.Object}
```
public Object getRelativePropertyValue(int key, Object value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |
| قيمة | java.lang.Object |  |

**Returns:**
java.lang.Object
### isHidden() {#isHidden}
```
public boolean isHidden()
```


يحصل على قيمة تشير إلى ما إذا كان هذا الإدخال مخفيًا في أسطورة المخطط. القيمة الافتراضية هي **false**.

 **Remarks:** 

عندما يكون إدخال أسطورة المخطط مخفيًا، لا يؤثر ذلك على سلسلة المخطط أو خط الاتجاه المقابل الذي لا يزال معروضًا في المخطط.

 **Examples:** 

يوضح كيفية التعامل مع مدخل وسيلة إيضاح لسلسلة المخطط.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);

 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();
 series.clear();

 String[] categories = new String[] { "AW Category 1", "AW Category 2" };

 ChartSeries series1 = series.add("Series 1", categories, new double[] { 1.0, 2.0 });
 series.add("Series 2", categories, new double[] { 3.0, 4.0 });
 series.add("Series 3", categories, new double[] { 5.0, 6.0 });
 series.add("Series 4", categories, new double[] { 0.0, 0.0 });

 ChartLegendEntryCollection legendEntries = chart.getLegend().getLegendEntries();
 legendEntries.get(3).isHidden(true);

 doc.save(getArtifactsDir() + "Charts.LegendEntries.docx");
 
```

**Returns:**
boolean - قيمة تشير إلى ما إذا كان هذا الإدخال مخفيًا في أسطورة المخطط.
### isHidden(boolean value) {#isHidden-boolean}
```
public void isHidden(boolean value)
```


يضبط قيمة تشير إلى ما إذا كان هذا الإدخال مخفيًا في أسطورة المخطط. القيمة الافتراضية هي **false**.

 **Remarks:** 

عندما يكون إدخال أسطورة المخطط مخفيًا، لا يؤثر ذلك على سلسلة المخطط أو خط الاتجاه المقابل الذي لا يزال معروضًا في المخطط.

 **Examples:** 

يوضح كيفية التعامل مع مدخل وسيلة إيضاح لسلسلة المخطط.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);

 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();
 series.clear();

 String[] categories = new String[] { "AW Category 1", "AW Category 2" };

 ChartSeries series1 = series.add("Series 1", categories, new double[] { 1.0, 2.0 });
 series.add("Series 2", categories, new double[] { 3.0, 4.0 });
 series.add("Series 3", categories, new double[] { 5.0, 6.0 });
 series.add("Series 4", categories, new double[] { 0.0, 0.0 });

 ChartLegendEntryCollection legendEntries = chart.getLegend().getLegendEntries();
 legendEntries.get(3).isHidden(true);

 doc.save(getArtifactsDir() + "Charts.LegendEntries.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة تشير إلى ما إذا كان هذا الإدخال مخفيًا في أسطورة المخطط. |

