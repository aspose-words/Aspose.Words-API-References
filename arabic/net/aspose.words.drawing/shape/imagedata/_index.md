---
title: Shape.ImageData
second_title: Aspose.Words لمراجع .NET API
description: Shape ملكية. يوفر الوصول إلى صورة الشكل. إرجاعباطل إذا كان الشكل لا يمكن أن يحتوي على صورة.
type: docs
weight: 110
url: /ar/net/aspose.words.drawing/shape/imagedata/
---
## Shape.ImageData property

يوفر الوصول إلى صورة الشكل. إرجاع`باطل` إذا كان الشكل لا يمكن أن يحتوي على صورة.

```csharp
public ImageData ImageData { get; }
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

يوضح كيفية إدراج صورة مرتبطة في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// فيما يلي طريقتان لتطبيق صورة على شكل حتى يتمكن من عرضها.
// 1 - قم بتعيين الشكل الذي يحتوي على الصورة.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// كل صورة نخزنها في شكلها ستزيد من حجم وثيقتنا.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - قم بتعيين الشكل للارتباط بملف صورة في نظام الملفات المحلي.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// سيؤدي الارتباط بالصور إلى توفير المساحة وينتج عنه مستند أصغر.
// ومع ذلك، يمكن للمستند عرض الصورة بشكل صحيح فقط while
// ملف الصورة موجود في الموقع الذي تشير إليه خاصية "SourceFullName" الخاصة بالشكل.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### أنظر أيضا

* class [ImageData](../../imagedata/)
* class [Shape](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shape/)
* المجسم [Aspose.Words](../../../)


