---
title: "Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly method"
linktitle: "RemoveSelfOnly"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly method. Bu SDT düğümünü yalnızca kendisini kaldırır, ancak içeriğini belge ağacında tutar (C++)."
type: docs
weight: 17500
url: /tr/cpp/aspose.words.markup/istructureddocumenttag/removeselfonly/
---
## IStructuredDocumentTag::RemoveSelfOnly method


Bu SDT düğümünü yalnızca kendisini kaldırır, ancak içeriğini belge ağacında tutar.

```cpp
virtual void Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly()=0
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

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
