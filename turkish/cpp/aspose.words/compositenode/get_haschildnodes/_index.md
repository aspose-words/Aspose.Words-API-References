---
title: "Aspose::Words::CompositeNode::get_HasChildNodes yöntemi"
linktitle: "get_HasChildNodes"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::CompositeNode::get_HasChildNodes yöntemi. Bu düğümün herhangi bir alt düğümü varsa C++'de true döndürür."
type: docs
weight: 6000
url: /tr/cpp/aspose.words/compositenode/get_haschildnodes/
---
## CompositeNode::get_HasChildNodes method


Bu düğümün herhangi bir çocuğu varsa **true** döndürür.

```cpp
bool Aspose::Words::CompositeNode::get_HasChildNodes()
```


## Örnekler



İki tablodan satırların nasıl birleştirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

// Aşağıda bir belgeden tablo almanın iki yolu verilmiştir.
// 1 -  Body düğümünün "Tables" koleksiyonundan:
System::SharedPtr<Aspose::Words::Tables::Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 -  "GetChild" yöntemini kullanarak:
auto secondTable = System::ExplicitCast<Aspose::Words::Tables::Table>(doc->GetChild(Aspose::Words::NodeType::Table, 1, true));

// Mevcut tablodan tüm satırları sonraki tabloya ekle.
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// Boş tablo kapsayıcısını kaldır.
secondTable->Remove();

doc->Save(get_ArtifactsDir() + u"Table.CombineTables.docx");
```

## Ayrıca Bakınız

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
