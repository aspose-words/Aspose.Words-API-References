---
title: ChartDataLabelPosition Enum
linktitle: ChartDataLabelPosition
articleTitle: ChartDataLabelPosition
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.ChartDataLabelPosition enum لتخصيص تسميات بيانات الرسم البياني بسهولة لتحسين الوضوح والعرض.
type: docs
weight: 960
url: /ar/net/aspose.words.drawing.charts/chartdatalabelposition/
---
## ChartDataLabelPosition enumeration

يحدد موضع تسمية بيانات الرسم البياني.

```csharp
public enum ChartDataLabelPosition
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Center | `0` | يحدد أنه يجب عرض تسمية البيانات في وسط علامة البيانات. |
| Left | `1` | يحدد أنه يجب عرض تسمية البيانات على يسار علامة البيانات. |
| Right | `2` | يحدد أنه يجب عرض تسمية البيانات على يمين علامة البيانات. |
| Above | `3` | يحدد أنه يجب عرض تسمية البيانات أعلى علامة البيانات. |
| Below | `4` | يحدد أنه يجب عرض تسمية البيانات أسفل علامة البيانات. |
| InsideBase | `5` | يحدد أنه يجب عرض تسمية البيانات داخل قاعدة علامة البيانات. |
| InsideEnd | `6` | يحدد أنه يجب عرض تسمية البيانات داخل نهاية علامة البيانات. |
| OutsideEnd | `7` | يحدد أنه يجب عرض تسمية البيانات خارج نهاية علامة البيانات. |
| BestFit | `8` | يحدد أنه يجب عرض تسمية البيانات في الموضع الأكثر ملاءمة. |

## ملاحظات

لا تسمح جميع أنواع السلاسل بتحديد مواضع العلامات. وتلك التي تسمح بذلك، لا تدعم جميع القيم.

## أمثلة

يوضح كيفية تعيين موضع تسمية البيانات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إدراج مخطط عمودي.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

//حذف السلسلة المولدة افتراضيًا.
seriesColl.Clear();

//إضافة سلسلة.
ChartSeries series = seriesColl.Add(
    "Series 1",
    new string[] { "Category 1", "Category 2", "Category 3" },
    new double[] { 4, 5, 6 });

// إظهار تسميات البيانات وتعيين لون الخط.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.Font.Color = Color.White;

// تعيين موضع تسمية البيانات.
dataLabels.Position = ChartDataLabelPosition.InsideBase;
dataLabels[0].Position = ChartDataLabelPosition.OutsideEnd;
dataLabels[0].Font.Color = Color.DarkRed;

doc.Save(ArtifactsDir + "Charts.LabelPosition.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
