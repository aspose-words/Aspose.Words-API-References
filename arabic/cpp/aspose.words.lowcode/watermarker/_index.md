---
title: "Aspose::Words::LowCode::Watermarker class"
linktitle: "مُضيف العلامة المائية"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::LowCode::Watermarker فئة. توفر طرقًا تهدف إلى إدراج العلامات المائية في المستندات باستخدام C++."
type: docs
weight: 1750
url: /ar/cpp/aspose.words.lowcode/watermarker/
---
## Watermarker class


يوفر طرقًا تهدف إلى إدراج العلامات المائية في المستندات.

```cpp
class Watermarker : public Aspose::Words::LowCode::Processor
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::WatermarkerContext\>\&) | ينشئ مثيلًا جديدًا لمعالج العلامة المائية. |
| [Execute](../processor/execute/)() | تنفيذ إجراء المعالج. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | تنفيذ إجراء المعالج مع السماح بإلغاء مهمة معالجة المستند باستخدام رمز الإلغاء المحدد. |
| [From](../processor/from/)(const System::String\&) | يحدد المستند الإدخالي للمعالجة. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | يحدد المستند الإدخالي للمعالجة. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | يحدد المستند الإدخالي للمعالجة. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | يحدد المستند الإدخالي للمعالجة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::String\&) | يضيف علامة مائية صورة إلى المستند. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | يضيف علامة مائية صورة إلى المستند مع خيارات. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) | يضيف علامة مائية صورة إلى المستند مع خيارات وتنسيق حفظ محدد. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | يضيف علامة مائية صورة إلى المستند مع خيارات وتنسيق حفظ محدد. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) | يضيف علامة مائية صورة إلى المستند مع خيارات وتنسيق حفظ محدد. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | يضيف علامة مائية صورة إلى المستند مع خيارات وتنسيق حفظ محدد. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&) | يضيف علامة مائية صورة إلى المستند من التدفقات مع خيارات. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | يضيف علامة مائية صورة إلى المستند من التدفقات مع خيارات. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&) | يضيف علامة مائية صورة إلى المستند من التدفقات مع خيارات. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | يضيف علامة مائية صورة إلى المستند من التدفقات مع خيارات. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&) | يضيف علامة مائية صورة إلى المستند من التدفقات مع خيارات. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | يضيف علامة مائية صورة إلى المستند من التدفقات مع خيارات. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | يضيف علامة مائية صورة إلى المستند من التدفقات مع خيارات. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | يضيف علامة مائية صورة إلى المستند من التدفقات مع خيارات. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::String\&) | يضيف علامة مائية نصية إلى المستند. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | يضيف علامة مائية نصية إلى المستند مع خيارات. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) | يضيف علامة مائية نصية إلى المستند مع خيارات وتنسيق حفظ محدد. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | يضيف علامة مائية نصية إلى المستند مع خيارات وتنسيق حفظ محدد. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) | يضيف علامة مائية نصية إلى المستند مع خيارات وتنسيق حفظ محدد. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | يضيف علامة مائية نصية إلى المستند مع خيارات وتنسيق حفظ محدد. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&) | يضيف علامة مائية نصية إلى المستند من التدفقات مع خيارات. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | يضيف علامة مائية نصية إلى المستند من التدفقات مع خيارات. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) | يضيف علامة مائية نصية إلى المستند من التدفقات مع خيارات. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | يضيف علامة مائية نصية إلى المستند من التدفقات مع خيارات. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&) | يضيف علامة مائية نصية إلى المستند مع خيارات. يُولِّد المخرجات كصور. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | يضيف علامة مائية نصية إلى المستند مع خيارات. يُولِّد المخرجات كصور. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&) | يضيف علامة مائية نصية إلى المستند مع خيارات. يُولِّد المخرجات كصور. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | يضيف علامة مائية نصية إلى المستند مع خيارات. يُولِّد المخرجات كصور. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::ArrayPtr\<uint8_t\>\&) | يضيف علامة مائية صورة إلى المستند مع خيارات. يُولِّد المخرجات كصور. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | يضيف علامة مائية صورة إلى المستند مع خيارات. يُولِّد المخرجات كصور. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | يضيف علامة مائية صورة إلى المستند مع خيارات. يُولِّد المخرجات كصور. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | يضيف علامة مائية صورة إلى المستند مع خيارات. يُولِّد المخرجات كصور. |
| [To](../processor/to/)(const System::String\&) | يحدد ملف الإخراج للمعالج. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | يحدد ملف الإخراج للمعالج. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | يحدد ملف الإخراج للمعالج. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يحدد تدفق الإخراج للمعالج. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | يحدد تدفق الإخراج للمعالج. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## انظر أيضًا

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
