---
title: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetById method"
linktitle: "GetById"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetById method. يُرجِع علامة المستند المُنظمة حسب المعرف في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.markup/structureddocumenttagcollection/getbyid/
---
## StructuredDocumentTagCollection::GetById method


يعيد علامة المستند المهيكلة حسب المعرف.

```cpp
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> Aspose::Words::Markup::StructuredDocumentTagCollection::GetById(int32_t id)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| معرف | int32_t | معرّف علامة المستند المُنظمة. |
## ملاحظات


يرجع null إذا تعذر العثور على علامة المستند المُنظمة ذات المعرف المحدد.

## أمثلة



يوضح كيفية الحصول على علامة المستند المهيكلة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags by id.docx");

// احصل على علامة المستند المهيكلة حسب المعرف.
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> sdt = doc->get_Range()->get_StructuredDocumentTags()->GetById(1160505028);
std::cout << System::Convert::ToString(sdt->get_IsMultiSection()) << std::endl;
std::cout << sdt->get_Title() << std::endl;

// احصل على علامة المستند المهيكلة أو العلامة المتقاربة حسب العنوان.
sdt = doc->get_Range()->get_StructuredDocumentTags()->GetByTitle(u"Alias4");
std::cout << sdt->get_Id() << std::endl;
```

## انظر أيضًا

* Interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* Class [StructuredDocumentTagCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
