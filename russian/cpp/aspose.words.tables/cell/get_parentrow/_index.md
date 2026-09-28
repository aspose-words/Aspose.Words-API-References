---
title: "Aspose::Words::Tables::Cell::get_ParentRow method"
linktitle: "get_ParentRow"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::Cell::get_ParentRow method. Возвращает родительскую строку ячейки в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words.tables/cell/get_parentrow/
---
## Cell::get_ParentRow method


Возвращает родительскую строку ячейки.

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::Tables::Cell::get_ParentRow()
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

* Class [Row](../../row/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
