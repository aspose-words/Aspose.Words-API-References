---
title: SvgSaveOptions.TextOutputMode
linktitle: TextOutputMode
articleTitle: TextOutputMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية TextOutputMode في SvgSaveOptions، التي تتحكم في عرض النص في SVG لتحسين جودة الصورة والتخصيص. حسّن رسوماتك اليوم!
type: docs
weight: 120
url: /ar/net/aspose.words.saving/svgsaveoptions/textoutputmode/
---
## SvgSaveOptions.TextOutputMode property

يحصل على قيمة تحدد كيفية عرض النص في SVG أو يعينها.

```csharp
public SvgTextOutputMode TextOutputMode { get; set; }
```

## ملاحظات

استخدم هذه الخاصية للحصول على أو تعيين وضع كيفية تقديم النص داخل المستند عند الحفظ بتنسيق SVG.

القيمة الافتراضية هيUseTargetMachineFonts.

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

* enum [SvgTextOutputMode](../../svgtextoutputmode/)
* class [SvgSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
