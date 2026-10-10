---
title: "Aspose::Words::Saving::SvgTextOutputMode enum"
linktitle: "SvgTextOutputMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::SvgTextOutputMode enum. يسمح بتحديد كيفية عرض النص داخل المستند عند الحفظ بتنسيق SVG في C++."
type: docs
weight: 83000
url: /ar/cpp/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enum


يسمح بتحديد كيفية عرض النص داخل المستند عند حفظه بتنسيق SVG.

```cpp
enum class SvgTextOutputMode
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| UseSvgFonts | 0 | يتم استخدام خطوط SVG لعرض النص. ملاحظة، ليس كل المتصفحات تدعم خطوط SVG. |
| UseTargetMachineFonts | 1 | [Fonts](../../aspose.words.fonts/) المثبتة على الجهاز الهدف تُستخدم لعرض النص. ملاحظة، إذا كانت بعض الخطوط المستخدمة في المستند غير متوفرة على الجهاز الهدف، قد يظهر المستند بشكل مختلف. |
| UsePlacedGlyphs | 2 | يتم عرض النص باستخدام المنحنيات. ملاحظة، لن يعمل تحديد النص إذا استخدمت هذا الخيار. |


## أمثلة



يعرض كيفية محاكاة خصائص الصور عند تحويل مستند .docx إلى .svg.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// قم بتكوين كائن SvgSaveOptions للحفظ بدون حدود صفحات أو نص قابل للتحديد.
auto options = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
options->set_FitToViewPort(true);
options->set_ShowPageBorder(false);
options->set_TextOutputMode(Aspose::Words::Saving::SvgTextOutputMode::UsePlacedGlyphs);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.SaveLikeImage.svg", options);
```

## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
