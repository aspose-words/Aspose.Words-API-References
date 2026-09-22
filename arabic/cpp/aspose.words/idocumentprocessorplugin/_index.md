---
title: "واجهة Aspose::Words::IDocumentProcessorPlugin"
linktitle: "IDocumentProcessorPlugin"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "واجهة Aspose::Words::IDocumentProcessorPlugin. تحدد واجهة لمكوّن إضافي لمعالجة المستندات الخارجية في C++."
type: docs
weight: 76750
url: /ar/cpp/aspose.words/idocumentprocessorplugin/
---
## IDocumentProcessorPlugin interface


يحدد واجهة لمكوّن معالجة مستندات خارجي.

```cpp
class IDocumentProcessorPlugin : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| virtual [Append](./append/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>) | أضف المستند بتحميله باستخدام خيارات التحميل المحددة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Load](./load/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>) | حمّل المستند باستخدام خيارات التحميل المحددة. |
| virtual [Save](./save/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | احفظ المستند الذي تم تحميله بواسطة طريقة [Load()](./load/) إلى تدفق الإخراج باستخدام خيارات الحفظ المحددة. |
| virtual [SetImageWatermark](./setimagewatermark/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>) | يضيف علامة مائية صورة على كل صفحة من المستند الذي تم تحميله بواسطة طريقة [Load()](./load/). |
| virtual [SetTextWatermark](./settextwatermark/)(System::String, System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>) | يضيف علامة مائية نصية على كل صفحة من المستند الذي تم تحميله بواسطة طريقة [Load()](./load/). |
| virtual [ToDocument](./todocument/)() | يحلل المستند الذي تم تحميله بواسطة طريقة [Load()](./load/) إلى كائن [Document](../document/). |
| virtual [ToPages](./topages/)(System::SharedPtr\<Aspose::Words::Saving::FixedPageSaveOptions\>) | يحفظ كل صفحة من المستند الذي تم تحميله بواسطة طريقة [Load()](./load/) باستخدام خيارات حفظ الصفحات الثابتة المحددة. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
