---
title: ParagraphFormat.Shading
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words لـ .NET
description: ParagraphFormat Shading ملكية. إرجاع أShading الكائن الذي يشير إلى تنسيق التظليل للفقرة في C#.
type: docs
weight: 280
url: /ar/net/aspose.words/paragraphformat/shading/
---
## ParagraphFormat.Shading property

إرجاع أ[`Shading`](../../shading/) الكائن الذي يشير إلى تنسيق التظليل للفقرة.

```csharp
public Shading Shading { get; }
```

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

### أنظر أيضا

* class [Shading](../../shading/)
* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
