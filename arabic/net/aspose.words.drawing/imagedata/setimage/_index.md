---
title: ImageData.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية استخدام طريقة SetImage في ImageData لتحسين أشكالك بصور مخصصة. ارتقِ بتصميمك بكل سهولة!
type: docs
weight: 210
url: /ar/net/aspose.words.drawing/imagedata/setimage/
---
## SetImage(*Image*) {#setimage}

يحدد الصورة التي يعرضها الشكل.

```csharp
public void SetImage(Image image)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| image | Image | كائن الصورة. |

## أمثلة

يوضح كيفية عرض الصور من نظام الملفات المحلي في مستند.

```csharp
Document doc = new Document();

// لعرض صورة في مستند، سنحتاج إلى إنشاء شكل
// والتي سوف تحتوي على صورة، ثم إضافتها إلى نص المستند.
Shape imgShape;

// فيما يلي طريقتان للحصول على صورة من ملف في نظام الملفات المحلي.
// 1 - إنشاء كائن صورة من ملف صورة:
using (Image srcImage = Image.FromFile(ImageDir + "Logo.jpg"))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(srcImage);
}

// 2 - فتح ملف صورة من نظام الملفات المحلي باستخدام دفق:
using (Stream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(stream);
    imgShape.Left = 150.0f;
}

doc.Save(ArtifactsDir + "Drawing.ImportImage.docx");
```

### أنظر أيضا

* class [ImageData](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)

---

## SetImage(*Stream*) {#setimage_1}

يحدد الصورة التي يعرضها الشكل.

```csharp
public void SetImage(Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | الدفق الذي يحتوي على الصورة. |

## أمثلة

يوضح كيفية عرض الصور من نظام الملفات المحلي في مستند.

```csharp
Document doc = new Document();

// لعرض صورة في مستند، سنحتاج إلى إنشاء شكل
// والتي سوف تحتوي على صورة، ثم إضافتها إلى نص المستند.
Shape imgShape;

// فيما يلي طريقتان للحصول على صورة من ملف في نظام الملفات المحلي.
// 1 - إنشاء كائن صورة من ملف صورة:
using (Image srcImage = Image.FromFile(ImageDir + "Logo.jpg"))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(srcImage);
}

// 2 - فتح ملف صورة من نظام الملفات المحلي باستخدام دفق:
using (Stream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(stream);
    imgShape.Left = 150.0f;
}

doc.Save(ArtifactsDir + "Drawing.ImportImage.docx");
```

### أنظر أيضا

* class [ImageData](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)

---

## SetImage(*string*) {#setimage_2}

يحدد الصورة التي يعرضها الشكل.

```csharp
public void SetImage(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | ملف الصورة. يمكن أن يكون اسم ملف أو رابط URL. |

## أمثلة

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

* class [ImageData](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
