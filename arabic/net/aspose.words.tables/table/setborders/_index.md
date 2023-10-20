---
title: Table.SetBorders
linktitle: SetBorders
articleTitle: SetBorders
second_title: Aspose.Words لـ .NET
description: Table SetBorders طريقة. يضبط كل حدود الجدول على نمط الخط والعرض واللون المحدد في C#.
type: docs
weight: 420
url: /ar/net/aspose.words.tables/table/setborders/
---
## Table.SetBorders method

يضبط كل حدود الجدول على نمط الخط والعرض واللون المحدد.

```csharp
public void SetBorders(LineStyle lineStyle, double lineWidth, Color color)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| lineStyle | LineStyle | نمط الخط المطلوب تطبيقه. |
| lineWidth | Double | عرض الخط المراد ضبطه (بالنقاط). |
| color | Color | اللون الذي سيتم استخدامه للحدود. |

## أمثلة

يوضح كيفية تنسيق كافة حدود الجدول مرة واحدة.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// امسح جميع الحدود الموجودة في الجدول.
table.ClearBorders();

// قم بتعيين خط أخضر واحد ليكون بمثابة الحدود الخارجية والداخلية لهذا الجدول.
table.SetBorders(LineStyle.Single, 1.5, Color.Green);

doc.Save(ArtifactsDir + "Table.SetBorders.docx");
```

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

* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
