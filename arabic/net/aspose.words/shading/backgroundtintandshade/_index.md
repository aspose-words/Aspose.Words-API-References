---
title: Shading.BackgroundTintAndShade
linktitle: BackgroundTintAndShade
articleTitle: BackgroundTintAndShade
second_title: Aspose.Words لـ .NET
description: Shading BackgroundTintAndShade ملكية. الحصول على أو تعيين قيمة مزدوجة تعمل على تفتيح أو تغميق لون سمة الخلفية في C#.
type: docs
weight: 30
url: /ar/net/aspose.words/shading/backgroundtintandshade/
---
## Shading.BackgroundTintAndShade property

الحصول على أو تعيين قيمة مزدوجة تعمل على تفتيح أو تغميق لون سمة الخلفية.

```csharp
public double BackgroundTintAndShade { get; set; }
```

## ملاحظات

تتراوح القيم المسموح بها من -1 (الأغمق) إلى 1 (الأفتح) لهذه الخاصية. الصفر (0) محايد. محاولة تعيين هذه الخاصية إلى قيمة أقل من -1 أو أكثر من 1 تؤدي إلىArgumentOutOfRangeException.

يؤدي تعيين هذه الخاصية لكائن التظليل بألوان غير متعلقة بالموضوع إلى ظهورInvalidOperationException.

## أمثلة

يوضح كيفية تعيين الألوان الأمامية والخلفية لتظليل الملمس.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shading shading = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Shading;
shading.Texture = TextureIndex.Texture12Pt5Percent;
shading.ForegroundPatternThemeColor = ThemeColor.Dark1;
shading.BackgroundPatternThemeColor = ThemeColor.Dark2;

shading.ForegroundTintAndShade = 0.5;
shading.BackgroundTintAndShade = -0.2;

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Writeln("Foreground and background pattern colors for shading texture.");

doc.Save(ArtifactsDir + "Font.ForegroundAndBackground.docx");
```

### أنظر أيضا

* class [Shading](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
