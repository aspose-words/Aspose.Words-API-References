---
title: SaveOptions.UseAntiAliasing
linktitle: UseAntiAliasing
articleTitle: UseAntiAliasing
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية "حفظ الخيارات" و"استخدام خاصية منع التعرجات" لتحسين جودة العرض. تحكّم في خاصية منع التعرجات للحصول على صور أكثر سلاسة وأداء أفضل.
type: docs
weight: 200
url: /ar/net/aspose.words.saving/saveoptions/useantialiasing/
---
## SaveOptions.UseAntiAliasing property

يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم استخدام التنعيم للرسم أم لا.

```csharp
public bool UseAntiAliasing { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع` . عندما يتم تعيين هذه القيمة على`حقيقي` يتم استخدام التنعيم في العرض.

يتم استخدام هذه الخاصية عند تصدير المستند إلى التنسيقات التالية: Tiff ،Png ،Bmp ، Jpeg ،Emf . عند تصدير المستند إلى Html ،Mhtml ، Epub ،Azw3 أوMobiيستخدم هذا الخيار للصور النقطية.

## أمثلة

يوضح كيفية تحسين جودة المستند المقدم باستخدام SaveOptions.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 60;
builder.Writeln("Some text.");

SaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
doc.Save(ArtifactsDir + "Document.ImageSaveOptions.Default.jpg", options);

options.UseAntiAliasing = true;
options.UseHighQualityRendering = true;

doc.Save(ArtifactsDir + "Document.ImageSaveOptions.HighQuality.jpg", options);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
