---
title: Shading.ForegroundPatternColor
linktitle: ForegroundPatternColor
articleTitle: ForegroundPatternColor
second_title: Aspose.Words لـ .NET
description: Shading ForegroundPatternColor ملكية. الحصول على أو تعيين اللون المطبق على مقدمة الصورةShading الكائن في C#.
type: docs
weight: 40
url: /ar/net/aspose.words/shading/foregroundpatterncolor/
---
## Shading.ForegroundPatternColor property

الحصول على أو تعيين اللون المطبق على مقدمة الصورة[`Shading`](../) الكائن.

```csharp
public Color ForegroundPatternColor { get; set; }
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

* class [Shading](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
