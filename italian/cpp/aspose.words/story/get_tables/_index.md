---
title: "Aspose::Words::Story::get_Tables metodo"
linktitle: "get_Tables"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Story::get_Tables metodo. Ottiene una collezione di tabelle che sono figli immediati della storia in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words/story/get_tables/
---
## Story::get_Tables method


Ottiene una collezione di tabelle che sono figli immediati della storia.

```cpp
System::SharedPtr<Aspose::Words::Tables::TableCollection> Aspose::Words::Story::get_Tables() override
```


## Esempi



Mostra come rimuovere la prima e l'ultima riga di tutte le tabelle in un documento.
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

## Vedi anche

* Class [TableCollection](../../../aspose.words.tables/tablecollection/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
