---
title: Class ImageData
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.ImageData فصل. يحدد صورة لشكل .
type: docs
weight: 930
url: /ar/net/aspose.words.drawing/imagedata/
---
## ImageData class

يحدد صورة لشكل .

```csharp
public class ImageData
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [BiLevel](../../aspose.words.drawing/imagedata/bilevel/) { get; set; } | لتحديد ما إذا كان سيتم عرض الصورة بالأبيض والأسود. |
| [Borders](../../aspose.words.drawing/imagedata/borders/) { get; } | يحصل على مجموعة حدود الصورة. الحدود لها تأثير فقط على الصور المضمنة . |
| [Brightness](../../aspose.words.drawing/imagedata/brightness/) { get; set; } | الحصول على سطوع الصورة أو ضبطه . يجب أن تكون قيمة هذه الخاصية رقمًا من 0.0 (خافت) إلى 1.0 (الأكثر سطوعًا) . |
| [ChromaKey](../../aspose.words.drawing/imagedata/chromakey/) { get; set; } | يحدد قيمة اللون للصورة التي سيتم التعامل معها على أنها شفافة. |
| [Contrast](../../aspose.words.drawing/imagedata/contrast/) { get; set; } | الحصول على أو تحديد التباين للصورة المحددة. يجب أن تكون قيمة value لهذه الخاصية عددًا من 0.0 (أقل تباين) إلى 1.0 (أكبر تباين) . |
| [CropBottom](../../aspose.words.drawing/imagedata/cropbottom/) { get; set; } | يحدد جزء إزالة الصورة من الجانب السفلي. |
| [CropLeft](../../aspose.words.drawing/imagedata/cropleft/) { get; set; } | يحدد جزء إزالة الصورة من الجانب الأيسر. |
| [CropRight](../../aspose.words.drawing/imagedata/cropright/) { get; set; } | يحدد جزء إزالة الصورة من الجانب الأيمن. |
| [CropTop](../../aspose.words.drawing/imagedata/croptop/) { get; set; } | يحدد جزء إزالة الصورة من الجانب العلوي. |
| [GrayScale](../../aspose.words.drawing/imagedata/grayscale/) { get; set; } | لتحديد ما إذا كان سيتم عرض الصورة في وضع التدرج الرمادي. |
| [HasImage](../../aspose.words.drawing/imagedata/hasimage/) { get; } | إرجاع صحيح إذا كان للشكل بايت صورة أو ربط صورة. |
| [ImageBytes](../../aspose.words.drawing/imagedata/imagebytes/) { get; set; } | الحصول على أو تعيين وحدات البايت الأولية للصورة المخزنة بالشكل. |
| [ImageSize](../../aspose.words.drawing/imagedata/imagesize/) { get; } | الحصول على معلومات حول حجم الصورة ودقتها. |
| [ImageType](../../aspose.words.drawing/imagedata/imagetype/) { get; } | يحصل على نوع الصورة. |
| [IsLink](../../aspose.words.drawing/imagedata/islink/) { get; } | يعود صحيحًا إذا كانت الصورة مرتبطة بالشكل (متى[`SourceFullName`](./sourcefullname/) محدد) . |
| [IsLinkOnly](../../aspose.words.drawing/imagedata/islinkonly/) { get; } | إرجاع صحيح إذا كانت الصورة مرتبطة وغير مخزنة في المستند. |
| [SourceFullName](../../aspose.words.drawing/imagedata/sourcefullname/) { get; set; } | الحصول على أو تحديد مسار واسم الملف المصدر للصورة المرتبطة. |
| [Title](../../aspose.words.drawing/imagedata/title/) { get; set; } | يحدد عنوان الصورة. _ |

## طُرق

| اسم | وصف |
| --- | --- |
| [Save](../../aspose.words.drawing/imagedata/save/#save)(Stream) | يحفظ الصورة في الدفق المحدد. |
| [Save](../../aspose.words.drawing/imagedata/save/#save_1)(string) | يحفظ الصورة في ملف . |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage)(Image) | يضبط الصورة التي يعرضها الشكل. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_1)(Stream) | يضبط الصورة التي يعرضها الشكل. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_2)(string) | يضبط الصورة التي يعرضها الشكل. |
| [ToByteArray](../../aspose.words.drawing/imagedata/tobytearray/)() | إرجاع بايت الصورة لأي صورة بغض النظر عما إذا كانت الصورة مخزنة أو مرتبطة. |
| [ToImage](../../aspose.words.drawing/imagedata/toimage/)() | يحصل على الصورة المخزنة بالشكل كملفImage الكائن . |
| [ToStream](../../aspose.words.drawing/imagedata/tostream/)() | إنشاء وإرجاع دفق يحتوي على بايت الصورة. |

### ملاحظات

استخدم ال[`ImageData`](../shape/imagedata/) للوصول إلى الصورة وتعديلها داخل الشكل . لا يمكنك إنشاء مثيلات من`ImageData` فئة مباشرة.

يمكن تخزين الصورة داخل شكل أو ربطها بملف خارجي أو كليهما (مرتبطة ومخزنة في المستند).

بغض النظر عما إذا كانت الصورة مخزنة داخل الشكل أو مرتبطة ، يمكنك دائمًا الوصول إلى الصورة الفعلية باستخدام[`ToByteArray`](./tobytearray/) و[`ToStream`](./tostream/) و[`ToImage`](./toimage/) أو[`Save`](./save/) طرق . إذا تم تخزين الصورة داخل الشكل ، يمكنك أيضًا الوصول إليها مباشرةً باستخدام ملف[`ImageBytes`](./imagebytes/) منشأه.

لتخزين صورة داخل شكل ، استخدم ملف[`SetImage`](./setimage/) طريقة. لربط صورة بشكل ما ، قم بتعيين ملف[`SourceFullName`](./sourcefullname/) منشأه.

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

يوضح كيفية إدراج صورة مرتبطة في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// فيما يلي طريقتان لتطبيق صورة على شكل بحيث يمكن عرضها.
// 1 - اضبط الشكل ليحتوي على الصورة.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// كل صورة نقوم بتخزينها بالشكل ستزيد من حجم وثيقتنا.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - اضبط الشكل للارتباط بملف صورة في نظام الملفات المحلي.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// سيوفر الارتباط بالصور مساحة وينتج عنه مستند أصغر.
// ومع ذلك ، يمكن للمستند فقط عرض الصورة بشكل صحيح أثناء
// ملف الصورة موجود في الموقع الذي تشير إليه خاصية "SourceFullName" للشكل.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)


