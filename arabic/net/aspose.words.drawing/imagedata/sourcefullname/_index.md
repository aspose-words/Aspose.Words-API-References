---
title: ImageData.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ImageData SourceFullName لإدارة مسارات الصور وأسماء الملفات المرتبطة بسهولة، مما يعزز كفاءة التعامل مع الصور.
type: docs
weight: 170
url: /ar/net/aspose.words.drawing/imagedata/sourcefullname/
---
## ImageData.SourceFullName property

يحصل على مسار واسم ملف المصدر للصورة المرتبطة أو يعينهما.

```csharp
public string SourceFullName { get; set; }
```

## ملاحظات

القيمة الافتراضية هي سلسلة فارغة.

لو`SourceFullName` ليست سلسلة فارغة، الصورة مرتبطة.

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
