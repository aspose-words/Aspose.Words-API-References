---
title: "Aspose::Words::TextWatermarkOptions فئة"
linktitle: "TextWatermarkOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::TextWatermarkOptions. تحتوي على خيارات يمكن تحديدها عند إضافة علامة مائية بنص. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 72000
url: /ar/cpp/aspose.words/textwatermarkoptions/
---
## TextWatermarkOptions class


يحتوي على خيارات يمكن تحديدها عند إضافة علامة مائية بنص. لمعرفة المزيد، زر مقالة الوثائق [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/).

```cpp
class TextWatermarkOptions : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Color](./get_color/)() const | يحصل أو يعيّن لون الخط. القيمة الافتراضية هي **Silver**. |
| [get_FontFamily](./get_fontfamily/)() const | يحصل أو يعيّن اسم عائلة الخط. القيمة الافتراضية هي "Calibri". |
| [get_FontSize](./get_fontsize/)() const | يحصل أو يعيّن حجم الخط. القيمة الافتراضية هي 0 - تلقائي. |
| [get_IsSemitrasparent](./get_issemitrasparent/)() const | يحصل أو يعيّن قيمة منطقية مسؤولة عن شفافية العلامة المائية. القيمة الافتراضية هي **true**. |
| [get_Layout](./get_layout/)() const | يحصل أو يعيّن تخطيط العلامة المائية. القيمة الافتراضية هي [Diagonal](../watermarklayout/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | مُعيّن لـ [Aspose::Words::TextWatermarkOptions::get_Color](./get_color/). |
| [set_FontFamily](./set_fontfamily/)(const System::String\&) | مُعيّن لـ [Aspose::Words::TextWatermarkOptions::get_FontFamily](./get_fontfamily/). |
| [set_FontSize](./set_fontsize/)(float) | مُعيّن لـ [Aspose::Words::TextWatermarkOptions::get_FontSize](./get_fontsize/). |
| [set_IsSemitrasparent](./set_issemitrasparent/)(bool) | مُعيّن لـ [Aspose::Words::TextWatermarkOptions::get_IsSemitrasparent](./get_issemitrasparent/). |
| [set_Layout](./set_layout/)(Aspose::Words::WatermarkLayout) | مُعيّن لـ [Aspose::Words::TextWatermarkOptions::get_Layout](./get_layout/). |
| [TextWatermarkOptions](./textwatermarkoptions/)() |  |
| static [Type](./type/)() |  |

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
