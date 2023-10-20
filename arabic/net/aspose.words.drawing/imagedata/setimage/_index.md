---
title: ImageData.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words لـ .NET
description: ImageData SetImage طريقة. يضبط الصورة التي يعرضها الشكل في C#.
type: docs
weight: 200
url: /ar/net/aspose.words.drawing/imagedata/setimage/
---
## SetImage(*Image*) {#setimage}

يضبط الصورة التي يعرضها الشكل.

```csharp
public void SetImage(Image image)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| image | Image | كائن الصورة. |

## أمثلة

يوضح كيفية عرض الصور من نظام الملفات المحلي في المستند.

```csharp
Document doc = new Document();

// لعرض صورة في مستند، سنحتاج إلى إنشاء شكل
// الذي سيحتوي على صورة، ثم يُلحقها بنص المستند.
Shape imgShape;

// فيما يلي طريقتان للحصول على صورة من ملف في نظام الملفات المحلي.
// 1 - إنشاء كائن صورة من ملف صورة:
using (Image srcImage = Image.FromFile(ImageDir + "Logo.jpg"))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(srcImage);
}

// 2 - افتح ملف صورة من نظام الملفات المحلي باستخدام الدفق:
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

يضبط الصورة التي يعرضها الشكل.

```csharp
public void SetImage(Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | الدفق الذي يحتوي على الصورة. |

## أمثلة

يوضح كيفية عرض الصور من نظام الملفات المحلي في المستند.

```csharp
Document doc = new Document();

// لعرض صورة في مستند، سنحتاج إلى إنشاء شكل
// الذي سيحتوي على صورة، ثم يُلحقها بنص المستند.
Shape imgShape;

// فيما يلي طريقتان للحصول على صورة من ملف في نظام الملفات المحلي.
// 1 - إنشاء كائن صورة من ملف صورة:
using (Image srcImage = Image.FromFile(ImageDir + "Logo.jpg"))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(srcImage);
}

// 2 - افتح ملف صورة من نظام الملفات المحلي باستخدام الدفق:
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

يضبط الصورة التي يعرضها الشكل.

```csharp
public void SetImage(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | ملف الصورة. يمكن أن يكون اسم ملف أو عنوان URL. |

## أمثلة

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

* class [ImageData](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
