---
title: "Aspose::Words::Markup::IStructuredDocumentTag::GetChildNodes metodu"
linktitle: "GetChildNodes"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::IStructuredDocumentTag::GetChildNodes metodu. Belirtilen türlerle eşleşen alt düğümlerin canlı bir koleksiyonunu C++'da döndürür."
type: docs
weight: 14500
url: /tr/cpp/aspose.words.markup/istructureddocumenttag/getchildnodes/
---
## IStructuredDocumentTag::GetChildNodes method


Belirtilen türlerle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür.

```cpp
virtual System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::IStructuredDocumentTag::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep)=0
```


## Örnekler



Yapılandırılmış belge etiketini nasıl kaldıracağını gösterir, ancak içindeki içeriği korur.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// Bu koleksiyon, aralıklı ve aralıklı olmayan yapılandırılmış etiketlere erişim için birleşik bir arayüz sağlar.
System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>> sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(5, sdts->LINQ_Count());

// Burada, aralıklı ve aralıklı olmayan yapılandırılmış etiketlerin ortak arayüzünden alt düğümleri alabiliriz.
for (auto&& sdt : System::IterateOver(sdts))
{
    if (sdt->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count() > 0)
    {
        sdt->RemoveSelfOnly();
    }
}

sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(0, sdts->LINQ_Count());
```

## Ayrıca Bakınız

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
