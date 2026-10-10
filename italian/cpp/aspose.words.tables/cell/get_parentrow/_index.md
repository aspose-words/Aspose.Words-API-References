---
title: "Metodo Aspose::Words::Tables::Cell::get_ParentRow"
linktitle: "get_ParentRow"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Tables::Cell::get_ParentRow. Restituisce la riga padre della cella in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.tables/cell/get_parentrow/
---
## Cell::get_ParentRow method


Restituisce la riga genitore della cella.

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::Tables::Cell::get_ParentRow()
```


## Esempi



Mostra come impostare una tabella per rimanere unita nella stessa pagina.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table spanning two pages.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Abilitare KeepWithNext per ogni paragrafo nella tabella tranne per il
// gli ultimi nella riga finale impediranno alla tabella di dividersi su più pagine.
for (auto&& cell : System::IterateOver<Aspose::Words::Tables::Cell>(table->GetChildNodes(Aspose::Words::NodeType::Cell, true)))
{
    for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(cell->get_Paragraphs()))
    {
        ASSERT_TRUE(para->get_IsInCell());

        if (!(cell->get_ParentRow()->get_IsLastRow() && para->get_IsEndOfCell()))
        {
            para->get_ParagraphFormat()->set_KeepWithNext(true);
        }
    }
}

doc->Save(get_ArtifactsDir() + u"Table.KeepTableTogether.docx");
```

## Vedi anche

* Class [Row](../../row/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
