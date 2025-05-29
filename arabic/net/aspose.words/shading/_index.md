---
title: Shading Class
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Shading، المصممة لتعزيز مستنداتك بسمات تظليل قابلة للتخصيص للحصول على مظهر احترافي.
type: docs
weight: 6820
url: /ar/net/aspose.words/shading/
---
## Shading class

يحتوي على سمات التظليل لكائن.

لمعرفة المزيد، قم بزيارة[البرمجة باستخدام المستندات](https://docs.aspose.com/words/net/programming-with-documents/) مقالة توثيقية.

```csharp
public class Shading : InternableComplexAttr
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [BackgroundPatternColor](../../aspose.words/shading/backgroundpatterncolor/) { get; set; } | يحصل على اللون الذي يتم تطبيقه على خلفية`Shading` الكائن. |
| [BackgroundPatternThemeColor](../../aspose.words/shading/backgroundpatternthemecolor/) { get; set; } | يحصل على لون سمة نمط الخلفية أو يعينه في مخطط الألوان المطبق المرتبط بهذا`Shading` الكائن. |
| [BackgroundTintAndShade](../../aspose.words/shading/backgroundtintandshade/) { get; set; } | يحصل على قيمة مزدوجة أو يعينها لتفتيح أو تعتيم لون سمة الخلفية. |
| [ForegroundPatternColor](../../aspose.words/shading/foregroundpatterncolor/) { get; set; } | يحصل على اللون الذي يتم تطبيقه على مقدمة الصورة أو يعينه`Shading` الكائن. |
| [ForegroundPatternThemeColor](../../aspose.words/shading/foregroundpatternthemecolor/) { get; set; } | يحصل على لون سمة نمط المقدمة أو يعينه في مخطط الألوان المطبق المرتبط بهذا`Shading` الكائن. |
| [ForegroundTintAndShade](../../aspose.words/shading/foregroundtintandshade/) { get; set; } | يحصل على قيمة مزدوجة أو يعينها لتفتيح أو تعتيم لون السمة الأمامية. |
| [Texture](../../aspose.words/shading/texture/) { get; set; } | يحصل على نسيج التظليل أو يعينه. |

## طُرق

| اسم | وصف |
| --- | --- |
| [ClearFormatting](../../aspose.words/shading/clearformatting/)() | يزيل التظليل من الكائن. |
| override [Equals](../../aspose.words/shading/equals/#equals_1)(*object*) | يحدد ما إذا كان الكائن المحدد يساوي في القيمة الكائن الحالي. |
| [Equals](../../aspose.words/shading/equals/#equals)(*Shading*) | يحدد ما إذا كان المحدد`Shading` يساوي القيمة الحالية`Shading` . |
| override [GetHashCode](../../aspose.words/shading/gethashcode/)() | يعمل كدالة تجزئة لهذا النوع. |

## أمثلة

يوضح كيفية تزيين النص باستخدام الحدود والتظليل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

BorderCollection borders = builder.ParagraphFormat.Borders;
borders.DistanceFromText = 20;
borders[BorderType.Left].LineStyle = LineStyle.Double;
borders[BorderType.Right].LineStyle = LineStyle.Double;
borders[BorderType.Top].LineStyle = LineStyle.Double;
borders[BorderType.Bottom].LineStyle = LineStyle.Double;

Shading shading = builder.ParagraphFormat.Shading;
shading.Texture = TextureIndex.TextureDiagonalCross;
shading.BackgroundPatternColor = Color.LightCoral;
shading.ForegroundPatternColor = Color.LightSalmon;

builder.Write("This paragraph is formatted with a double border and shading.");
doc.Save(ArtifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
```

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

* class [InternableComplexAttr](../internablecomplexattr/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
