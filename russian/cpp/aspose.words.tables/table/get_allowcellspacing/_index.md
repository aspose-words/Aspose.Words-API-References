---
title: "Aspose::Words::Tables::Table::get_AllowCellSpacing метод"
linktitle: "get_AllowCellSpacing"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::Table::get_AllowCellSpacing метод. Получает или задает параметр \"Разрешить расстояние между ячейками\" в C++."
type: docs
weight: 13000
url: /ru/cpp/aspose.words.tables/table/get_allowcellspacing/
---
## Table::get_AllowCellSpacing method


Получает или задаёт параметр "Allow spacing between cells".

```cpp
bool Aspose::Words::Tables::Table::get_AllowCellSpacing()
```


## Примеры



Показывает, как включить расстояние между отдельными ячейками в таблице.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Animal");
builder->InsertCell();
builder->Write(u"Class");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Dog");
builder->InsertCell();
builder->Write(u"Mammal");
builder->EndTable();

table->set_CellSpacing(3);

// Установите свойство "AllowCellSpacing" в "true", чтобы включить расстояние между ячейками
// со значением, равным значению свойства "CellSpacing", в пунктах.
// Установите свойство "AllowCellSpacing" в "false", чтобы отключить расстояние между ячейками
// и игнорировать значение свойства "CellSpacing".
table->set_AllowCellSpacing(allowCellSpacing);

doc->Save(get_ArtifactsDir() + u"Table.AllowCellSpacing.html");

// Изменение свойства "CellSpacing" автоматически включит расстояние между ячейками.
table->set_CellSpacing(5);

ASSERT_TRUE(table->get_AllowCellSpacing());
```

## См. также

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
