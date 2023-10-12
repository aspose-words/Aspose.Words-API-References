---
title: SvgSaveOptions.FitToViewPort
second_title: Aspose.Words لمراجع .NET API
description: SvgSaveOptions ملكية. يحدد ما إذا كان ينبغي لمخرجات SVG أن تملأ منطقة إطار العرض المتاحة نافذة المتصفح أو الحاوية. عند التعيين علىحقيقي تم ضبط عرض وارتفاع مخرجات SVG على 100.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/svgsaveoptions/fittoviewport/
---
## SvgSaveOptions.FitToViewPort property

يحدد ما إذا كان ينبغي لمخرجات SVG أن تملأ منطقة إطار العرض المتاحة (نافذة المتصفح أو الحاوية). عند التعيين على`حقيقي` تم ضبط عرض وارتفاع مخرجات SVG على 100%.

القيمة الافتراضية هي`خطأ شنيع`.

```csharp
public bool FitToViewPort { get; set; }
```

### أمثلة

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
* مساحة الاسم [Aspose.Words.Saving](../../svgsaveoptions/)
* المجسم [Aspose.Words](../../../)


