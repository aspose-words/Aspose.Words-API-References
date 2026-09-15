---
title: "Aspose::Words::TextWatermarkOptions::get_FontFamily طريقة"
linktitle: "get_FontFamily"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::TextWatermarkOptions::get_FontFamily طريقة. يحصل أو يضبط اسم عائلة الخط. القيمة الافتراضية هي \"Calibri\" في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/textwatermarkoptions/get_fontfamily/
---
## TextWatermarkOptions::get_FontFamily method


يحصل أو يعيّن اسم عائلة الخط. القيمة الافتراضية هي "Calibri".

```cpp
System::String Aspose::Words::TextWatermarkOptions::get_FontFamily() const
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
