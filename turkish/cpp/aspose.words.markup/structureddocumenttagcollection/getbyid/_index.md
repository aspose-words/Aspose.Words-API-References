---
title: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetById yöntemi"
linktitle: "GetById"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetById yöntemi. C++'ta tanımlayıcı ile yapılandırılmış belge etiketini döndürür."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.markup/structureddocumenttagcollection/getbyid/
---
## StructuredDocumentTagCollection::GetById method


Kimliğe göre yapılandırılmış belge etiketini döndürür.

```cpp
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> Aspose::Words::Markup::StructuredDocumentTagCollection::GetById(int32_t id)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| id | int32_t | Yapılandırılmış belge etiketi tanımlayıcısı. |
## Açıklamalar


Belirtilen tanımlayıcıya sahip yapılandırılmış belge etiketi bulunamazsa null döndürür.

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

* Interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* Class [StructuredDocumentTagCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
