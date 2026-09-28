---
title: "Метод Aspose::Words::Tables::Cell::EnsureMinimum"
linktitle: "EnsureMinimum"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Tables::Cell::EnsureMinimum. Если последний дочерний элемент не является абзацем, создаёт и добавляет один пустой абзац в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.tables/cell/ensureminimum/
---
## Cell::EnsureMinimum method


Если последний дочерний элемент не является абзацем, создаёт и добавляет один пустой абзац.

```cpp
void Aspose::Words::Tables::Cell::EnsureMinimum()
```


## Примеры



Показывает, как убедиться, что узел ячейки содержит необходимые узлы для начала добавления содержимого.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);
auto cell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
row->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(cell);

// Ячейки могут содержать абзацы с типичными элементами, такими как run, shape и даже другие таблицы.
// Новая ячейка не содержит абзацев, и мы не можем добавить содержимое, такое как узлы run и shape, пока они не появятся.
ASSERT_EQ(0, cell->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Вызов метода "EnsureMinimum" для ячейки гарантирует, что
// у ячейки будет как минимум один пустой абзац, к которому мы затем можем добавить содержимое.
cell->EnsureMinimum();
cell->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## См. также

* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
