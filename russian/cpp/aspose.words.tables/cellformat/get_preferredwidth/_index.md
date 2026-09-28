---
title: "Aspose::Words::Tables::CellFormat::get_PreferredWidth метод"
linktitle: "get_PreferredWidth"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::CellFormat::get_PreferredWidth метод. Возвращает или задает предпочтительную ширину ячейки в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.tables/cellformat/get_preferredwidth/
---
## CellFormat::get_PreferredWidth method


Возвращает или задает предпочтительную ширину ячейки.

```cpp
System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::CellFormat::get_PreferredWidth()
```

## Примечания


Предпочтительная ширина (вместе с параметром Auto Fit таблицы) определяет, как фактическая ширина ячейки вычисляется алгоритмом раскладки таблицы. Раскладка [Table](../../table/) может выполняться Aspose.Words при сохранении документа или Microsoft Word при отображении документа.

Предпочтительная ширина может быть указана в пунктах или в процентах. Предпочтительная ширина также может быть указана как "auto", что означает отсутствие заданной предпочтительной ширины.

Значение по умолчанию — [Auto](../../preferredwidth/auto/).

## Примеры



Показывает, как задать предпочтительную ширину для ячеек таблицы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Существует два способа применения класса "PreferredWidth" к ячейкам таблицы.
// 1 -  Установить абсолютную предпочтительную ширину в пунктах:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(40));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightYellow());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

// 2 -  Установить относительную предпочтительную ширину в процентах от ширины таблицы:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(20));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

builder->InsertCell();

// Ячейка без указанной предпочтительной ширины займет оставшееся доступное пространство.
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());

// Каждая конфигурация свойства "PreferredWidth" создает новый объект.
ASSERT_NE(System::ObjectExt::GetHashCode(table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_PreferredWidth()), System::ObjectExt::GetHashCode(builder->get_CellFormat()->get_PreferredWidth()));

builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightGreen());
builder->Writeln(u"Automatically sized cell.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

## См. также

* Class [PreferredWidth](../../preferredwidth/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
