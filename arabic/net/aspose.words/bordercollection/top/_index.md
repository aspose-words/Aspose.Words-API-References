---
title: BorderCollection.Top
linktitle: Top
articleTitle: Top
second_title: Aspose.Words لـ .NET
description: BorderCollection Top ملكية. يحصل على الحد العلوي في C#.
type: docs
weight: 120
url: /ar/net/aspose.words/bordercollection/top/
---
## BorderCollection.Top property

يحصل على الحد العلوي.

```csharp
public Border Top { get; }
```

## أمثلة

يوضح كيفية تطبيق لون الحدود والتظليل أثناء إنشاء الجدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// ابدأ الجدول وقم بتعيين اللون/السمك الافتراضي لحدوده.
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// أنشئ صفًا يحتوي على خليتين بألوان خلفية مختلفة.
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// إعادة تعيين تنسيق الخلية لتعطيل ألوان الخلفية
// قم بتعيين سمك حدود مخصص لجميع الخلايا الجديدة التي أنشأها المنشئ،
// ثم أنشئ صفًا ثانيًا.
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
