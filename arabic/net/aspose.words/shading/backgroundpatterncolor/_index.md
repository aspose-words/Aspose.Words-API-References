---
title: Shading.BackgroundPatternColor
linktitle: BackgroundPatternColor
articleTitle: BackgroundPatternColor
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Shading BackgroundPatternColor لتخصيص لون خلفية كائن التظليل الخاص بك، مما يعزز الجاذبية البصرية لتصميمك.
type: docs
weight: 10
url: /ar/net/aspose.words/shading/backgroundpatterncolor/
---
## Shading.BackgroundPatternColor property

يحصل على اللون الذي يتم تطبيقه على خلفية[`Shading`](../) الكائن.

```csharp
public Color BackgroundPatternColor { get; set; }
```

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

### أنظر أيضا

* class [Shading](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
