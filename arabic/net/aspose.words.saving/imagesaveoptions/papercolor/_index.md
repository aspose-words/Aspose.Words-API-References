---
title: ImageSaveOptions.PaperColor
linktitle: PaperColor
articleTitle: PaperColor
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PaperColor في ImageSaveOptions لتخصيص ألوان الخلفية للصور التي تم إنشاؤها بسهولة، مما يعزز الجاذبية البصرية والتفرد.
type: docs
weight: 110
url: /ar/net/aspose.words.saving/imagesaveoptions/papercolor/
---
## ImageSaveOptions.PaperColor property

يحصل على لون الخلفية (الورق) للصور المولدة أو يعينه.

القيمة الافتراضية هيWhite.

```csharp
public Color PaperColor { get; set; }
```

## ملاحظات

عند عرض صفحات مستند يحدد لون الخلفية الخاص به، فإن لون خلفية المستند سيحل محل اللون المحدد بواسطة هذه الخاصية.

## أمثلة

يقوم بتحويل صفحة من مستند Word إلى صورة ذات خلفية شفافة أو ملونة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// قم بإنشاء كائن "ImageSaveOptions" الذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل الطريقة التي تقوم بها هذه الطريقة بتحويل المستند إلى صورة.
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);
// اضبط خاصية "PaperColor" على لون شفاف لتطبيق لون شفاف
// خلفية المستند أثناء عرضه على صورة.
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// اضبط خاصية "PaperColor" على لون معتم لتطبيق هذا اللون
// كخلفية للمستند كما نقوم بتحويله إلى صورة.
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

### أنظر أيضا

* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
