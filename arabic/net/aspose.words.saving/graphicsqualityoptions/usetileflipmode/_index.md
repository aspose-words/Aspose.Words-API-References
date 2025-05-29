---
title: GraphicsQualityOptions.UseTileFlipMode
linktitle: UseTileFlipMode
articleTitle: UseTileFlipMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية GraphicsQualityOptions UseTileFlipMode للتحكم في إعدادات WrapMode لتحسين جودة الصورة في تطبيقاتك.
type: docs
weight: 80
url: /ar/net/aspose.words.saving/graphicsqualityoptions/usetileflipmode/
---
## GraphicsQualityOptions.UseTileFlipMode property

يحصل على علم يشير إلى ما إذا كان WrapMode هو TileFlipXY أو يعينه.

```csharp
public bool UseTileFlipMode { get; set; }
```

## ملاحظات

الWrapMode يحدد كيفية تبليط الملمس أو التدرج عندما يكون أصغر من المنطقة التي يتم ملؤها بمقدار x000d.

يستخدم بشكل افتراضيTile (يحدد التبليط دون التقليب). يؤدي هذا إلى عرض غير دقيق للصورة المقاسة (بدقة عالية).

تسمح هذه الخاصية بالتبديل إلى WrapModeTileFlipXY (يحدد أن البلاط يتم قلبه أفقيًا أثناء التحرك على طول الصف ويتم قلبه رأسيًا أثناء التحرك على طول العمود).

## أمثلة

يوضح كيفية منع ظهور الخط الأبيض عند العرض بدقة عالية.

```csharp
Document doc = new Document(MyDir + "Shape high dpi.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShapeRenderer renderer = shape.GetShapeRenderer();

ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png)
{
    Resolution = 500, GraphicsQualityOptions = new GraphicsQualityOptions { UseTileFlipMode = true }
};
renderer.Save(ArtifactsDir + "ImageSaveOptions.UseTileFlipMode.png", saveOptions);
```

### أنظر أيضا

* class [GraphicsQualityOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
