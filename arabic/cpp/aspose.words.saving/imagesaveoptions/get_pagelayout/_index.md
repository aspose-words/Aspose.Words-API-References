---
title: "طريقة Aspose::Words::Saving::ImageSaveOptions::get_PageLayout"
linktitle: "get_PageLayout"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::ImageSaveOptions::get_PageLayout. يحصل على أو يضبط التخطيط المستخدم عند تحويل صفحات متعددة إلى مخرج واحد في C++."
type: docs
weight: 9500
url: /ar/cpp/aspose.words.saving/imagesaveoptions/get_pagelayout/
---
## ImageSaveOptions::get_PageLayout method


يحصل أو يضبط التخطيط المستخدم عند عرض صفحات متعددة في مخرج واحد.

```cpp
System::SharedPtr<Aspose::Words::Saving::MultiPageLayout> Aspose::Words::Saving::ImageSaveOptions::get_PageLayout() const
```

## ملاحظات


استخدم إحدى طرق المصنع لـ [MultiPageLayout](../../multipagelayout/) لتكوين هذه الخاصية.

بالنسبة إلى [Tiff](../../../aspose.words/saveformat/) القيمة الافتراضية هي [TiffFrames](../../multipagelayout/tiffframes/). بالنسبة إلى الصيغ الأخرى القيمة الافتراضية هي [SinglePage](../../multipagelayout/singlepage/).

هذه الخاصية لها تأثير فقط عند الحفظ إلى الصيغ التالية: [Jpeg](../../../aspose.words/saveformat/), [Gif](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Tiff](../../../aspose.words/saveformat/), [WebP](../)

## أمثلة



يظهر كيفية حفظ المستند كصورة JPG مع إعدادات تخطيط متعدد الصفحات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// إعداد تخطيط شبكة مع:
// - 3 أعمدة لكل صف.
// - 10 نقاط مسافة بين الصفحات (أفقية وعمودية).
options->set_PageLayout(Aspose::Words::Saving::MultiPageLayout::Grid(3, 10.0f, 10.0f));

// تخطيطات بديلة:
// options.PageLayout = MultiPageLayout.Horizontal(10);
// options.PageLayout = MultiPageLayout.Vertical(10);

// تخصيص الخلفية والحد.
options->get_PageLayout()->set_BackColor(System::Drawing::Color::get_LightGray());
options->get_PageLayout()->set_BorderColor(System::Drawing::Color::get_Blue());
options->get_PageLayout()->set_BorderWidth(2.0f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.GridLayout.jpg", options);
```

## انظر أيضًا

* Class [MultiPageLayout](../../multipagelayout/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
