---
title: "Aspose::Words::Tables::PreferredWidth::FromPoints метод"
linktitle: "FromPoints"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::PreferredWidth::FromPoints метод. Метод создания, который возвращает новый экземпляр, представляющий предпочтительную ширину, указанную с помощью количества пунктов в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.tables/preferredwidth/frompoints/
---
## PreferredWidth::FromPoints method


Метод создания, который возвращает новый экземпляр, представляющий предпочтительную ширину, заданную в пунктах.

```cpp
static System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::PreferredWidth::FromPoints(double points)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| пункты | double | Значение должно быть от 0 до 22 дюймов (22 * 72 пункта). |

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


Показывает, как использовать инструменты конвертации единиц при указании предпочтительной ширины для ячейки.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(Aspose::Words::ConvertUtil::InchToPoint(3)));
builder->InsertCell();

ASPOSE_ASSERT_EQ(216.0, table->get_FirstRow()->get_FirstCell()->get_CellFormat()->get_PreferredWidth()->get_Value());
```

## См. также

* Class [PreferredWidth](../)
* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
