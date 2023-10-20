---
title: Table.LeftIndent
linktitle: LeftIndent
articleTitle: LeftIndent
second_title: Aspose.Words لـ .NET
description: Table LeftIndent ملكية. الحصول على أو تعيين القيمة التي تمثل المسافة البادئة اليسرى للجدول في C#.
type: docs
weight: 190
url: /ar/net/aspose.words.tables/table/leftindent/
---
## Table.LeftIndent property

الحصول على أو تعيين القيمة التي تمثل المسافة البادئة اليسرى للجدول.

```csharp
public double LeftIndent { get; set; }
```

## أمثلة

يوضح كيفية إنشاء جدول منسق باستخدام DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
table.LeftIndent = 20;

// قم بتعيين بعض خيارات التنسيق لمظهر النص والجدول.
builder.RowFormat.Height = 40;
builder.RowFormat.HeightRule = HeightRule.AtLeast;
builder.CellFormat.Shading.BackgroundPatternColor = Color.FromArgb(198, 217, 241);

builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Font.Size = 16;
builder.Font.Name = "Arial";
builder.Font.Bold = true;

// سيؤدي تكوين خيارات التنسيق في أداة إنشاء المستندات إلى تطبيقها
// إلى الخلية/الصف الحالي الذي يوجد به المؤشر،
// بالإضافة إلى أي خلايا وصفوف جديدة تم إنشاؤها باستخدام هذا المنشئ.
builder.Write("Header Row,\n Cell 1");
builder.InsertCell();
builder.Write("Header Row,\n Cell 2");
builder.InsertCell();
builder.Write("Header Row,\n Cell 3");
builder.EndRow();

// أعد تكوين كائنات التنسيق الخاصة بالمنشئ للصفوف والخلايا الجديدة التي نحن على وشك إنشاؤها.
// لن يقوم المنشئ بتطبيق هذه العناصر على الصف الأول الذي تم إنشاؤه بالفعل بحيث يبرز كصف رأس.
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

* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
