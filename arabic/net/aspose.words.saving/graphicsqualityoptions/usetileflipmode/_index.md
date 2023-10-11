---
title: GraphicsQualityOptions.UseTileFlipMode
second_title: Aspose.Words لمراجع .NET API
description: GraphicsQualityOptions ملكية. الحصول على علامة تشير إلى ما إذا كان WrapMode هو TileFlipXY أو تعيينها.
type: docs
weight: 80
url: /ar/net/aspose.words.saving/graphicsqualityoptions/usetileflipmode/
---
## GraphicsQualityOptions.UseTileFlipMode property

الحصول على علامة تشير إلى ما إذا كان WrapMode هو TileFlipXY أو تعيينها.

```csharp
public bool UseTileFlipMode { get; set; }
```

### ملاحظات

الWrapMode يحدد كيفية تجانب المادة أو التدرج عندما يكون أصغر من المساحة التي يتم ملؤها.

حسب الاستخدامات الافتراضيةTile (يحدد التبليط دون التقليب). يؤدي هذا إلى عرض غير دقيق للصورة التي تم تغيير حجمها (بدقة عالية).

تسمح هذه الخاصية بتبديل WrapMode إلىTileFlipXY (يحدد أنه يتم قلب المربعات أفقيًا أثناء تحركك على طول الصف وقلبها رأسيًا أثناء تحركك على طول عمود).

### أمثلة

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
* مساحة الاسم [Aspose.Words.Saving](../../graphicsqualityoptions/)
* المجسم [Aspose.Words](../../../)


