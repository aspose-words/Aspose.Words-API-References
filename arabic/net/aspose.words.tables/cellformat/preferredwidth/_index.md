---
title: CellFormat.PreferredWidth
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية CellFormat PreferredWidth لتخصيص عرض الخلايا بسهولة لتحقيق أفضل تخطيط وتصميم لجداول بياناتك. حسّن عرض بياناتك!
type: docs
weight: 80
url: /ar/net/aspose.words.tables/cellformat/preferredwidth/
---
## CellFormat.PreferredWidth property

يعيد أو يعين العرض المفضل للخلية.

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

## ملاحظات

يُحدد العرض المُفضّل (مع خيار "التوافق التلقائي" في الجدول) كيفية حساب العرض الفعلي للخلية باستخدام خوارزمية تخطيط الجدول. يُمكن تنفيذ تخطيط الجدول باستخدام Aspose.Words عند حفظ المستند، أو باستخدام Microsoft Word عند عرضه.

يمكن تحديد العرض المُفضّل بالنقاط أو بالنسبة المئوية. كما يمكن تحديد قيمة العرض المُفضّل على أنها "تلقائي"، مما يعني عدم تحديد أي عرض مُفضّل.

القيمة الافتراضية هي[`Auto`](../../preferredwidth/auto/).

## أمثلة

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

* class [PreferredWidth](../../preferredwidth/)
* class [CellFormat](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
