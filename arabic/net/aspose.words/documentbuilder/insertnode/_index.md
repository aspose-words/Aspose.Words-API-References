---
title: DocumentBuilder.InsertNode
linktitle: InsertNode
articleTitle: InsertNode
second_title: Aspose.Words لـ .NET
description: حسّن عملية إنشاء مستنداتك باستخدام طريقة InsertNode في DocumentBuilder. أدرج العقد قبل المؤشر بسهولة لتحرير سلس!
type: docs
weight: 410
url: /ar/net/aspose.words/documentbuilder/insertnode/
---
## DocumentBuilder.InsertNode method

يقوم بإدراج عقدة قبل المؤشر.

```csharp
public void InsertNode(Node node)
```

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

* class [Node](../../node/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
