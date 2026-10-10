---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_Title method"
linktitle: "get_Title"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_Title method. Bu SDT ile ilişkili dostane adı belirtir. C++'da null olamaz."
type: docs
weight: 12000
url: /tr/cpp/aspose.words.markup/istructureddocumenttag/get_title/
---
## IStructuredDocumentTag::get_Title method


Bu **SDT** ile ilişkili dostane adı belirtir. Null olamaz.

```cpp
virtual System::String Aspose::Words::Markup::IStructuredDocumentTag::get_Title() const =0
```


## Örnekler



Yapılandırılmış belge etiketinin nasıl alınacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags by id.docx");

// Kimliğe göre yapılandırılmış belge etiketini al.
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> sdt = doc->get_Range()->get_StructuredDocumentTags()->GetById(1160505028);
std::cout << System::Convert::ToString(sdt->get_IsMultiSection()) << std::endl;
std::cout << sdt->get_Title() << std::endl;

// Başlığa göre yapılandırılmış belge etiketini veya aralık etiketini al.
sdt = doc->get_Range()->get_StructuredDocumentTags()->GetByTitle(u"Alias4");
std::cout << sdt->get_Id() << std::endl;
```

## Ayrıca Bakınız

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
