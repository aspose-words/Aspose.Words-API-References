---
title: Fill.Solid
linktitle: Solid
articleTitle: Solid
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة Fill Solid لتحقيق تعبئة لونية متسقة، مما يعزز الجاذبية البصرية والتصميم الموحد بسهولة.
type: docs
weight: 260
url: /ar/net/aspose.words.drawing/fill/solid/
---
## Solid() {#solid}

يضبط التعبئة على لون موحد.

```csharp
public void Solid()
```

## ملاحظات

استخدم هذه الطريقة لتحويل أي من التعبئة إلى تعبئة صلبة مرة أخرى.

## أمثلة

يوضح كيفية تحويل أي من التعبئة إلى تعبئة صلبة مرة أخرى.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// الحصول على كائن التعبئة لخط التشغيل الأول.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

//تحقق من خصائص التعبئة للخط.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// تغيير نوع التعبئة إلى صلب بلون أخضر موحد.
fill.Solid();
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### أنظر أيضا

* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)

---

## Solid(*Color*) {#solid_1}

يضبط التعبئة إلى لون موحد محدد.

```csharp
public void Solid(Color color)
```

## ملاحظات

استخدم هذه الطريقة لتحويل أي من التعبئة إلى تعبئة صلبة مرة أخرى.

## أمثلة

يوضح كيفية استخدام تنسيق الرسم البياني.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

//حذف السلسلة التي تم إنشاؤها افتراضيًا.
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2" };
series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });

//تنسيق خلفية الرسم البياني.
chart.Format.Fill.Solid(Color.DarkSlateGray);

//إخفاء علامات المحور.
chart.AxisX.TickLabels.Position = AxisTickLabelPosition.None;
chart.AxisY.TickLabels.Position = AxisTickLabelPosition.None;

//تنسيق عنوان الرسم البياني.
chart.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

//تنسيق عنوان المحور.
chart.AxisX.Title.Show = true;
chart.AxisX.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

//تنسيق الأسطورة.
chart.Legend.Format.Fill.Solid(Color.LightGoldenrodYellow);

doc.Save(ArtifactsDir + "Charts.ChartFormat.docx");
```

### أنظر أيضا

* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
