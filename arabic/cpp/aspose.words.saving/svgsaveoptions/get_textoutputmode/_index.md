---
title: "Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode طريقة"
linktitle: "get_TextOutputMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode طريقة. يحصل على أو يحدد قيمة تحدد كيفية عرض النص في SVG في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words.saving/svgsaveoptions/get_textoutputmode/
---
## SvgSaveOptions::get_TextOutputMode method


يحصل أو يعيّن قيمة تحدد كيفية عرض النص في SVG.

```cpp
Aspose::Words::Saving::SvgTextOutputMode Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode() const
```

## ملاحظات


استخدم هذه الخاصية للحصول على أو تعيين وضعية كيفية عرض النص داخل المستند عند الحفظ بتنسيق SVG.

القيمة الافتراضية هي [UseTargetMachineFonts](../../svgtextoutputmode/).

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

* Enum [SvgTextOutputMode](../../svgtextoutputmode/)
* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
