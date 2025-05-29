---
title: ImageSaveOptions.ImageColorMode
linktitle: ImageColorMode
articleTitle: ImageColorMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ImageSaveOptions ImageColorMode لتخصيص وتحسين وضع الألوان للصور المُولّدة بسهولة. حسّن صورك اليوم!
type: docs
weight: 50
url: /ar/net/aspose.words.saving/imagesaveoptions/imagecolormode/
---
## ImageSaveOptions.ImageColorMode property

يحصل على وضع اللون للصور المولدة أو يعينه.

```csharp
public ImageColorMode ImageColorMode { get; set; }
```

## ملاحظات

لا يكون لهذه الخاصية تأثير إلا عند الحفظ بتنسيقات الصور النقطية.

القيمة الافتراضية هيNone.

## أمثلة

يوضح كيفية تعيين وضع الألوان عند عرض المستندات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// عندما نحفظ المستند كصورة، يمكننا تمرير كائن SaveOptions إلى
// حدد وضع اللون للصورة التي سيتم إنشاءها من خلال عملية الحفظ.
// إذا قمنا بتعيين خاصية "ImageColorMode" إلى "ImageColorMode.BlackAndWhite"،
// ستطبق عملية الحفظ تقليل لون التدرج الرمادي أثناء عرض المستند.
 // إذا قمنا بتعيين خاصية "ImageColorMode" إلى "ImageColorMode.Grayscale"،
// ستؤدي عملية الحفظ إلى تحويل المستند إلى صورة أحادية اللون.
// إذا قمنا بتعيين خاصية "ImageColorMode" إلى "None"، فسوف تطبق عملية الحفظ الطريقة الافتراضية
// والحفاظ على كافة ألوان المستند في الصورة الناتجة.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.ImageColorMode = imageColorMode;

doc.Save(ArtifactsDir + "ImageSaveOptions.ColorMode.png", imageSaveOptions);
```

### أنظر أيضا

* enum [ImageColorMode](../../imagecolormode/)
* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
