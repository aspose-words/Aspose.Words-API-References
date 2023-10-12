---
title: ImageData.ImageType
second_title: Aspose.Words لمراجع .NET API
description: ImageData ملكية. الحصول على نوع الصورة.
type: docs
weight: 140
url: /ar/net/aspose.words.drawing/imagedata/imagetype/
---
## ImageData.ImageType property

الحصول على نوع الصورة.

```csharp
public ImageType ImageType { get; }
```

### أمثلة

يوضح كيفية استخراج الصور من مستند وحفظها في نظام الملفات المحلي كملفات فردية.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// احصل على مجموعة الأشكال من المستند،
// وحفظ بيانات الصورة لكل شكل مع صورة كملف في نظام الملفات المحلي.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // قد تحتوي بيانات صورة الأشكال على صور للعديد من تنسيقات الصور الممكنة.
        // يمكننا تحديد امتداد الملف لكل صورة تلقائيًا، بناءً على تنسيقها.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

### أنظر أيضا

* enum [ImageType](../../imagetype/)
* class [ImageData](../)
* مساحة الاسم [Aspose.Words.Drawing](../../imagedata/)
* المجسم [Aspose.Words](../../../)


