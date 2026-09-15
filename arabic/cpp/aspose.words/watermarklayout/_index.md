---
title: "Aspose::Words::WatermarkLayout تعداد"
linktitle: "WatermarkLayout"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::WatermarkLayout تعداد. يحدد تخطيط العلامة المائية بالنسبة إلى مركز العلامة المائية في C++."
type: docs
weight: 130000
url: /ar/cpp/aspose.words/watermarklayout/
---
## WatermarkLayout enum


يعرف تخطيط العلامة المائية بالنسبة إلى مركز العلامة المائية.

```cpp
enum class WatermarkLayout
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| أفقي | 0 | تخطيط العلامة المائية الأفقي. يتطابق مع 0 درجة من الدوران. |
| Diagonal | 315 | تخطيط العلامة المائية القطري. يتطابق مع 315 درجة من الدوران. |


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
