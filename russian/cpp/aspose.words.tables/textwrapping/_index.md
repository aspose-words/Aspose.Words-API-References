---
title: "Aspose::Words::Tables::TextWrapping enum"
linktitle: "TextWrapping"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::TextWrapping enum. Указывает, как текст оборачивается вокруг таблицы в C++."
type: docs
weight: 16000
url: /ru/cpp/aspose.words.tables/textwrapping/
---
## TextWrapping enum


Указывает, как текст обтекает таблицу.

```cpp
enum class TextWrapping
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 | Текст и таблица отображаются в порядке их появления в документе. |
| Вокруг | 1 | Текст оборачивается вокруг таблицы, занимая доступное боковое пространство. |
| Default | н/д | Значение по умолчанию. |


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
