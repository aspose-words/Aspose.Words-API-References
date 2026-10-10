---
title: "فئة Aspose::Words::Watermark"
linktitle: "علامة مائية"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Watermark. تمثل فئة للعمل مع العلامة المائية للمستند. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 76000
url: /ar/cpp/aspose.words/watermark/
---
## Watermark class


يمثل فئة للعمل مع علامة مائية للمستند. لمعرفة المزيد، زر مقالة الوثائق [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/).

```cpp
class Watermark : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Type](./get_type/)() | يحصل على نوع العلامة المائية. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | يزيل العلامة المائية. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | يضيف علامة مائية صورة إلى المستند. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | يضيف علامة مائية صورة إلى المستند. |
| [SetImage](./setimage/)(const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | يضيف علامة مائية صورة إلى المستند. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | يضيف علامة مائية صورة إلى المستند. |
| [SetText](./settext/)(const System::String\&) | يضيف علامة مائية نصية إلى المستند. |
| [SetText](./settext/)(const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | يضيف علامة مائية نصية إلى المستند. |
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
