---
title: "Aspose::Words::NodeCollection::Clear method"
linktitle: "Clear"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::NodeCollection::Clear yöntemi. C++'da bu koleksiyondaki ve belgelerdeki tüm düğümleri kaldırır."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/nodecollection/clear/
---
## NodeCollection::Clear method


Bu koleksiyondaki ve belgedeki tüm düğümleri kaldırır.

```cpp
void Aspose::Words::NodeCollection::Clear()
```


## Örnekler



Bir belgeden tüm bölümleri kaldırmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Bu belge, tüm belge içeriğini içeren ve gösteren birkaç alt düğüme sahip bir bölüme sahiptir.
ASSERT_EQ(1, doc->get_Sections()->get_Count());
ASSERT_EQ(17, doc->get_Sections()->idx_get(0)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", doc->GetText().Trim());

// Bölüm koleksiyonunu temizleyin, bu belgeye ait tüm alt öğeleri kaldıracaktır.
doc->get_Sections()->Clear();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
ASSERT_EQ(System::String::Empty, doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
