---
title: "Метод Aspose::Words::Paragraph::get_IsInCell"
linktitle: "get_IsInCell"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Paragraph::get_IsInCell. Истина, если этот абзац является непосредственным дочерним элементом Cell; иначе ложь в C++."
type: docs
weight: 13000
url: /ru/cpp/aspose.words/paragraph/get_isincell/
---
## Paragraph::get_IsInCell method


Истина, если этот абзац является непосредственным дочерним элементом [Cell](../../../aspose.words.tables/cell/); иначе ложь.

```cpp
bool Aspose::Words::Paragraph::get_IsInCell()
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
