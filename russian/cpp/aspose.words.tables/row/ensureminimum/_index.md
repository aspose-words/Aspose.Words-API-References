---
title: "Метод Aspose::Words::Tables::Row::EnsureMinimum"
linktitle: "EnsureMinimum"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Tables::Row::EnsureMinimum. Если у Row нет ячеек, создает и добавляет одну ячейку Cell в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.tables/row/ensureminimum/
---
## Row::EnsureMinimum method


Если у [Row](../) нет ячеек, создает и добавляет одну [Cell](../../cell/).

```cpp
void Aspose::Words::Tables::Row::EnsureMinimum()
```


## Примеры



Показывает, как убедиться, что узел строки содержит необходимые узлы для начала добавления содержимого.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

// Строки содержат ячейки, содержащие абзацы с типичными элементами, такими как runs, shapes и даже другие таблицы.
// У нашей новой строки нет этих узлов, и мы не можем добавить содержимое, пока они не появятся.
ASSERT_EQ(0, row->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Вызов метода "EnsureMinimum" у таблицы гарантирует, что
// Таблица имеет как минимум одну ячейку с пустым абзацем.
row->EnsureMinimum();
row->get_FirstCell()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## См. также

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
