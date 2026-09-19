---
title: "Aspose::Words::Tables::Table::get_Rows metodo"
linktitle: "get_Rows"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::Table::get_Rows metodo. Fornisce accesso tipizzato alle righe della tabella in C++."
type: docs
weight: 33000
url: /it/cpp/aspose.words.tables/table/get_rows/
---
## Table::get_Rows method


Fornisce un accesso tipizzato alle righe della tabella.

```cpp
System::SharedPtr<Aspose::Words::Tables::RowCollection> Aspose::Words::Tables::Table::get_Rows()
```


## Esempi



Mostra come iterare attraverso tutte le tabelle nel documento e stampare il contenuto di ogni cella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(2, tables->ToArray()->get_Length());

for (int32_t i = 0; i < tables->get_Count(); i++)
{
    std::cout << System::String::Format(u"Start of Table {0}", i) << std::endl;

    System::SharedPtr<Aspose::Words::Tables::RowCollection> rows = tables->idx_get(i)->get_Rows();

    // Possiamo usare il metodo "ToArray" su una raccolta di righe per clonarla in un array.
    ASPOSE_ASSERT_EQ(rows, rows->ToArray());
    ASPOSE_ASSERT_NS(rows, rows->ToArray());

    for (int32_t j = 0; j < rows->get_Count(); j++)
    {
        std::cout << System::String::Format(u"\tStart of Row {0}", j) << std::endl;

        System::SharedPtr<Aspose::Words::Tables::CellCollection> cells = rows->idx_get(j)->get_Cells();

        // Possiamo usare il metodo "ToArray" su una raccolta di celle per clonarla in un array.
        ASPOSE_ASSERT_EQ(cells, cells->ToArray());
        ASPOSE_ASSERT_NS(cells, cells->ToArray());

        for (int32_t k = 0; k < cells->get_Count(); k++)
        {
            System::String cellText = cells->idx_get(k)->ToString(Aspose::Words::SaveFormat::Text).Trim();
            std::cout << System::String::Format(u"\t\tContents of Cell:{0} = \"{1}\"", k, cellText) << std::endl;
        }

        std::cout << System::String::Format(u"\tEnd of Row {0}", j) << std::endl;
    }

    std::cout << System::String::Format(u"End of Table {0}\n", i) << std::endl;
}
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

* Class [RowCollection](../../rowcollection/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
