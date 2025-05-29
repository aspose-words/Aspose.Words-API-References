---
title: BorderCollection.Left
linktitle: Left
articleTitle: Left
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية BorderCollection Left، وقم بالوصول بسهولة إلى الحد الأيسر وتخصيصه لتحسين مرونة التصميم والجاذبية البصرية.
type: docs
weight: 70
url: /ar/net/aspose.words/bordercollection/left/
---
## BorderCollection.Left property

يحصل على الحد الأيسر.

```csharp
public Border Left { get; }
```

## أمثلة

يوضح كيفية تطبيق لون الحدود والتظليل أثناء إنشاء جدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// ابدأ جدولًا وقم بتعيين لون/سمك افتراضي لحدوده.
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// قم بإنشاء صف يحتوي على خليتين بألوان خلفية مختلفة.
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// إعادة تعيين تنسيق الخلية لتعطيل ألوان الخلفية
// تعيين سمك حدود مخصص لجميع الخلايا الجديدة التي ينشئها المنشئ،
// ثم قم ببناء صف ثاني.
builder.CellFormat.ClearFormatting();
builder.CellFormat.Borders.Left.LineWidth = 4.0;
builder.CellFormat.Borders.Right.LineWidth = 4.0;
builder.CellFormat.Borders.Top.LineWidth = 4.0;
builder.CellFormat.Borders.Bottom.LineWidth = 4.0;

builder.InsertCell();
builder.Writeln("Row 2, Cell 1.");
builder.InsertCell();
builder.Writeln("Row 2, Cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.TableBordersAndShading.docx");
```

### أنظر أيضا

* class [Border](../../border/)
* class [BorderCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
