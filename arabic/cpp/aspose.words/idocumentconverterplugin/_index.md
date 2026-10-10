---
title: "واجهة Aspose::Words::IDocumentConverterPlugin"
linktitle: "IDocumentConverterPlugin"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "واجهة Aspose::Words::IDocumentConverterPlugin. تُعرّف واجهة لمكوّن تحويل خارجي في C++."
type: docs
weight: 76250
url: /ar/cpp/aspose.words/idocumentconverterplugin/
---
## IDocumentConverterPlugin interface


يحدد واجهة لمكوّن تحويل خارجي.

```cpp
class IDocumentConverterPlugin : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| virtual [Convert](./convert/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | يحوّل المستند باستخدام تدفقات الإدخال والإخراج المحددة وخيارات الحفظ. |
| virtual [ConvertToImages](./converttoimages/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | يحوّل الصفحات من المستند من تدفق الإدخال إلى مصفوفة من الصور. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
