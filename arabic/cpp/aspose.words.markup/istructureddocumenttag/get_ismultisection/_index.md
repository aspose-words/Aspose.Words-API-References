---
title: "طريقة Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection"
linktitle: "get_IsMultiSection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection. تُرجع true إذا كان هذا الكائن علامة مستند منسقة متعددة الأقسام (multi-section) في C++."
type: docs
weight: 3500
url: /ar/cpp/aspose.words.markup/istructureddocumenttag/get_ismultisection/
---
## IStructuredDocumentTag::get_IsMultiSection method


يرجع true إذا كانت هذه الحالة علامة مستند مهيكلة بنطاق (متعددة الأقسام).

```cpp
virtual bool Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection()=0
```


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

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
