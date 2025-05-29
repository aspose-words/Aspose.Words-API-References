---
title: PreferredWidth.Equals
linktitle: Equals
articleTitle: Equals
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تقوم طريقة PreferredWidth Equals بالتحقق مما إذا كان العرض المحدد يتطابق مع القيمة الحالية، مما يضمن الدقة في تصميم التخطيط الخاص بك.
type: docs
weight: 60
url: /ar/net/aspose.words.tables/preferredwidth/equals/
---
## Equals(*[PreferredWidth](../)*) {#equals}

يحدد ما إذا كان المحدد[`PreferredWidth`](../) يساوي القيمة الحالية[`PreferredWidth`](../) .

```csharp
public bool Equals(PreferredWidth other)
```

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

* class [PreferredWidth](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)

---

## Equals(*object*) {#equals_1}

يحدد ما إذا كان الكائن المحدد يساوي في القيمة الكائن الحالي.

```csharp
public override bool Equals(object obj)
```

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

* class [PreferredWidth](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
