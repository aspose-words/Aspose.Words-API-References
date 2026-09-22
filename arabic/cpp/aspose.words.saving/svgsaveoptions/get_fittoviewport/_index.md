---
title: "طريقة Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort"
linktitle: "get_FitToViewPort"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort. تحدد ما إذا كان يجب أن يملأ SVG الناتج مساحة العرض المتاحة (نافذة المتصفح أو الحاوية). عندما تُضبط على true يتم تعيين عرض وارتفاع SVG الناتج إلى 100٪. القيمة الافتراضية هي false في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.saving/svgsaveoptions/get_fittoviewport/
---
## SvgSaveOptions::get_FitToViewPort method


يحدد ما إذا كان SVG الناتج يجب أن يملأ مساحة العرض المتاحة (نافذة المتصفح أو الحاوية). عند تعيينه إلى **true** يتم ضبط عرض وارتفاع SVG الناتج إلى 100٪. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort() const
```


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

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
