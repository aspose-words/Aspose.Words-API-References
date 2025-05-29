---
title: SaveOptions.UseHighQualityRendering
linktitle: UseHighQualityRendering
articleTitle: UseHighQualityRendering
second_title: Aspose.Words لـ .NET
description: حسّن خيارات الحفظ باستخدام خاصية UseHighQualityRendering للحصول على نتائج فائقة الجودة. تحكم في سرعة وجودة العرض للحصول على نتائج مثالية.
type: docs
weight: 210
url: /ar/net/aspose.words.saving/saveoptions/usehighqualityrendering/
---
## SaveOptions.UseHighQualityRendering property

يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم استخدام خوارزميات عرض عالية الجودة (أي بطيئة) أم لا.

```csharp
public bool UseHighQualityRendering { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع` .

يتم استخدام هذه الخاصية عند تصدير المستند إلى تنسيقات الصور: Tiff ،Png ،Bmp ، Jpeg ،Emf.

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
