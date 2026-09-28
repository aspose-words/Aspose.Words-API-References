---
title: "Метод Aspose::Words::Tables::Table::get_AllowAutoFit"
linktitle: "get_AllowAutoFit"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Tables::Table::get_AllowAutoFit. Позволяет Microsoft Word и Aspose.Words автоматически изменять размер ячеек таблицы, чтобы они соответствовали содержимому, в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words.tables/table/get_allowautofit/
---
## Table::get_AllowAutoFit method


Позволяет Microsoft Word и Aspose.Words автоматически изменять размер ячеек в таблице, чтобы они соответствовали содержимому.

```cpp
bool Aspose::Words::Tables::Table::get_AllowAutoFit()
```

## Примечания


Значение по умолчанию — **true**.

## Примеры



Показывает, как включить/выключить автоматическое изменение размера ячеек таблицы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(100));
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->EndRow();
builder->EndTable();

// Установите свойство "AllowAutoFit" в "false", чтобы таблица сохраняла размеры
// всех её строк и ячеек и обрезала содержимое, если оно становится слишком большим, чтобы поместиться.
// Установите свойство "AllowAutoFit" в "true", чтобы позволить таблице изменять ширину и высоту её ячеек
// для размещения их содержимого.
table->set_AllowAutoFit(allowAutoFit);

doc->Save(get_ArtifactsDir() + u"Table.AllowAutoFitOnTable.html");
```

## См. также

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
