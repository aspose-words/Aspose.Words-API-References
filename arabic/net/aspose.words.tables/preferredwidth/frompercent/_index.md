---
title: PreferredWidth.FromPercent
linktitle: FromPercent
articleTitle: FromPercent
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة PreferredWidth FromPercent، التي تُنشئ مثيلًا جديدًا لتحديد العروض المفضلة كنسبة مئوية. حسّن دقة تصميمك!
type: docs
weight: 20
url: /ar/net/aspose.words.tables/preferredwidth/frompercent/
---
## PreferredWidth.FromPercent method

طريقة إنشاء تقوم بإرجاع مثيل جديد يمثل عرضًا مفضلًا محددًا كنسبة مئوية.

```csharp
public static PreferredWidth FromPercent(double percent)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| percent | Double | القيمة يجب أن تكون من 0 إلى 100. |

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

* class [PreferredWidth](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
