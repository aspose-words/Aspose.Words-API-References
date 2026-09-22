---
title: "Aspose::Words::Markup::StructuredDocumentTagCollection sınıfı"
linktitle: "StructuredDocumentTagCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::StructuredDocumentTagCollection sınıfı. Belirtilen aralıktaki yapılandırılmış belge etiketlerini temsil eden IStructuredDocumentTag örneklerinin bir koleksiyonu. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 12000
url: /tr/cpp/aspose.words.markup/structureddocumenttagcollection/
---
## StructuredDocumentTagCollection class


Belirtilen aralıktaki yapılandırılmış belge etiketlerini temsil eden [IStructuredDocumentTag](../istructureddocumenttag/) örneklerinin bir koleksiyonu. Daha fazla bilgi için [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) belge makalesini ziyaret edin.

```cpp
class StructuredDocumentTagCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Count](./get_count/)() | Koleksiyondaki yapılandırılmış belge etiketlerinin sayısını döndürür. |
| [GetById](./getbyid/)(int32_t) | Kimliğe göre yapılandırılmış belge etiketini döndürür. |
| [GetByTag](./getbytag/)(const System::String\&) | Belirtilen etikete sahip koleksiyonda bulunan ilk yapılandırılmış belge etiketini döndürür. |
| [GetByTitle](./getbytitle/)(const System::String\&) | Belirtilen başlığa sahip koleksiyonda bulunan ilk yapılandırılmış belge etiketini döndürür. |
| [GetEnumerator](./getenumerator/)() override | Bir enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Belirtilen indeksteki yapılandırılmış belge etiketini döndürür. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(int32_t) | Belirtilen kimliğe sahip yapılandırılmış belge etiketini kaldırır. |
| [RemoveAt](./removeat/)(int32_t) | Belirtilen indeksteki bir yapılandırılmış belge etiketini kaldırır. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
