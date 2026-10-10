---
title: "Aspose::Words::WatermarkType enum"
linktitle: "WatermarkType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::WatermarkType enum. يحدد نوع العلامة المائية في C++."
type: docs
weight: 131000
url: /ar/cpp/aspose.words/watermarktype/
---
## WatermarkType enum


يحدد نوع العلامة المائية.

```cpp
enum class WatermarkType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Text | 0 | يشير إلى أن النص سيُستخدم كعلامة مائية. مثل هذه العلامة المائية تتطابق مع كائن WordArt. |
| Image | 1 | يشير إلى أن الصورة ستُستخدم كعلامة مائية. مثل هذه العلامة المائية تتطابق مع شكل يحتوي على صورة. |
| None | 2 | يشير إلى أن العلامة المائية غير محددة. |


## أمثلة



يُظهر كيفية إنشاء علامة مائية نصية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// أضف علامة مائية نصية عادية.
doc->get_Watermark()->SetText(u"Aspose Watermark");

// إذا رغبنا في تعديل تنسيق النص باستخدامه كعلامة مائية،
// يمكننا القيام بذلك بتمرير كائن TextWatermarkOptions عند إنشاء العلامة المائية.
auto textWatermarkOptions = System::MakeObject<Aspose::Words::TextWatermarkOptions>();
textWatermarkOptions->set_FontFamily(u"Arial");
textWatermarkOptions->set_FontSize(36.0f);
textWatermarkOptions->set_Color(System::Drawing::Color::get_Black());
textWatermarkOptions->set_Layout(Aspose::Words::WatermarkLayout::Diagonal);
textWatermarkOptions->set_IsSemitrasparent(false);

doc->get_Watermark()->SetText(u"Aspose Watermark", textWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.TextWatermark.docx");

// يمكننا إزالة العلامة المائية من مستند مثل هذا.
if (doc->get_Watermark()->get_Type() == Aspose::Words::WatermarkType::Text)
{
    doc->get_Watermark()->Remove();
}
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
