---
title: "Aspose::Words::Tables::CellFormat::get_Borders метод"
linktitle: "get_Borders"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::CellFormat::get_Borders метод. Получает коллекцию границ ячейки в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.tables/cellformat/get_borders/
---
## CellFormat::get_Borders method


Получает коллекцию границ ячейки.

```cpp
System::SharedPtr<Aspose::Words::BorderCollection> Aspose::Words::Tables::CellFormat::get_Borders()
```


## Примеры



Показывает, как объединить строки из двух таблиц в одну.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

// Ниже представлены два способа получения таблицы из документа.
// 1 -  Из коллекции "Tables" узла Body:
System::SharedPtr<Aspose::Words::Tables::Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 -  С использованием метода "GetChild":
auto secondTable = System::ExplicitCast<Aspose::Words::Tables::Table>(doc->GetChild(Aspose::Words::NodeType::Table, 1, true));

// Добавьте все строки из текущей таблицы к следующей.
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// Удалите пустой контейнер таблицы.
secondTable->Remove();

doc->Save(get_ArtifactsDir() + u"Table.CombineTables.docx");
```

## См. также

* Class [BorderCollection](../../../aspose.words/bordercollection/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
