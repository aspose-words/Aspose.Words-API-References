---
title: PreferredWidth Class
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Tables.PreferredWidth، الحل الأمثل لتحديد عرض الجداول والخلايا الأمثل بدقة ومرونة. حسّن تخطيطات مستنداتك اليوم!
type: docs
weight: 7140
url: /ar/net/aspose.words.tables/preferredwidth/
---
## PreferredWidth class

يمثل قيمة ووحدة قياسها التي تُستخدم لتحديد العرض المفضل للجدول أو الخلية.

لمعرفة المزيد، قم بزيارة[العمل مع الجداول](https://docs.aspose.com/words/net/working-with-tables/) مقالة توثيقية.

```csharp
public sealed class PreferredWidth
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Type](../../aspose.words.tables/preferredwidth/type/) { get; } | يحصل على وحدة القياس المستخدمة لقيمة العرض المفضلة هذه. |
| [Value](../../aspose.words.tables/preferredwidth/value/) { get; } | يحصل على قيمة العرض المُفضّلة. وحدة القياس مُحدّدة في[`Type`](./type/) الملكية. |

## طُرق

| اسم | وصف |
| --- | --- |
| static [FromPercent](../../aspose.words.tables/preferredwidth/frompercent/)(*double*) | طريقة إنشاء تقوم بإرجاع مثيل جديد يمثل عرضًا مفضلًا محددًا كنسبة مئوية. |
| static [FromPoints](../../aspose.words.tables/preferredwidth/frompoints/)(*double*) | طريقة إنشاء تقوم بإرجاع مثيل جديد يمثل عرضًا مفضلًا يتم تحديده باستخدام عدد من النقاط. |
| override [Equals](../../aspose.words.tables/preferredwidth/equals/#equals_1)(*object*) | يحدد ما إذا كان الكائن المحدد يساوي في القيمة الكائن الحالي. |
| [Equals](../../aspose.words.tables/preferredwidth/equals/#equals)(*PreferredWidth*) | يحدد ما إذا كان المحدد`PreferredWidth` يساوي القيمة الحالية`PreferredWidth` . |
| override [GetHashCode](../../aspose.words.tables/preferredwidth/gethashcode/)() | يعمل كدالة تجزئة لهذا النوع. |
| override [ToString](../../aspose.words.tables/preferredwidth/tostring/)() | يعيد سلسلة سهلة الاستخدام تعرض قيمة هذا الكائن. |

## مجالات

| اسم | وصف |
| --- | --- |
| static readonly [Auto](../../aspose.words.tables/preferredwidth/auto/) | يعيد مثيلًا يمثل قيمة "العرض المفضل غير محدد". |

## ملاحظات

يمكن تحديد العرض المفضل كنسبة مئوية أو عدد من النقاط أو قيمة خاصة "لا شيء/تلقائي".

إن حالات هذه الفئة غير قابلة للتغيير.

## أمثلة

يوضح كيفية ضبط الجدول ليتناسب تلقائيًا مع 50% من عرض الصفحة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell #1");
builder.InsertCell();
builder.Write("Cell #2");
builder.InsertCell();
builder.Write("Cell #3");

table.PreferredWidth = PreferredWidth.FromPercent(50);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
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

* مساحة الاسم [Aspose.Words.Tables](../../aspose.words.tables/)
* المجسم [Aspose.Words](../../)
