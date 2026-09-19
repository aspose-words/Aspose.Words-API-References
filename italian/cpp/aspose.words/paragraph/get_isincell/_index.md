---
title: "Aspose::Words::Paragraph::get_IsInCell method"
linktitle: "get_IsInCell"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Paragraph::get_IsInCell method. Vero se questo paragrafo è un figlio immediato di Cell; falso altrimenti in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words/paragraph/get_isincell/
---
## Paragraph::get_IsInCell method


Vero se questo paragrafo è un figlio immediato di [Cell](../../../aspose.words.tables/cell/); falso altrimenti.

```cpp
bool Aspose::Words::Paragraph::get_IsInCell()
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

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
