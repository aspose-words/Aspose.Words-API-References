---
title: ImageData.Save
second_title: Aspose.Words لمراجع .NET API
description: ImageData طريقة. يحفظ الصورة في الدفق المحدد.
type: docs
weight: 190
url: /ar/net/aspose.words.drawing/imagedata/save/
---
## Save(Stream) {#save}

يحفظ الصورة في الدفق المحدد.

```csharp
public void Save(Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | الدفق حيث يتم حفظ الصورة فيه. |

### ملاحظات

هل من مسؤولية المتصل التخلص من كائن الدفق.

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

---

## Save(string) {#save_1}

يحفظ الصورة في ملف .

```csharp
public void Save(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم الملف حيث يتم حفظ الصورة. |

### أمثلة

يوضح كيفية استخراج الصور من مستند ، وحفظها في نظام الملفات المحلي كملفات فردية.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// احصل على مجموعة الأشكال من المستند ،
// وحفظ بيانات الصورة لكل شكل مع صورة كملف في نظام الملفات المحلي.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
        // قد تحتوي بيانات صور الأشكال على صور للعديد من تنسيقات الصور الممكنة. 
        // يمكننا تحديد امتداد ملف لكل صورة تلقائيًا ، بناءً على تنسيقها.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

### أنظر أيضا

* class [ImageData](../)
* مساحة الاسم [Aspose.Words.Drawing](../../imagedata/)
* المجسم [Aspose.Words](../../../)


