---
title: DocumentBuilder.InsertNode
linktitle: InsertNode
articleTitle: InsertNode
second_title: Aspose.Words لـ .NET
description: DocumentBuilder InsertNode طريقة. إدراج عقدة قبل المؤشر في C#.
type: docs
weight: 380
url: /ar/net/aspose.words/documentbuilder/insertnode/
---
## DocumentBuilder.InsertNode method

إدراج عقدة قبل المؤشر.

```csharp
public void InsertNode(Node node)
```

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

* class [Node](../../node/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
