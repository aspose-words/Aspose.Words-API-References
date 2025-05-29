---
title: ImageData Class
linktitle: ImageData
articleTitle: ImageData
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.ImageData، الحل الأمثل لتحديد الصور وإدارتها في الأشكال. حسّن تصميم مستندك بسهولة!
type: docs
weight: 1390
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
| [BiLevel](../../aspose.words.drawing/imagedata/bilevel/) { get; set; } | يحدد ما إذا كانت الصورة سيتم عرضها باللونين الأبيض والأسود. |
| [Borders](../../aspose.words.drawing/imagedata/borders/) { get; } | يحصل على مجموعة حدود الصورة. الحدود لا تؤثر إلا على الصور المضمنة. |
| [Brightness](../../aspose.words.drawing/imagedata/brightness/) { get; set; } | يحصل على سطوع الصورة أو يضبطه. يجب أن تكون قيمة هذه الخاصية رقمًا من 0.0 (الأقل سطوعًا) إلى 1.0 (الأكثر سطوعًا). |
| [ChromaKey](../../aspose.words.drawing/imagedata/chromakey/) { get; set; } | يحدد قيمة لون الصورة التي سيتم التعامل معها على أنها شفافة. |
| [Contrast](../../aspose.words.drawing/imagedata/contrast/) { get; set; } | يحصل على تباين الصورة المحددة أو يضبطه. يجب أن تكون قيمة لهذه الخاصية رقمًا يتراوح بين 0.0 (أقل تباين) و1.0 (أعلى تباين). |
| [CropBottom](../../aspose.words.drawing/imagedata/cropbottom/) { get; set; } | يحدد جزء إزالة الصورة من الجانب السفلي. |
| [CropLeft](../../aspose.words.drawing/imagedata/cropleft/) { get; set; } | يحدد جزء إزالة الصورة من الجانب الأيسر. |
| [CropRight](../../aspose.words.drawing/imagedata/cropright/) { get; set; } | يحدد جزء إزالة الصورة من الجانب الأيمن. |
| [CropTop](../../aspose.words.drawing/imagedata/croptop/) { get; set; } | يحدد جزء إزالة الصورة من الجانب العلوي. |
| [GrayScale](../../aspose.words.drawing/imagedata/grayscale/) { get; set; } | يحدد ما إذا كانت الصورة سيتم عرضها في وضع التدرج الرمادي. |
| [HasImage](../../aspose.words.drawing/imagedata/hasimage/) { get; } | إرجاع`حقيقي` إذا كان الشكل يحتوي على بايتات صورة أو روابط صورة. |
| [ImageBytes](../../aspose.words.drawing/imagedata/imagebytes/) { get; set; } | يحصل على البايتات الخام للصورة المخزنة في الشكل أو يعينها. |
| [ImageSize](../../aspose.words.drawing/imagedata/imagesize/) { get; } | يحصل على معلومات حول حجم الصورة ودقتها. |
| [ImageType](../../aspose.words.drawing/imagedata/imagetype/) { get; } | يحصل على نوع الصورة. |
| [IsLink](../../aspose.words.drawing/imagedata/islink/) { get; } | إرجاع`حقيقي` إذا كانت الصورة مرتبطة بالشكل (عندما[`SourceFullName`](./sourcefullname/) (تم تحديده). |
| [IsLinkOnly](../../aspose.words.drawing/imagedata/islinkonly/) { get; } | إرجاع`حقيقي` إذا كانت الصورة مرتبطة ولم يتم تخزينها في المستند. |
| [SourceFullName](../../aspose.words.drawing/imagedata/sourcefullname/) { get; set; } | يحصل على مسار واسم ملف المصدر للصورة المرتبطة أو يعينهما. |
| [Title](../../aspose.words.drawing/imagedata/title/) { get; set; } | يحدد عنوان الصورة. |

## طُرق

| اسم | وصف |
| --- | --- |
| [FitImageToShape](../../aspose.words.drawing/imagedata/fitimagetoshape/)() | تناسب بيانات الصورة مع إطار الشكل بحيث تتطابق نسبة العرض إلى الارتفاع لبيانات الصورة مع نسبة العرض إلى الارتفاع لإطار الشكل. |
| [Save](../../aspose.words.drawing/imagedata/save/#save)(*Stream*) | يحفظ الصورة في التدفق المحدد. |
| [Save](../../aspose.words.drawing/imagedata/save/#save_1)(*string*) | يحفظ الصورة في ملف. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage)(*Image*) | يحدد الصورة التي يعرضها الشكل. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_1)(*Stream*) | يحدد الصورة التي يعرضها الشكل. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_2)(*string*) | يحدد الصورة التي يعرضها الشكل. |
| [ToByteArray](../../aspose.words.drawing/imagedata/tobytearray/)() | يعيد بايتات الصورة لأي صورة بغض النظر عما إذا كانت الصورة مخزنة أو مرتبطة. |
| [ToImage](../../aspose.words.drawing/imagedata/toimage/)() | يحصل على الصورة المخزنة في الشكل كـImage الكائن. |
| [ToStream](../../aspose.words.drawing/imagedata/tostream/)() | ينشئ ويعيد مجرى يحتوي على بايتات الصورة. |

## ملاحظات

استخدم[`ImageData`](../shape/imagedata/)الخاصية للوصول إلى الصورة وتعديلها داخل الشكل. لا تقم بإنشاء مثيلات من`ImageData` الصف مباشرة.

يمكن تخزين الصورة داخل شكل، أو ربطها بملف خارجي، أو كليهما (ربطها وتخزينها في المستند).

بغض النظر عما إذا كانت الصورة مخزنة داخل الشكل أو مرتبطة، يمكنك دائمًا الوصول إلى الصورة actual باستخدام[`ToByteArray`](./tobytearray/) ،[`ToStream`](./tostream/) ،[`ToImage`](./toimage/) أو[`Save`](./save/) methods. إذا تم تخزين الصورة داخل الشكل، فيمكنك أيضًا الوصول إليها مباشرةً باستخدام[`ImageBytes`](./imagebytes/) ملكية.

لتخزين صورة داخل شكل استخدم[`SetImage`](./setimage/) الطريقة. لربط صورة بشكل، اضبط[`SourceFullName`](./sourcefullname/) ملكية.

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

يوضح كيفية إدراج صورة مرتبطة في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// فيما يلي طريقتان لتطبيق صورة على شكل حتى يمكن عرضها.
// 1 - اضبط الشكل لاحتواء الصورة.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// كل صورة نقوم بتخزينها بالشكل المناسب سوف تؤدي إلى زيادة حجم مستندنا.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - قم بتعيين الشكل للارتباط بملف صورة في نظام الملفات المحلي.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// سيؤدي ربط الصور إلى توفير المساحة وسيؤدي إلى مستند أصغر حجمًا.
// ومع ذلك، لا يمكن للمستند عرض الصورة بشكل صحيح إلا أثناء
// ملف الصورة موجود في الموقع الذي يشير إليه خاصية "SourceFullName" الخاصة بالشكل.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
