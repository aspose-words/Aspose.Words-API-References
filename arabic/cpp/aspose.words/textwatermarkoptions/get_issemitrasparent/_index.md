---
title: "Aspose::Words::TextWatermarkOptions::get_IsSemitrasparent طريقة"
linktitle: "get_IsSemitrasparent"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::TextWatermarkOptions::get_IsSemitrasparent طريقة. يحصل أو يضبط قيمة منطقية مسؤولة عن شفافية العلامة المائية. القيمة الافتراضية هي true في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words/textwatermarkoptions/get_issemitrasparent/
---
## TextWatermarkOptions::get_IsSemitrasparent method


يحصل أو يعيّن قيمة منطقية مسؤولة عن شفافية العلامة المائية. القيمة الافتراضية هي **true**.

```cpp
bool Aspose::Words::TextWatermarkOptions::get_IsSemitrasparent() const
```


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

* Class [TextWatermarkOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
