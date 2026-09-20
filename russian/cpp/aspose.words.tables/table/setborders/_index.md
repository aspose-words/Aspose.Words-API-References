---
title: "Метод Aspose::Words::Tables::Table::SetBorders"
linktitle: "SetBorders"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Tables::Table::SetBorders. Устанавливает все границы таблицы в указанный стиль линии, ширину и цвет в C++."
type: docs
weight: 69000
url: /ru/cpp/aspose.words.tables/table/setborders/
---
## Table::SetBorders method


Устанавливает все границы таблицы с заданным стилем линии, шириной и цветом.

```cpp
void Aspose::Words::Tables::Table::SetBorders(Aspose::Words::LineStyle lineStyle, double lineWidth, System::Drawing::Color color)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| lineStyle | Aspose::Words::LineStyle | Стиль линии, который следует применить. |
| lineWidth | double | Ширина линии, которую нужно установить (в пунктах). |
| color | System::Drawing::Color | Цвет, используемый для границы. |

## Примеры



Показывает, как применить цвет границы и затенения при построении таблицы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте таблицу и задайте цвет/толщину по умолчанию для её границ.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
table->SetBorders(Aspose::Words::LineStyle::Single, 2.0, System::Drawing::Color::get_Black());

// Создайте строку с двумя ячейками, имеющими разные цвета фона.
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSkyBlue());
builder->Writeln(u"Row 1, Cell 1.");
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());
builder->Writeln(u"Row 1, Cell 2.");
builder->EndRow();

// Сбросьте форматирование ячейки, чтобы отключить цвета фона
// установите пользовательскую толщину границы для всех новых ячеек, создаваемых построителем,
// затем создайте вторую строку.
builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->get_Borders()->get_Left()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Right()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Top()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Bottom()->set_LineWidth(4.0);

builder->InsertCell();
builder->Writeln(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Writeln(u"Row 2, Cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.TableBordersAndShading.docx");
```


Показывает, как отформатировать все границы таблицы одновременно.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Удалить все существующие границы из таблицы.
table->ClearBorders();

// Установить одну зеленую линию в качестве всех внешних и внутренних границ этой таблицы.
table->SetBorders(Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Table.SetBorders.docx");
```

## См. также

* Enum [LineStyle](../../../aspose.words/linestyle/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
