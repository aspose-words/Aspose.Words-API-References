---
title: Shape.HasImage
second_title: Aspose.Words لمراجع .NET API
description: Shape ملكية. إرجاعحقيقي إذا كان الشكل يحتوي على بايتات صورة أو يربط صورة.
type: docs
weight: 80
url: /ar/net/aspose.words.drawing/shape/hasimage/
---
## Shape.HasImage property

إرجاع`حقيقي` إذا كان الشكل يحتوي على بايتات صورة أو يربط صورة.

```csharp
public bool HasImage { get; }
```

### أمثلة

يوضح كيفية حذف جميع الأشكال التي تحتوي على صور من مستند.

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

* class [Shape](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shape/)
* المجسم [Aspose.Words](../../../)


