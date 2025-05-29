---
title: ImageSaveOptions.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة ImageSaveOptions Clone لإنشاء استنساخ عميق لكائناتك بسهولة، مما يعزز كفاءة الترميز ومرونته.
type: docs
weight: 210
url: /ar/net/aspose.words.saving/imagesaveoptions/clone/
---
## ImageSaveOptions.Clone method

ينشئ نسخة طبق الأصل عميقة من هذا الكائن.

```csharp
public ImageSaveOptions Clone()
```

## أمثلة

يوضح كيفية تحديد معدل البت لكل بكسل الذي سيتم به تحويل المستند إلى صورة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// عندما نحفظ المستند كصورة، يمكننا تمرير كائن SaveOptions إلى
// حدد تنسيق البكسل للصورة التي سيتم إنشاءها من خلال عملية الحفظ.
// ستؤثر معدلات البت المختلفة لكل بكسل على جودة وحجم ملف الصورة المولدة.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PixelFormat = imagePixelFormat;

//يمكننا استنساخ مثيلات ImageSaveOptions.
Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

### أنظر أيضا

* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
