---
title: Shading Class
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Shading فصل. يحتوي على سمات تظليل لكائن ما في C#.
type: docs
weight: 5990
url: /ar/net/aspose.words/shading/
---
## Shading class

يحتوي على سمات تظليل لكائن ما.

لمعرفة المزيد، قم بزيارة[البرمجة بالوثائق](https://docs.aspose.com/words/net/programming-with-documents/) مقالة توثيقية.

```csharp
public class Shading : InternableComplexAttr
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [BackgroundPatternColor](../../aspose.words/shading/backgroundpatterncolor/) { get; set; } | الحصول على أو تعيين اللون المطبق على خلفية الصورة`Shading` الكائن. |
| [BackgroundPatternThemeColor](../../aspose.words/shading/backgroundpatternthemecolor/) { get; set; } | الحصول على أو تعيين لون سمة نمط الخلفية في نظام الألوان المطبق المرتبط بهذا`Shading` الكائن. |
| [BackgroundTintAndShade](../../aspose.words/shading/backgroundtintandshade/) { get; set; } | الحصول على أو تعيين قيمة مزدوجة تعمل على تفتيح أو تغميق لون سمة الخلفية. |
| [ForegroundPatternColor](../../aspose.words/shading/foregroundpatterncolor/) { get; set; } | الحصول على أو تعيين اللون المطبق على مقدمة الصورة`Shading` الكائن. |
| [ForegroundPatternThemeColor](../../aspose.words/shading/foregroundpatternthemecolor/) { get; set; } | الحصول على أو تعيين لون سمة النمط الأمامي في نظام الألوان المطبق المرتبط بهذا`Shading` الكائن. |
| [ForegroundTintAndShade](../../aspose.words/shading/foregroundtintandshade/) { get; set; } | الحصول على أو تعيين قيمة مزدوجة تعمل على تفتيح أو تغميق لون المظهر الأمامي. |
| [Texture](../../aspose.words/shading/texture/) { get; set; } | الحصول على نسيج التظليل أو تعيينه. |

## طُرق

| اسم | وصف |
| --- | --- |
| [ClearFormatting](../../aspose.words/shading/clearformatting/)() | إزالة التظليل من الكائن. |
| override [Equals](../../aspose.words/shading/equals/#equals_1)(*object*) | تحديد ما إذا كان الكائن المحدد يساوي قيمة الكائن الحالي. |
| [Equals](../../aspose.words/shading/equals/#equals)(*Shading*) | تحديد ما إذا كان المحدد`Shading` يساوي القيمة الحالية`Shading` . |
| override [GetHashCode](../../aspose.words/shading/gethashcode/)() | بمثابة وظيفة تجزئة لهذا النوع. |

## أمثلة

يوضح كيفية تزيين النص بالحدود والتظليل.

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

* class [InternableComplexAttr](../internablecomplexattr/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
