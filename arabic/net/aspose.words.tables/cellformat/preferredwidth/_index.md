---
title: CellFormat.PreferredWidth
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: Aspose.Words لـ .NET
description: CellFormat PreferredWidth ملكية. إرجاع أو تعيين العرض المفضل للخلية في C#.
type: docs
weight: 70
url: /ar/net/aspose.words.tables/cellformat/preferredwidth/
---
## CellFormat.PreferredWidth property

إرجاع أو تعيين العرض المفضل للخلية.

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

## ملاحظات

يحدد العرض المفضل (مع خيار الاحتواء التلقائي للجدول) كيفية حساب عرض الفعلي للخلية بواسطة خوارزمية تخطيط الجدول. يمكن تنفيذ تخطيط الجدول بواسطة Aspose.Words عندما يحفظ المستند أو بواسطة Microsoft Word عندما يعرض المستند.

يمكن تحديد العرض المفضل بالنقاط أو بالنسبة المئوية. يمكن أيضًا تحديد width المفضل كـ "تلقائي"، مما يعني عدم تحديد العرض المفضل.

القيمة الافتراضية هي[`Auto`](../../preferredwidth/auto/).

## أمثلة

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

* class [PreferredWidth](../../preferredwidth/)
* class [CellFormat](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
