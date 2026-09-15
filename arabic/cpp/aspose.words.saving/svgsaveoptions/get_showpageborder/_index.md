---
title: "طريقة Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder"
linktitle: "get_ShowPageBorder"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder. تتحكم فيما إذا كان يتم إضافة حد إلى مخطط الصفحة. القيمة الافتراضية هي true في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.saving/svgsaveoptions/get_showpageborder/
---
## SvgSaveOptions::get_ShowPageBorder method


يتحكم فيما إذا كان يتم إضافة حد إلى مخطط الصفحة. القيمة الافتراضية هي **true**.

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder() const
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
