---
title: "Aspose::Words::Tables::Table::get_FirstRow yöntemi"
linktitle: "get_FirstRow"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Table::get_FirstRow yöntemi. Tablo içindeki ilk Row düğümünü C++'da döndürür."
type: docs
weight: 23000
url: /tr/cpp/aspose.words.tables/table/get_firstrow/
---
## Table::get_FirstRow method


Tablodaki ilk [Row](../../row/) düğümünü döndürür.

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::Tables::Table::get_FirstRow()
```


## Örnekler



Bir belgedeki tüm tabloların ilk ve son satırlarını nasıl kaldıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(5, tables->idx_get(0)->get_Rows()->get_Count());
ASSERT_EQ(4, tables->idx_get(1)->get_Rows()->get_Count());

for (auto&& table : System::IterateOver(tables->LINQ_OfType<System::SharedPtr<Aspose::Words::Tables::Table> >()))
{
    System::SharedPtr<Aspose::Words::Tables::Row> condExpression = table->get_FirstRow();
    if (condExpression != nullptr)
    {
        condExpression->Remove();
    }
    System::SharedPtr<Aspose::Words::Tables::Row> condExpression2 = table->get_LastRow();
    if (condExpression2 != nullptr)
    {
        condExpression2->Remove();
    }
}

ASSERT_EQ(3, tables->idx_get(0)->get_Rows()->get_Count());
ASSERT_EQ(2, tables->idx_get(1)->get_Rows()->get_Count());
```


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

* Class [Row](../../row/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
