---
title: RowFormat.HeightRule
linktitle: HeightRule
articleTitle: HeightRule
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية RowFormat HeightRule لتخصيص ارتفاعات صفوف الجدول بسهولة للحصول على تخطيط وتصميم مثالي في تطبيقاتك.
type: docs
weight: 50
url: /ar/net/aspose.words.tables/rowformat/heightrule/
---
## RowFormat.HeightRule property

يحصل على القاعدة لتحديد ارتفاع صف الجدول أو يعينها.

```csharp
public HeightRule HeightRule { get; set; }
```

## أمثلة

يوضح كيفية تنسيق الصفوف باستخدام منشئ المستندات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// ابدأ صفًا ثانيًا، ثم اضبط ارتفاعه. سيُطبّق المُنشئ هذه الإعدادات على
// الصف الحالي، بالإضافة إلى أي صفوف جديدة يتم إنشاؤها بعد ذلك.
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// لم يتأثر الصف الأول بإعادة تكوين الحشو ولا يزال يحتفظ بالقيم الافتراضية.
Assert.AreEqual(0.0d, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);

Assert.AreEqual(100.0d, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

يوضح كيفية إنشاء جدول منسق باستخدام DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
table.LeftIndent = 20;

// تعيين بعض خيارات التنسيق لمظهر النص والجدول.
builder.RowFormat.Height = 40;
builder.RowFormat.HeightRule = HeightRule.AtLeast;
builder.CellFormat.Shading.BackgroundPatternColor = Color.FromArgb(198, 217, 241);

builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Font.Size = 16;
builder.Font.Name = "Arial";
builder.Font.Bold = true;

// سيؤدي تكوين خيارات التنسيق في منشئ المستندات إلى تطبيقها
// إلى الخلية/الصف الحالي الذي يوجد فيه المؤشر،
// بالإضافة إلى أي خلايا أو صفوف جديدة تم إنشاؤها باستخدام هذا المنشئ.
builder.Write("Header Row,\n Cell 1");
builder.InsertCell();
builder.Write("Header Row,\n Cell 2");
builder.InsertCell();
builder.Write("Header Row,\n Cell 3");
builder.EndRow();

// إعادة تكوين كائنات تنسيق المنشئ للصفوف والخلايا الجديدة التي سنقوم بإنشائها.
// لن يقوم المنشئ بتطبيق هذه العناصر على الصف الأول الذي تم إنشاؤه بالفعل حتى يظهر كصف رأس.
builder.CellFormat.Shading.BackgroundPatternColor = Color.White;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.RowFormat.Height = 30;
builder.RowFormat.HeightRule = HeightRule.Auto;
builder.InsertCell();
builder.Font.Size = 12;
builder.Font.Bold = false;

builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");
builder.InsertCell();
builder.Write("Row 1, Cell 3.");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.InsertCell();
builder.Write("Row 2, Cell 3.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateFormattedTable.docx");
```

### أنظر أيضا

* enum [HeightRule](../../../aspose.words/heightrule/)
* class [RowFormat](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
