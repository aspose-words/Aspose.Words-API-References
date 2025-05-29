---
title: Shading.ForegroundTintAndShade
linktitle: ForegroundTintAndShade
articleTitle: ForegroundTintAndShade
second_title: Aspose.Words لـ .NET
description: قم بضبط خاصية ForegroundTintAndShade لتفتيح أو تعتيم ألوان السمة الخاصة بك بسهولة، مما يعزز الجاذبية البصرية لتصميمك.
type: docs
weight: 60
url: /ar/net/aspose.words/shading/foregroundtintandshade/
---
## Shading.ForegroundTintAndShade property

يحصل على قيمة مزدوجة أو يعينها لتفتيح أو تعتيم لون السمة الأمامية.

```csharp
public double ForegroundTintAndShade { get; set; }
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentOutOfRangeException | قم بالرمي إذا قمت بتعيين هذه الخاصية إلى قيمة أقل من -1 أو أكثر من 1. |
| InvalidOperationException | قم برمي هذه الخاصية إذا قمت بتعيين كائن التظليل بألوان غير خاصة بالموضوع. |

## ملاحظات

القيم المسموح بها تتراوح من -1 (الأغمق) إلى 1 (الأفتح) لهذه الخاصية.

الصفر (0) محايد.

## أمثلة

يوضح كيفية تعيين ألوان المقدمة والخلفية لملمس التظليل.

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
