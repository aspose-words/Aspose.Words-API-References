---
title: "طريقة Aspose::Words::DocumentBase::get_Document"
linktitle: "get_Document"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBase::get_Document. تُعيد هذه الحالة بلغة C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/documentbase/get_document/
---
## DocumentBase::get_Document method


يحصل على هذا الكائن.

```cpp
System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::DocumentBase::get_Document() const override
```


## أمثلة



يعرض كيفية إنشاء مستند بسيط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// كائنات Document الجديدة تأتي افتراضيًا مع الحد الأدنى من العقد
// المطلوبة لبدء إضافة محتوى مثل النص والأشكال: Section، Body، و Paragraph.
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## انظر أيضًا

* Class [DocumentBase](../)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
