---
title: "Aspose::Words::ParagraphFormat::get_KeepWithNext metodo"
linktitle: "get_KeepWithNext"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ParagraphFormat::get_KeepWithNext metodo. Vero se il paragrafo deve rimanere nella stessa pagina del paragrafo che lo segue in C++."
type: docs
weight: 18000
url: /it/cpp/aspose.words/paragraphformat/get_keepwithnext/
---
## ParagraphFormat::get_KeepWithNext method


Vero se il paragrafo deve rimanere nella stessa pagina del paragrafo che lo segue.

```cpp
bool Aspose::Words::ParagraphFormat::get_KeepWithNext()
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

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
