---
title: ImageData.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words لـ .NET
description: احفظ الصور بسهولة باستخدام طريقة حفظ ImageData. بسّط سير عملك بتخزين الصور مباشرةً في المسار الذي اخترته بسهولة.
type: docs
weight: 200
url: /ar/net/aspose.words.drawing/imagedata/save/
---
## Save(*Stream*) {#save}

يحفظ الصورة في التدفق المحدد.

```csharp
public void Save(Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | المكان الذي تريد حفظ الصورة فيه. |

## ملاحظات

هل تقع على عاتق المتصل مسؤولية التخلص من كائن التدفق؟

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

---

## Save(*string*) {#save_1}

يحفظ الصورة في ملف.

```csharp
public void Save(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم الملف الذي تريد حفظ الصورة فيه. |

## أمثلة

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

* class [ImageData](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
