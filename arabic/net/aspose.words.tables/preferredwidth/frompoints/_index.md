---
title: PreferredWidth.FromPoints
linktitle: FromPoints
articleTitle: FromPoints
second_title: Aspose.Words لـ .NET
description: PreferredWidth FromPoints طريقة. طريقة إنشاء تقوم بإرجاع مثيل جديد يمثل العرض المفضل المحدد باستخدام عدد من النقاط في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.tables/preferredwidth/frompoints/
---
## PreferredWidth.FromPoints method

طريقة إنشاء تقوم بإرجاع مثيل جديد يمثل العرض المفضل المحدد باستخدام عدد من النقاط.

```csharp
public static PreferredWidth FromPoints(double points)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| points | Double | يجب أن تكون القيمة من 0 إلى 22 بوصة (22*72 نقطة). |

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
// 1 - قم بتعيين العرض المفضل المطلق بناءً على النقاط:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 - قم بتعيين العرض المفضل النسبي بناءً على النسبة المئوية لعرض الجدول:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// الخلية التي لم يتم تحديد العرض المفضل لها سوف تشغل بقية المساحة المتوفرة.
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// يقوم كل تكوين لخاصية "PreferredWidth" بإنشاء كائن جديد.
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
