---
title: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle yöntemi."
linktitle: "GetByTitle"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle yöntemi. C++'ta belirtilen başlığa sahip koleksiyonda bulunan ilk yapılandırılmış belge etiketini döndürür."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.markup/structureddocumenttagcollection/getbytitle/
---
## StructuredDocumentTagCollection::GetByTitle method


Belirtilen başlığa sahip koleksiyonda bulunan ilk yapılandırılmış belge etiketini döndürür.

```cpp
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle(const System::String &title)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| başlık | const System::String\& | Yapılandırılmış belge etiketinin başlığı. |
## Açıklamalar


Belirtilen başlığa sahip yapılandırılmış belge etiketi bulunamazsa null döndürür.

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
