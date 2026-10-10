---
title: "Aspose::Words::Tables::CellFormat::get_Borders yöntemi"
linktitle: "get_Borders"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::CellFormat::get_Borders yöntemi. Hücrenin kenarlık koleksiyonunu C++'ta alır."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.tables/cellformat/get_borders/
---
## CellFormat::get_Borders method


Hücrenin kenarlık koleksiyonunu alır.

```cpp
System::SharedPtr<Aspose::Words::BorderCollection> Aspose::Words::Tables::CellFormat::get_Borders()
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

* Class [BorderCollection](../../../aspose.words/bordercollection/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
