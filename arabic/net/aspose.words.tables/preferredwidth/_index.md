---
title: Class PreferredWidth
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Tables.PreferredWidth فصل. يمثل القيمة ووحدة القياس الخاصة بها المستخدمة لتحديد العرض المفضل للجدول أو الخلية.
type: docs
weight: 6290
url: /ar/net/aspose.words.tables/preferredwidth/
---
## PreferredWidth class

يمثل القيمة ووحدة القياس الخاصة بها المستخدمة لتحديد العرض المفضل للجدول أو الخلية.

لمعرفة المزيد، قم بزيارة[العمل مع الجداول](https://docs.aspose.com/words/net/working-with-tables/) مقالة توثيقية.

```csharp
public sealed class PreferredWidth
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Type](../../aspose.words.tables/preferredwidth/type/) { get; } | للحصول على وحدة القياس المستخدمة لقيمة العرض المفضلة هذه. |
| [Value](../../aspose.words.tables/preferredwidth/value/) { get; } | يحصل على قيمة العرض المفضلة. وحدة القياس محددة في[`Type`](./type/) الملكية. |

## طُرق

| اسم | وصف |
| --- | --- |
| static [FromPercent](../../aspose.words.tables/preferredwidth/frompercent/)(double) | طريقة إنشاء تقوم بإرجاع مثيل جديد يمثل العرض المفضل المحدد كنسبة مئوية. |
| static [FromPoints](../../aspose.words.tables/preferredwidth/frompoints/)(double) | طريقة إنشاء تقوم بإرجاع مثيل جديد يمثل العرض المفضل المحدد باستخدام عدد من النقاط. |
| override [Equals](../../aspose.words.tables/preferredwidth/equals/#equals_1)(object) | تحديد ما إذا كان الكائن المحدد يساوي قيمة الكائن الحالي. |
| [Equals](../../aspose.words.tables/preferredwidth/equals/#equals)(PreferredWidth) | تحديد ما إذا كان المحدد`PreferredWidth` يساوي القيمة الحالية`PreferredWidth` . |
| override [GetHashCode](../../aspose.words.tables/preferredwidth/gethashcode/)() | بمثابة دالة تجزئة لهذا النوع. |
| override [ToString](../../aspose.words.tables/preferredwidth/tostring/)() | تُرجع سلسلة سهلة الاستخدام تعرض قيمة هذا الكائن. |

## مجالات

| اسم | وصف |
| --- | --- |
| static readonly [Auto](../../aspose.words.tables/preferredwidth/auto/) | إرجاع مثيل يمثل القيمة "لم يتم تحديد العرض المفضل". |

### ملاحظات

يمكن تحديد العرض المفضل كنسبة مئوية أو عدد النقاط أو قيمة خاصة "لا شيء/تلقائي".

مثيلات هذه الفئة غير قابلة للتغيير.

### أمثلة

يوضح كيفية تعيين جدول ليتناسب تلقائيًا مع 50% من عرض الصفحة.

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

* مساحة الاسم [Aspose.Words.Tables](../../aspose.words.tables/)
* المجسم [Aspose.Words](../../)


