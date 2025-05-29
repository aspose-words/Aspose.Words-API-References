---
title: SvgSaveOptions.FitToViewPort
linktitle: FitToViewPort
articleTitle: FitToViewPort
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية SvgSaveOptions FitToViewPort على تحسين مخرجات SVG الخاصة بك لملء أي نافذة أو حاوية متصفح بشكل مثالي للحصول على صور مذهلة.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/svgsaveoptions/fittoviewport/
---
## SvgSaveOptions.FitToViewPort property

يحدد ما إذا كان يجب أن يملأ ملف SVG الناتج منطقة عرض النافذة أو الحاوية المتاحة. عند ضبطه على`حقيقي`تم ضبط عرض وارتفاع SVG الناتج على 100%.

القيمة الافتراضية هي`خطأ شنيع`.

```csharp
public bool FitToViewPort { get; set; }
```

## أمثلة

يوضح كيفية محاكاة خصائص الصور عند تحويل مستند .docx إلى .svg.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// قم بتكوين كائن SvgSaveOptions للحفظ بدون حدود للصفحة أو نص قابل للتحديد.
SvgSaveOptions options = new SvgSaveOptions
{
    FitToViewPort = true,
    ShowPageBorder = false,
    TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs
};

doc.Save(ArtifactsDir + "SvgSaveOptions.SaveLikeImage.svg", options);
```

### أنظر أيضا

* class [SvgSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
