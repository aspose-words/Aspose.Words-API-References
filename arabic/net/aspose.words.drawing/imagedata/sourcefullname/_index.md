---
title: ImageData.SourceFullName
second_title: Aspose.Words لمراجع .NET API
description: ImageData ملكية. الحصول على أو تعيين مسار واسم الملف المصدر للصورة المرتبطة.
type: docs
weight: 170
url: /ar/net/aspose.words.drawing/imagedata/sourcefullname/
---
## ImageData.SourceFullName property

الحصول على أو تعيين مسار واسم الملف المصدر للصورة المرتبطة.

```csharp
public string SourceFullName { get; set; }
```

### ملاحظات

القيمة الافتراضية هي سلسلة فارغة.

لو`SourceFullName` ليست سلسلة فارغة، الصورة مرتبطة.

### أمثلة

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
* مساحة الاسم [Aspose.Words.Drawing](../../imagedata/)
* المجسم [Aspose.Words](../../../)


