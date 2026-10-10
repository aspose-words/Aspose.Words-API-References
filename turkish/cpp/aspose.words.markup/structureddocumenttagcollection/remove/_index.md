---
title: "Aspose::Words::Markup::StructuredDocumentTagCollection::Remove yöntemi"
linktitle: "Remove"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::StructuredDocumentTagCollection::Remove yöntemi. C++'ta belirtilen tanımlayıcıya sahip yapılandırılmış belge etiketini kaldırır."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.markup/structureddocumenttagcollection/remove/
---
## StructuredDocumentTagCollection::Remove method


Belirtilen kimliğe sahip yapılandırılmış belge etiketini kaldırır.

```cpp
void Aspose::Words::Markup::StructuredDocumentTagCollection::Remove(int32_t id)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| id | int32_t | Yapılandırılmış belge etiketi tanımlayıcısı. |

## Örnekler



Yapılandırılmış belge etiketinin nasıl kaldırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTagCollection> structuredDocumentTags = doc->get_Range()->get_StructuredDocumentTags();
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> sdt;
for (int32_t i = 0; i < structuredDocumentTags->get_Count(); i++)
{
    sdt = structuredDocumentTags->idx_get(i);
    std::cout << sdt->get_Title() << std::endl;
}

sdt = structuredDocumentTags->GetById(1691867797);
ASSERT_EQ(1691867797, sdt->get_Id());

ASSERT_EQ(5, structuredDocumentTags->get_Count());
// Yapılandırılmış belge etiketini Id ile kaldırın.
structuredDocumentTags->Remove(1691867797);
// Yapılandırılmış belge etiketini 0 konumunda kaldırın.
structuredDocumentTags->RemoveAt(0);
ASSERT_EQ(3, structuredDocumentTags->get_Count());
```

## Ayrıca Bakınız

* Class [StructuredDocumentTagCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
