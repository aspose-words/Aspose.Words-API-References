---
title: SvgSaveOptions.TextOutputMode
linktitle: TextOutputMode
articleTitle: TextOutputMode
second_title: Aspose.Words لـ .NET
description: SvgSaveOptions TextOutputMode ملكية. الحصول على أو تعيين قيمة تحدد كيفية عرض النص في SVG في C#.
type: docs
weight: 90
url: /ar/net/aspose.words.saving/svgsaveoptions/textoutputmode/
---
## SvgSaveOptions.TextOutputMode property

الحصول على أو تعيين قيمة تحدد كيفية عرض النص في SVG.

```csharp
public SvgTextOutputMode TextOutputMode { get; set; }
```

## ملاحظات

استخدم هذه الخاصية للحصول على أو تعيين الوضع الذي يجب أن يتم به عرض النص داخل المستند عند الحفظ بتنسيق SVG.

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
