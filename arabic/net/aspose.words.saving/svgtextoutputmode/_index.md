---
title: SvgTextOutputMode Enum
linktitle: SvgTextOutputMode
articleTitle: SvgTextOutputMode
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Saving.SvgTextOutputMode enum لتخصيص عرض النص بتنسيق SVG، مما يعزز عرض المستند وجاذبيته البصرية.
type: docs
weight: 6410
url: /ar/net/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enumeration

يسمح بتحديد كيفية عرض النص داخل المستند عند الحفظ بتنسيق SVG.

```csharp
public enum SvgTextOutputMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| UseSvgFonts | `0` | تُستخدم خطوط SVG لعرض النصوص. ملاحظة: لا تدعم جميع المتصفحات خطوط SVG. |
| UseTargetMachineFonts | `1` | يتم استخدام الخطوط المثبتة على الجهاز المستهدف لعرض النص. ملاحظة، إذا لم تكن بعض الخطوط المستخدمة في المستند متوفرة على الجهاز المستهدف، فقد يبدو المستند مختلفًا. |
| UsePlacedGlyphs | `2` | يتم عرض النص باستخدام المنحنيات. ملاحظة: لن يعمل تحديد النص باستخدام هذا الخيار. |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
