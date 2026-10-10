---
title: "Aspose::Words::Range::get_StructuredDocumentTags yöntemi"
linktitle: "get_StructuredDocumentTags"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Range::get_StructuredDocumentTags yöntemi. C++'da bu aralıktaki tüm yapılandırılmış belge etiketlerini temsil eden bir StructuredDocumentTags koleksiyonu döndürür."
type: docs
weight: 7000
url: /tr/cpp/aspose.words/range/get_structureddocumenttags/
---
## Range::get_StructuredDocumentTags method


Bu aralıktaki tüm yapılandırılmış belge etiketlerini temsil eden bir [StructuredDocumentTags](./) koleksiyonu döndürür.

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTagCollection> Aspose::Words::Range::get_StructuredDocumentTags()
```


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

* Class [StructuredDocumentTagCollection](../../../aspose.words.markup/structureddocumenttagcollection/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
