---
title: ImageData.ToImage
second_title: Aspose.Words لمراجع .NET API
description: ImageData طريقة. يحصل على الصورة المخزنة بالشكل aImage الكائن.
type: docs
weight: 230
url: /ar/net/aspose.words.drawing/imagedata/toimage/
---
## ImageData.ToImage method

يحصل على الصورة المخزنة بالشكل aImage الكائن.

```csharp
public Image ToImage()
```

### ملاحظات

جديدImage يتم إنشاء الكائن في كل مرة يتم فيها استدعاء هذه الطريقة.

تقع على عاتق المتصل مسؤولية التخلص من كائن الصورة.

### أمثلة

يوضح كيفية حفظ جميع الصور من مستند إلى نظام الملفات.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

// الأشكال ذات مجموعة العلامات "HasImage" تخزن جميع صور المستند وتعرضها.
IEnumerable<Shape> shapesWithImages = 
    imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Where(s => s.HasImage);

// تصفح كل شكل واحفظ صورته.
ImageFormatConverter formatConverter = new ImageFormatConverter();

using (IEnumerator<Shape> enumerator = shapesWithImages.GetEnumerator())
{
    int shapeIndex = 0;

    while (enumerator.MoveNext())
    {
        ImageData imageData = enumerator.Current.ImageData;
        ImageFormat format = imageData.ToImage().RawFormat;
        string fileExtension = formatConverter.ConvertToString(format);

        using (FileStream fileStream = File.Create(ArtifactsDir + $"Drawing.SaveAllImages.{++shapeIndex}.{fileExtension}"))
            imageData.Save(fileStream);
    }
}
```

### أنظر أيضا

* class [ImageData](../)
* مساحة الاسم [Aspose.Words.Drawing](../../imagedata/)
* المجسم [Aspose.Words](../../../)


