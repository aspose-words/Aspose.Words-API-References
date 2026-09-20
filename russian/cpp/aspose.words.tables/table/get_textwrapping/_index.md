---
title: "Aspose::Words::Tables::Table::get_TextWrapping метод"
linktitle: "get_TextWrapping"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::Table::get_TextWrapping метод. Получает или задает TextWrapping для таблицы в C++."
type: docs
weight: 38000
url: /ru/cpp/aspose.words.tables/table/get_textwrapping/
---
## Table::get_TextWrapping method


Получает или задает [TextWrapping](./) для таблицы.

```cpp
Aspose::Words::Tables::TextWrapping Aspose::Words::Tables::Table::get_TextWrapping()
```


## Примеры



Показывает, как работать с обтеканием текста таблицы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell 1");
builder->InsertCell();
builder->Write(u"Cell 2");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

builder->get_Font()->set_Size(16);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Установите свойство "TextWrapping" в "TextWrapping.Around", чтобы таблица оборачивала текст вокруг неё,
// и переместите её вниз в абзац ниже, задав позицию.
table->set_TextWrapping(Aspose::Words::Tables::TextWrapping::Around);
table->set_AbsoluteHorizontalDistance(100);
table->set_AbsoluteVerticalDistance(20);

doc->Save(get_ArtifactsDir() + u"Table.WrapText.docx");
```

## См. также

* Enum [TextWrapping](../../textwrapping/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
