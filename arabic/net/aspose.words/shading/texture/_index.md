---
title: Shading.Texture
linktitle: Texture
articleTitle: Texture
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية "نسيج التظليل" لتحسين تصميماتك. خصّص وعيّن القوام بسهولة للحصول على تأثيرات بصرية مذهلة في مشاريعك.
type: docs
weight: 70
url: /ar/net/aspose.words/shading/texture/
---
## Shading.Texture property

يحصل على نسيج التظليل أو يعينه.

```csharp
public TextureIndex Texture { get; set; }
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

* enum [TextureIndex](../../textureindex/)
* class [Shading](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
