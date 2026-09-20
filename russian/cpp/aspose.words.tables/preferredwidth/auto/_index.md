---
title: "Aspose::Words::Tables::PreferredWidth::Auto метод"
linktitle: "Авто"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::PreferredWidth::Auto метод. Возвращает экземпляр, представляющий значение \"предпочтительная ширина не указана\" в C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.tables/preferredwidth/auto/
---
## PreferredWidth::Auto method


Возвращает экземпляр, представляющий значение \"предпочтительная ширина не указана\".

```cpp
static System::SharedPtr<Aspose::Words::Tables::PreferredWidth> & Aspose::Words::Tables::PreferredWidth::Auto()
```


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

* Class [PreferredWidth](../)
* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
