---
title: "Aspose::Words::Tables::Row::get_IsLastRow metodo"
linktitle: "get_IsLastRow"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::Row::get_IsLastRow metodo. Vero se questa è l'ultima riga in una tabella; falso altrimenti in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.tables/row/get_islastrow/
---
## Row::get_IsLastRow method


Vero se questa è l'ultima riga in una tabella; falso altrimenti.

```cpp
bool Aspose::Words::Tables::Row::get_IsLastRow()
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

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
