---
title: SvgTextOutputMode Enum
linktitle: SvgTextOutputMode
articleTitle: SvgTextOutputMode
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.SvgTextOutputMode تعداد. يسمح بتحديد كيفية عرض النص داخل المستند عند الحفظ بتنسيق SVG في C#.
type: docs
weight: 5610
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
| UseSvgFonts | `0` | يتم استخدام خطوط SVG لعرض النص. لاحظ أنه ليست كل المتصفحات تدعم خطوط SVG. |
| UseTargetMachineFonts | `1` | يتم استخدام الخطوط المثبتة على الجهاز الهدف لعرض النص. ملاحظة، إذا كانت بعض الخطوط المستخدمة في المستند غير متوفرة على الجهاز المستهدف، فقد يبدو المستند بشكل مختلف. |
| UsePlacedGlyphs | `2` | يتم عرض النص باستخدام المنحنيات. لاحظ أن تحديد النص لن يعمل إذا استخدمت هذا الخيار. |

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
