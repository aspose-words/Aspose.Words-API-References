---
title: ImageData Class
linktitle: ImageData
articleTitle: ImageData
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.ImageData فصل. يحدد صورة للشكل في C#.
type: docs
weight: 1060
url: /ar/net/aspose.words.drawing/imagedata/
---
## ImageData class

يحدد صورة للشكل.

لمعرفة المزيد، قم بزيارة[العمل مع الصور](https://docs.aspose.com/words/net/working-with-images/) مقالة توثيقية.

```csharp
public class ImageData
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [BiLevel](../../aspose.words.drawing/imagedata/bilevel/) { get; set; } | يحدد ما إذا كان سيتم عرض الصورة بالأبيض والأسود. |
| [Borders](../../aspose.words.drawing/imagedata/borders/) { get; } | الحصول على مجموعة حدود الصورة. الحدود لها تأثير فقط على الصور المضمنة. |
| [Brightness](../../aspose.words.drawing/imagedata/brightness/) { get; set; } | الحصول على سطوع الصورة أو تعيينه. يجب أن تكون قيمة هذه الخاصية رقمًا من 0.0 (الأخفت) إلى 1.0 (الألمع). |
| [ChromaKey](../../aspose.words.drawing/imagedata/chromakey/) { get; set; } | يحدد قيمة اللون للصورة التي سيتم التعامل معها على أنها شفافة. |
| [Contrast](../../aspose.words.drawing/imagedata/contrast/) { get; set; } | الحصول على أو تعيين التباين للصورة المحددة. يجب أن تكون قيمة value لهذه الخاصية رقمًا يتراوح بين 0.0 (أقل تباين) إلى 1.0 (أكبر تباين). |
| [CropBottom](../../aspose.words.drawing/imagedata/cropbottom/) { get; set; } | يحدد جزء إزالة الصورة من الجانب السفلي. |
| [CropLeft](../../aspose.words.drawing/imagedata/cropleft/) { get; set; } | يحدد جزء إزالة الصورة من الجانب الأيسر. |
| [CropRight](../../aspose.words.drawing/imagedata/cropright/) { get; set; } | يحدد جزء إزالة الصورة من الجانب الأيمن. |
| [CropTop](../../aspose.words.drawing/imagedata/croptop/) { get; set; } | يحدد جزء إزالة الصورة من الجانب العلوي. |
| [GrayScale](../../aspose.words.drawing/imagedata/grayscale/) { get; set; } | يحدد ما إذا كانت الصورة سيتم عرضها في وضع التدرج الرمادي. |
| [HasImage](../../aspose.words.drawing/imagedata/hasimage/) { get; } | إرجاع`حقيقي` إذا كان الشكل يحتوي على بايتات صورة أو يربط صورة. |
| [ImageBytes](../../aspose.words.drawing/imagedata/imagebytes/) { get; set; } | الحصول على أو تعيين البايتات الأولية للصورة المخزنة في الشكل. |
| [ImageSize](../../aspose.words.drawing/imagedata/imagesize/) { get; } | الحصول على معلومات حول حجم الصورة ودقتها. |
| [ImageType](../../aspose.words.drawing/imagedata/imagetype/) { get; } | الحصول على نوع الصورة. |
| [IsLink](../../aspose.words.drawing/imagedata/islink/) { get; } | إرجاع`حقيقي` إذا كانت الصورة مرتبطة بالشكل (متى[`SourceFullName`](./sourcefullname/) تم تحديده). |
| [IsLinkOnly](../../aspose.words.drawing/imagedata/islinkonly/) { get; } | إرجاع`حقيقي` إذا كانت الصورة مرتبطة وغير مخزنة في المستند. |
| [SourceFullName](../../aspose.words.drawing/imagedata/sourcefullname/) { get; set; } | الحصول على أو تعيين مسار واسم الملف المصدر للصورة المرتبطة. |
| [Title](../../aspose.words.drawing/imagedata/title/) { get; set; } | يحدد عنوان الصورة. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Save](../../aspose.words.drawing/imagedata/save/#save)(*Stream*) | يحفظ الصورة في الدفق المحدد. |
| [Save](../../aspose.words.drawing/imagedata/save/#save_1)(*string*) | يحفظ الصورة في ملف. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage)(*Image*) | يضبط الصورة التي يعرضها الشكل. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_1)(*Stream*) | يضبط الصورة التي يعرضها الشكل. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_2)(*string*) | يضبط الصورة التي يعرضها الشكل. |
| [ToByteArray](../../aspose.words.drawing/imagedata/tobytearray/)() | إرجاع بايتات الصورة لأي صورة بغض النظر عما إذا كانت الصورة مخزنة أو مرتبطة. |
| [ToImage](../../aspose.words.drawing/imagedata/toimage/)() | يحصل على الصورة المخزنة بالشكل aImage الكائن. |
| [ToStream](../../aspose.words.drawing/imagedata/tostream/)() | إنشاء وإرجاع دفق يحتوي على بايتات الصورة. |

## ملاحظات

استخدم ال[`ImageData`](../shape/imagedata/) الخاصية للوصول إلى الصورة وتعديلها داخل الشكل. لا تقم بإنشاء مثيلات لـ`ImageData` الصف مباشرة.

يمكن تخزين الصورة داخل شكل أو ربطها بملف خارجي أو كليهما (ربطها وتخزينها في المستند).

بغض النظر عما إذا كانت الصورة مخزنة داخل الشكل أو مرتبطة، يمكنك دائمًا الوصول إلى الصورة الفعلية باستخدام[`ToByteArray`](./tobytearray/) ,[`ToStream`](./tostream/) ,[`ToImage`](./toimage/) أو[`Save`](./save/) methods. إذا كانت الصورة مخزنة داخل الشكل، فيمكنك أيضًا الوصول إليها مباشرة باستخدام[`ImageBytes`](./imagebytes/) ملكية.

لتخزين صورة داخل شكل، استخدم[`SetImage`](./setimage/) طريقة. لربط صورة بشكل ما، قم بتعيين[`SourceFullName`](./sourcefullname/) ملكية.

## أمثلة

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

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
