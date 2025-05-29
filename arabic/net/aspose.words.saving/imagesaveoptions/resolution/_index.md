---
title: ImageSaveOptions.Resolution
linktitle: Resolution
articleTitle: Resolution
second_title: Aspose.Words لـ .NET
description: حسّن صورك مع خيارات حفظ الصور! تحكّم بدقة العرض الأفقية والرأسية بدقة DPI لجودة ووضوح مذهلين. حسّن صورك اليوم!
type: docs
weight: 130
url: /ar/net/aspose.words.saving/imagesaveoptions/resolution/
---
## ImageSaveOptions.Resolution property

يحدد الدقة الأفقية والرأسية للصور المولدة، بنقاط لكل بوصة.

```csharp
public float Resolution { set; }
```

## ملاحظات

لا يكون لهذه الخاصية تأثير إلا عند الحفظ بتنسيقات الصور النقطية.

## أمثلة

يوضح كيفية تحديد الدقة أثناء عرض مستند بتنسيق PNG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// قم بإنشاء كائن "ImageSaveOptions" الذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل الطريقة التي تقوم بها هذه الطريقة بتحويل المستند إلى صورة.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

// اضبط خاصية "الدقة" على "72" لعرض المستند بدقة 72 نقطة في البوصة.
options.Resolution = 72;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png", options);

// اضبط خاصية "الدقة" على "300" لعرض المستند بدقة 300 نقطة في البوصة.
options.Resolution = 300;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png", options);
```

### أنظر أيضا

* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
