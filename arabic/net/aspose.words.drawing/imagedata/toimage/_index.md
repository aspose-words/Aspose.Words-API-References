---
title: ImageData.ToImage
second_title: Aspose.Words لمراجع .NET API
description: ImageData طريقة. يحصل على الصورة المخزنة بالشكل كملفImage الكائن .
type: docs
weight: 220
url: /ar/net/aspose.words.drawing/imagedata/toimage/
---
## ImageData.ToImage method

يحصل على الصورة المخزنة بالشكل كملفImage الكائن .

```csharp
public Image ToImage()
```

### ملاحظات

جديدImage يتم إنشاء الكائن في كل مرة يتم استدعاء هذه الطريقة.

تقع على عاتق المتصل مسؤولية التخلص من كائن الصورة.

### أمثلة

يوضح كيفية حفظ جميع الصور من مستند إلى نظام الملفات.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

// الأشكال مع مخزن مجموعة العلامات "HasImage" وعرض جميع صور المستند.
IEnumerable<Shape> shapesWithImages = 
    imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Where(s => s.HasImage);

// اذهب من خلال كل شكل واحفظ صورته.
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


