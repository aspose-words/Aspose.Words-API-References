---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_Title method"
linktitle: "get_Title"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_Title method. يحدد الاسم الودي المرتبط بهذه الـ SDT. لا يمكن أن يكون فارغًا في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words.markup/istructureddocumenttag/get_title/
---
## IStructuredDocumentTag::get_Title method


يحدد الاسم الودي المرتبط بهذا **SDT**. لا يمكن أن يكون null.

```cpp
virtual System::String Aspose::Words::Markup::IStructuredDocumentTag::get_Title() const =0
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
