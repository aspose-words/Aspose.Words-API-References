---
title: "Aspose::Words::Tables::Table::SetBorder метод"
linktitle: "SetBorder"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::Table::SetBorder метод. Устанавливает указанную границу таблицы в заданный стиль линии, ширину и цвет в C++."
type: docs
weight: 68000
url: /ru/cpp/aspose.words.tables/table/setborder/
---
## Table::SetBorder method


Устанавливает указанную границу таблицы с заданным стилем линии, шириной и цветом.

```cpp
void Aspose::Words::Tables::Table::SetBorder(Aspose::Words::BorderType borderType, Aspose::Words::LineStyle lineStyle, double lineWidth, System::Drawing::Color color, bool isOverrideCellBorders)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| borderType | Aspose::Words::BorderType | Граница таблицы, которую нужно изменить. |
| lineStyle | Aspose::Words::LineStyle | Стиль линии, который следует применить. |
| lineWidth | double | Ширина линии, которую нужно установить (в пунктах). |
| color | System::Drawing::Color | Цвет, используемый для границы. |
| isOverrideCellBorders | bool | Когда **true**, приводит к удалению всех существующих явных границ ячеек. |

## Примеры



Показывает, как применить контурную границу к таблице.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Выровняйте таблицу по центру страницы.
table->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);

// Очистите любые существующие границы и заливку в таблице.
table->ClearBorders();
table->ClearShading();

// Добавьте зеленые границы к контуру таблицы.
table->SetBorder(Aspose::Words::BorderType::Left, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Right, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Top, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Bottom, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);

// Заполните ячейки светло-зелёным сплошным цветом.
table->SetShading(Aspose::Words::TextureIndex::TextureSolid, System::Drawing::Color::get_LightGreen(), System::Drawing::Color::Empty);

doc->Save(get_ArtifactsDir() + u"Table.SetOutlineBorders.docx");
```

## См. также

* Enum [BorderType](../../../aspose.words/bordertype/)
* Enum [LineStyle](../../../aspose.words/linestyle/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
