---
title: "طريقة Aspose::Words::Document::get_OriginalLoadFormat"
linktitle: "get_OriginalLoadFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::get_OriginalLoadFormat. يحصل على تنسيق المستند الأصلي الذي تم تحميله إلى هذا الكائن في C++."
type: docs
weight: 41000
url: /ar/cpp/aspose.words/document/get_originalloadformat/
---
## Document::get_OriginalLoadFormat method


يحصل على تنسيق المستند الأصلي الذي تم تحميله إلى هذا الكائن.

```cpp
Aspose::Words::LoadFormat Aspose::Words::Document::get_OriginalLoadFormat() const
```

## ملاحظات


إذا أنشأت مستندًا فارغًا جديدًا، تُرجع قيمة [Doc](../../loadformat/).

## أمثلة



يوضح كيفية استرجاع تفاصيل عملية تحميل المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(get_MyDir() + u"Document.docx", doc->get_OriginalFileName());
ASSERT_EQ(Aspose::Words::LoadFormat::Docx, doc->get_OriginalLoadFormat());
```

## انظر أيضًا

* Enum [LoadFormat](../../loadformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
