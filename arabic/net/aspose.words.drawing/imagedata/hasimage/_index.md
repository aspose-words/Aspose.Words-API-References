---
title: ImageData.HasImage
linktitle: HasImage
articleTitle: HasImage
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ImageData HasImage. تحقق سريعًا مما إذا كان الشكل يحتوي على بايتات صور أو روابط، مما يُحسّن سير عمل تصميمك بسهولة.
type: docs
weight: 110
url: /ar/net/aspose.words.drawing/imagedata/hasimage/
---
## ImageData.HasImage property

إرجاع`حقيقي` إذا كان الشكل يحتوي على بايتات صورة أو روابط صورة.

```csharp
public bool HasImage { get; }
```

## أمثلة

يوضح كيفية حفظ كافة الصور من مستند إلى نظام الملفات.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

// الأشكال التي تحمل علامة "HasImage" تخزن وتعرض كافة صور المستند.
Shape[] shapesWithImages = imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>()
    .Where(s => s.HasImage).ToArray();

// قم بالمرور على كل شكل وحفظ صورته.
for (int shapeIndex = 0; shapeIndex < shapesWithImages.Length; ++shapeIndex)
{
    ImageData imageData = shapesWithImages[shapeIndex].ImageData;
    using (FileStream fileStream = File.Create(ArtifactsDir + $"Drawing.SaveAllImages.{shapeIndex + 1}.{imageData.ImageType}"))
        imageData.Save(fileStream);
}
```

### أنظر أيضا

* class [ImageData](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
