---
title: "Метод Aspose::Words::Tables::Table::EnsureMinimum"
linktitle: "EnsureMinimum"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Tables::Table::EnsureMinimum. Если у таблицы нет строк, создает и добавляет одну Row в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.tables/table/ensureminimum/
---
## Table::EnsureMinimum method


Если у таблицы нет строк, создает и добавляет одну [Row](../../row/).

```cpp
void Aspose::Words::Tables::Table::EnsureMinimum()
```


## Примеры



Показывает, как убедиться, что узел таблицы содержит узлы, необходимые для добавления содержимого.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// Таблицы содержат строки, которые содержат ячейки, которые могут содержать абзацы
// с типичными элементами, такими как фрагменты, фигуры и даже другие таблицы.
// Наша новая таблица не имеет этих узлов, и мы не можем добавить в неё содержимое, пока они не появятся.
ASSERT_EQ(0, table->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Вызов метода "EnsureMinimum" у таблицы гарантирует, что
// Таблица должна иметь как минимум одну строку и одну ячейку с пустым абзацем.
table->EnsureMinimum();
table->get_FirstRow()->get_FirstCell()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## См. также

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
