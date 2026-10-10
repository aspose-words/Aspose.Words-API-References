---
title: "Aspose::Words::Story::get_Tables yöntemi"
linktitle: "get_Tables"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Story::get_Tables yöntemi. C++'da hikayenin doğrudan alt öğesi olan tabloların bir koleksiyonunu alır."
type: docs
weight: 8000
url: /tr/cpp/aspose.words/story/get_tables/
---
## Story::get_Tables method


Hikayenin doğrudan çocukları olan tablo koleksiyonunu alır.

```cpp
System::SharedPtr<Aspose::Words::Tables::TableCollection> Aspose::Words::Story::get_Tables() override
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

## Ayrıca Bakınız

* Class [TableCollection](../../../aspose.words.tables/tablecollection/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
