---
title: "Метод Aspose::Words::Tables::Table::get_PreferredWidth"
linktitle: "get_PreferredWidth"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Tables::Table::get_PreferredWidth. Получает или задает предпочтительную ширину таблицы в C++."
type: docs
weight: 29000
url: /ru/cpp/aspose.words.tables/table/get_preferredwidth/
---
## Table::get_PreferredWidth method


Получает или задает предпочтительную ширину таблицы.

```cpp
System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::Table::get_PreferredWidth()
```

## Примечания


Значение по умолчанию — [Auto](../../preferredwidth/auto/).

## Примеры



Показывает, как установить таблицу для автоматической подгонки до 50% ширины страницы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell #1");
builder->InsertCell();
builder->Write(u"Cell #2");
builder->InsertCell();
builder->Write(u"Cell #3");

table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(50));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

## См. также

* Class [PreferredWidth](../../preferredwidth/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
