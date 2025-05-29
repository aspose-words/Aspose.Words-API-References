---
title: ParagraphFormat.Shading
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية التظليل في ParagraphFormat لتحسين تنسيق النص. استخدم خاصية التظليل لتحسين مظهر فقرتك بصريًا بسهولة.
type: docs
weight: 290
url: /ar/net/aspose.words/paragraphformat/shading/
---
## ParagraphFormat.Shading property

يعيد[`Shading`](../../shading/) الكائن الذي يشير إلى تنسيق التظليل للفقرة.

```csharp
public Shading Shading { get; }
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

* class [Shading](../../shading/)
* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
