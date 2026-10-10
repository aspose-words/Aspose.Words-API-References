---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection metodu"
linktitle: "get_IsMultiSection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection yöntemi. Bu örnek, C++'ta aralıklı (çok bölümlü) bir yapılandırılmış belge etiketi ise true döndürür."
type: docs
weight: 3500
url: /tr/cpp/aspose.words.markup/istructureddocumenttag/get_ismultisection/
---
## IStructuredDocumentTag::get_IsMultiSection method


Bu örnek bir aralıklı (çok bölümlü) yapılandırılmış belge etiketi ise true döndürür.

```cpp
virtual bool Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection()=0
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
