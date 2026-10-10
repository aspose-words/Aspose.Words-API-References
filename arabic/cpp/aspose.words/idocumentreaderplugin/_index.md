---
title: "واجهة Aspose::Words::IDocumentReaderPlugin"
linktitle: "IDocumentReaderPlugin"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "واجهة Aspose::Words::IDocumentReaderPlugin. تُعرّف واجهة للمكوّنات الإضافية الخارجية للقراءة التي يمكنها قراءة ملف إلى مستند في C++."
type: docs
weight: 77000
url: /ar/cpp/aspose.words/idocumentreaderplugin/
---
## IDocumentReaderPlugin interface


يحدد واجهة لمكوّنات قراءة خارجية يمكنها قراءة ملف إلى مستند.

```cpp
class IDocumentReaderPlugin : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Read](./read/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<Aspose::Words::Document\>) | يقرأ البيانات من التدفق المحدد إلى كائن [Document](../document/) . |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
