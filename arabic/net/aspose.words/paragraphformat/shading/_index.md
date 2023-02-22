---
title: ParagraphFormat.Shading
second_title: Aspose.Words لمراجع .NET API
description: ParagraphFormat ملكية. إرجاع كائن تظليل يشير إلى تنسيق التظليل للفقرة.
type: docs
weight: 270
url: /ar/net/aspose.words/paragraphformat/shading/
---
## ParagraphFormat.Shading property

إرجاع كائن تظليل يشير إلى تنسيق التظليل للفقرة.

```csharp
public Shading Shading { get; }
```

### أمثلة

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
* مساحة الاسم [Aspose.Words](../../paragraphformat/)
* المجسم [Aspose.Words](../../../)


