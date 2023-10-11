---
title: DocumentBuilder.InsertChart
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder طريقة. إدراج كائن مخطط في المستند وتغيير حجمه إلى الحجم المحدد.
type: docs
weight: 280
url: /ar/net/aspose.words/documentbuilder/insertchart/
---
## InsertChart(ChartType, double, double) {#insertchart_1}

إدراج كائن مخطط في المستند وتغيير حجمه إلى الحجم المحدد.

```csharp
public Shape InsertChart(ChartType chartType, double width, double height)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| chartType | ChartType | نوع المخطط المراد إدراجه في المستند. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس 100%. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس 100%. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

### ملاحظات

يمكنك تغيير حجم الصورة والموقع وطريقة تحديد الموضع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) الكائن الذي تم إرجاعه بهذه الطريقة.

### أمثلة

يوضح كيفية إدراج مخطط دائري في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, ConvertUtil.PixelToPoint(300), 
    ConvertUtil.PixelToPoint(300)).Chart;
chart.Series.Clear();
chart.Series.Add("My fruit",
    new[] { "Apples", "Bananas", "Cherries" },
    new[] { 1.3, 2.2, 1.5 });

doc.Save(ArtifactsDir + "DocumentBuilder.InsertPieChart.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## InsertChart(ChartType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertchart}

إدراج كائن مخطط في المستند وتغيير حجمه إلى الحجم المحدد.

```csharp
public Shape InsertChart(ChartType chartType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| chartType | ChartType | نوع المخطط المراد إدراجه في المستند. |
| horzPos | RelativeHorizontalPosition | يحدد المكان الذي يتم منه قياس المسافة إلى الصورة. |
| left | Double | المسافة بالنقاط من الأصل إلى الجانب الأيسر من الصورة. |
| vertPos | RelativeVerticalPosition | يحدد المكان الذي يتم قياس المسافة منه إلى الصورة. |
| top | Double | المسافة بالنقاط من الأصل إلى الجانب العلوي من الصورة. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس 100%. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس 100%. |
| wrapType | WrapType | يحدد كيفية التفاف النص حول الصورة. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

### ملاحظات

يمكنك تغيير حجم الصورة والموقع وطريقة تحديد الموضع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) الكائن الذي تم إرجاعه بهذه الطريقة.

### أمثلة

يوضح كيفية تحديد الموضع والالتفاف أثناء إدراج مخطط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertChart(ChartType.Pie, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
    100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertedChartRelativePosition.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)


