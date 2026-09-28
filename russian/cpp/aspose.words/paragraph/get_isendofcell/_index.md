---
title: "Aspose::Words::Paragraph::get_IsEndOfCell метод"
linktitle: "get_IsEndOfCell"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Paragraph::get_IsEndOfCell метод. True если этот абзац является последним абзацем в Cell; false в противном случае в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words/paragraph/get_isendofcell/
---
## Paragraph::get_IsEndOfCell method


True если этот абзац является последним абзацем в [Cell](../../../aspose.words.tables/cell/); иначе — false.

```cpp
bool Aspose::Words::Paragraph::get_IsEndOfCell()
```


## Примеры



Показывает, как установить таблицу, чтобы она оставалась вместе на одной странице.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table spanning two pages.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Включение KeepWithNext для каждого абзаца в таблице, за исключением
// последних в последней строке предотвратит разбиение таблицы на несколько страниц.
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

## См. также

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
