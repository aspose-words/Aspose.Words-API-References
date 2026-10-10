---
title: "طريقة Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle"
linktitle: "GetByTitle"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle. تُرجع أول علامة مستند مُنظمة يتم العثور عليها في المجموعة بالعنوان المحدد في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.markup/structureddocumenttagcollection/getbytitle/
---
## StructuredDocumentTagCollection::GetByTitle method


يعيد أول علامة مستند مهيكلة يتم العثور عليها في المجموعة بالعنوان المحدد.

```cpp
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle(const System::String &title)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| title | const System::String\& | عنوان علامة المستند المُنظمة. |
## ملاحظات


تُرجع null إذا تعذّر العثور على علامة المستند المُنظمة بالعنوان المحدد.

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
