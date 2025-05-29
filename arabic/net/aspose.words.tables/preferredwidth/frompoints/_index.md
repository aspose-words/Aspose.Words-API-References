---
title: PreferredWidth.FromPoints
linktitle: FromPoints
articleTitle: FromPoints
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة PreferredWidth FromPoints لإنشاء مثيل جديد بعرض محدد بالنقاط، مما يعزز دقة التصميم وكفاءته.
type: docs
weight: 30
url: /ar/net/aspose.words.tables/preferredwidth/frompoints/
---
## PreferredWidth.FromPoints method

طريقة إنشاء تقوم بإرجاع مثيل جديد يمثل عرضًا مفضلًا يتم تحديده باستخدام عدد من النقاط.

```csharp
public static PreferredWidth FromPoints(double points)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| points | Double | يجب أن تكون القيمة من 0 إلى 22 بوصة (22 * 72 نقطة). |

## أمثلة

يوضح كيفية استخدام أدوات تحويل الوحدات أثناء تحديد العرض المفضل للخلية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(ConvertUtil.InchToPoint(3));
builder.InsertCell();

Assert.AreEqual(216.0d, table.FirstRow.FirstCell.CellFormat.PreferredWidth.Value);
```

يوضح كيفية تعيين العرض المفضل لخلايا الجدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// هناك طريقتان لتطبيق فئة "PreferredWidth" على خلايا الجدول.
// 1 - تعيين العرض المفضل المطلق استنادًا إلى النقاط:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 - تعيين عرض مفضل نسبيًا استنادًا إلى النسبة المئوية لعرض الجدول:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// ستشغل الخلية التي ليس لها عرض مفضل محدد بقية المساحة المتوفرة.
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// يؤدي كل تكوين لخاصية "PreferredWidth" إلى إنشاء كائن جديد.
Assert.AreNotEqual(table.FirstRow.Cells[1].CellFormat.PreferredWidth.GetHashCode(),
    builder.CellFormat.PreferredWidth.GetHashCode());

builder.CellFormat.Shading.BackgroundPatternColor = Color.LightGreen;
builder.Writeln("Automatically sized cell.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

### أنظر أيضا

* class [PreferredWidth](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
