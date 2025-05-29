---
title: GraphicsQualityOptions Class
linktitle: GraphicsQualityOptions
articleTitle: GraphicsQualityOptions
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Saving.GraphicsQualityOptions لتحسين جودة رسومات المستندات باستخدام خيارات قابلة للتخصيص للحصول على إخراج فائق.
type: docs
weight: 5790
url: /ar/net/aspose.words.saving/graphicsqualityoptions/
---
## GraphicsQualityOptions class

يسمح بتحديد إضافيGraphics خيارات الجودة.

لمعرفة المزيد، قم بزيارة[حفظ مستند](https://docs.aspose.com/words/net/save-a-document/) مقالة توثيقية.

```csharp
public class GraphicsQualityOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [GraphicsQualityOptions](graphicsqualityoptions/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [CompositingMode](../../aspose.words.saving/graphicsqualityoptions/compositingmode/) { get; set; } | يحصل على قيمة تحدد كيفية رسم الصور المركبة لهذه الرسومات أو يعينها. |
| [CompositingQuality](../../aspose.words.saving/graphicsqualityoptions/compositingquality/) { get; set; } | يحصل على جودة عرض الصور المركبة المرسومة على هذه الرسومات أو يعينها. |
| [InterpolationMode](../../aspose.words.saving/graphicsqualityoptions/interpolationmode/) { get; set; } | يحصل على وضع الاستيفاء المرتبط بهذه الرسومات أو يعينه. |
| [SmoothingMode](../../aspose.words.saving/graphicsqualityoptions/smoothingmode/) { get; set; } | يحصل على جودة العرض لهذه الرسومات أو يعينها. |
| [StringFormat](../../aspose.words.saving/graphicsqualityoptions/stringformat/) { get; set; } | يحصل على معلومات تخطيط النص (مثل المحاذاة والتوجيه وعلامات التبويب) أو يعينها، وعمليات معالجة العرض (مثل إدراج النقاط الثلاث واستبدال الأرقام الوطنية) وميزات OpenType. |
| [TextRenderingHint](../../aspose.words.saving/graphicsqualityoptions/textrenderinghint/) { get; set; } | يحصل على وضع العرض للنص المرتبط بهذه الرسومات أو يعينه. |
| [UseTileFlipMode](../../aspose.words.saving/graphicsqualityoptions/usetileflipmode/) { get; set; } | يحصل على علم يشير إلى ما إذا كان WrapMode هو TileFlipXY أو يعينه. |

## أمثلة

يوضح كيفية تعيين خيارات جودة العرض أثناء تحويل المستندات إلى تنسيقات الصور.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

GraphicsQualityOptions qualityOptions = new GraphicsQualityOptions
{
    SmoothingMode = SmoothingMode.AntiAlias,
    TextRenderingHint = TextRenderingHint.ClearTypeGridFit,
    CompositingMode = CompositingMode.SourceOver,
    CompositingQuality = CompositingQuality.HighQuality,
    InterpolationMode = InterpolationMode.High,
    StringFormat = StringFormat.GenericTypographic
};

ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg);
saveOptions.GraphicsQualityOptions = qualityOptions;

doc.Save(ArtifactsDir + "ImageSaveOptions.GraphicsQuality.jpg", saveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
