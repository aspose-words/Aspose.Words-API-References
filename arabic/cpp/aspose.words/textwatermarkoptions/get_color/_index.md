---
title: "Aspose::Words::TextWatermarkOptions::get_Color طريقة"
linktitle: "get_Color"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::TextWatermarkOptions::get_Color طريقة. يحصل على أو يضبط لون الخط. القيمة الافتراضية هي Silver في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/textwatermarkoptions/get_color/
---
## TextWatermarkOptions::get_Color method


يحصل أو يعيّن لون الخط. القيمة الافتراضية هي **Silver**.

```cpp
System::Drawing::Color Aspose::Words::TextWatermarkOptions::get_Color() const
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
