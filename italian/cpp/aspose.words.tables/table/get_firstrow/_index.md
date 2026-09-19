---
title: "Aspose::Words::Tables::Table::get_FirstRow metodo"
linktitle: "get_FirstRow"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::Table::get_FirstRow metodo. Restituisce il primo nodo Row nella tabella in C++."
type: docs
weight: 23000
url: /it/cpp/aspose.words.tables/table/get_firstrow/
---
## Table::get_FirstRow method


Restituisce il primo nodo [Row](../../row/) nella tabella.

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::Tables::Table::get_FirstRow()
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


Mostra come combinare le righe di due tabelle in una sola.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

// Di seguito sono riportati due modi per ottenere una tabella da un documento.
// 1 -  Dalla collezione "Tables" di un nodo Body:
System::SharedPtr<Aspose::Words::Tables::Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 -  Utilizzando il metodo "GetChild":
auto secondTable = System::ExplicitCast<Aspose::Words::Tables::Table>(doc->GetChild(Aspose::Words::NodeType::Table, 1, true));

// Aggiungi tutte le righe dalla tabella corrente a quella successiva.
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// Rimuovi il contenitore della tabella vuota.
secondTable->Remove();

doc->Save(get_ArtifactsDir() + u"Table.CombineTables.docx");
```

## Vedi anche

* Class [Row](../../row/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
