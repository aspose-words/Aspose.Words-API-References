---
title: DocumentBuilder.ParagraphFormat
linktitle: ParagraphFormat
articleTitle: ParagraphFormat
second_title: Aspose.Words لـ .NET
description: استكشف خاصية ParagraphFormat في DocumentBuilder للوصول إلى ميزات تنسيق الفقرات الأساسية وتخصيصها لتحسين تصميم المستند.
type: docs
weight: 170
url: /ar/net/aspose.words/documentbuilder/paragraphformat/
---
## DocumentBuilder.ParagraphFormat property

يعيد كائنًا يمثل خصائص تنسيق الفقرة الحالية.

```csharp
public ParagraphFormat ParagraphFormat { get; }
```

## أمثلة

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

* class [ParagraphFormat](../../paragraphformat/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
