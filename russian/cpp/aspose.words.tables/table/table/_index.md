---
title: "Aspose::Words::Tables::Table::Table конструктор"
linktitle: "Table"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::Table::Table конструктор. Инициализирует новый экземпляр класса Table в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.tables/table/table/
---
## Table::Table constructor


Инициализирует новый экземпляр класса [Table](../).

```cpp
Aspose::Words::Tables::Table::Table(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| док | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Документ‑владелец. |
## Примечания


Когда [Table](../) создаётся, она принадлежит указанному документу, но ещё не является частью документа, и [ParentNode](../../../aspose.words/node/get_parentnode/) имеет значение **null**.

Чтобы добавить [Table](../) в документ, используйте [InsertAfter1()</see> или <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) в истории, где вы хотите вставить таблицу.

## Примеры



Показывает, как создать таблицу.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// Таблицы содержат строки, которые содержат ячейки, которые могут иметь абзацы
// с типичными элементами, такими как фрагменты, фигуры и даже другие таблицы.
// Вызов метода "EnsureMinimum" у таблицы гарантирует, что
// у таблицы будет как минимум одна строка, ячейка и абзац.
auto firstRow = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(firstRow);

auto firstCell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
firstRow->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(firstCell);

auto paragraph = System::MakeObject<Aspose::Words::Paragraph>(doc);
firstCell->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(paragraph);

// Добавьте текст в первую ячейку первой строки таблицы.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Table.CreateTable.docx");
```

## См. также

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
