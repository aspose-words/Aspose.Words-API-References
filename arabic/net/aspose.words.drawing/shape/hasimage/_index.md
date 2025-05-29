---
title: Shape.HasImage
linktitle: HasImage
articleTitle: HasImage
second_title: Aspose.Words لـ .NET
description: اكتشف ما إذا كان الشكل يحتوي على بيانات صورة أو رابط لها باستخدام خاصية HasImage. حسّن تصميماتك بسهولة!
type: docs
weight: 90
url: /ar/net/aspose.words.drawing/shape/hasimage/
---
## Shape.HasImage property

إرجاع`حقيقي` إذا كان الشكل يحتوي على بايتات صورة أو روابط صورة.

```csharp
public bool HasImage { get; }
```

## أمثلة

يوضح كيفية حذف كافة الأشكال التي تحتوي على صور من مستند.

```csharp
Document doc = new Document(MyDir + "Images.docx");
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.OfType<Shape>().Count(s => s.HasImage));

foreach (Shape shape in shapes.OfType<Shape>())
    if (shape.HasImage) 
        shape.Remove();

Assert.AreEqual(0, shapes.OfType<Shape>().Count(s => s.HasImage));
```

يوضح كيفية استخراج الصور من مستند وحفظها في نظام الملفات المحلي كملفات فردية.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// الحصول على مجموعة الأشكال من المستند،
// وحفظ بيانات الصورة لكل شكل مع الصورة كملف في نظام الملفات المحلي.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // قد تحتوي بيانات الصورة الخاصة بالأشكال على صور بتنسيقات صور متعددة محتملة.
        // يمكننا تحديد امتداد الملف لكل صورة تلقائيًا، استنادًا إلى تنسيقها.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

### أنظر أيضا

* class [Shape](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
