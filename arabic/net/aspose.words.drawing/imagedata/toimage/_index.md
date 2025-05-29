---
title: ImageData.ToImage
linktitle: ToImage
articleTitle: ToImage
second_title: Aspose.Words لـ .NET
description: استغلّ قوة طريقة ToImage في ImageData لاسترجاع الصور المُخزّنة في الأشكال ككائنات صور بسهولة. حسّن مشاريعك بسهولة!
type: docs
weight: 230
url: /ar/net/aspose.words.drawing/imagedata/toimage/
---
## ImageData.ToImage method

يحصل على الصورة المخزنة في الشكل كـImage الكائن.

```csharp
public Image ToImage()
```

## ملاحظات

جديدImage يتم إنشاء الكائن في كل مرة يتم فيها استدعاء هذه الطريقة.

تقع على عاتق المتصل مسؤولية التخلص من كائن الصورة.

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
