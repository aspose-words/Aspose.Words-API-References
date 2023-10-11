---
title: SaveOptions.UseAntiAliasing
second_title: Aspose.Words لمراجع .NET API
description: SaveOptions ملكية. الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم استخدام الصقل للعرض أم لا.
type: docs
weight: 190
url: /ar/net/aspose.words.saving/saveoptions/useantialiasing/
---
## SaveOptions.UseAntiAliasing property

الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم استخدام الصقل للعرض أم لا.

```csharp
public bool UseAntiAliasing { get; set; }
```

### ملاحظات

القيمة الافتراضية هي`خطأ شنيع` . عندما يتم ضبط هذه القيمة على`حقيقي` يتم استخدام الصقل للعرض.

يتم استخدام هذه الخاصية عند تصدير المستند إلى التنسيقات التالية: Tiff ,Png ,BmpJpeg ,Emf . عندما يتم تصدير المستند إلى the Html ,MhtmlEpub ,Azw3 أوMobi التنسيقات يستخدم هذا الخيار للصور النقطية.

### أمثلة

يوضح كيفية تحسين جودة المستند المعروض باستخدام SaveOptions.

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
* مساحة الاسم [Aspose.Words.Saving](../../saveoptions/)
* المجسم [Aspose.Words](../../../)


