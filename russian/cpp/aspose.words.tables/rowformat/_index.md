---
title: "Aspose::Words::Tables::RowFormat class"
linktitle: "RowFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::RowFormat class. Представляет все форматирование строки таблицы. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.tables/rowformat/
---
## RowFormat class


Представляет всё форматирование строки таблицы. Чтобы узнать больше, посетите статью документации [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class RowFormat : public Aspose::Words::IBorderAttrSource
```

## Методы

| Метод | Описание |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Сбрасывает форматирование строки к значениям по умолчанию. |
| [get_AllowBreakAcrossPages](./get_allowbreakacrosspages/)() | Истина, если текст в строке таблицы может разбиваться при разрыве страницы. |
| [get_Borders](./get_borders/)() | Получает коллекцию границ ячеек по умолчанию для строки. |
| [get_HeadingFormat](./get_headingformat/)() | Истина, если строка повторяется в качестве заголовка таблицы на каждой странице, когда таблица занимает более одной страницы. |
| [get_Height](./get_height/)() | Получает или задает высоту строки таблицы в пунктах. |
| [get_HeightRule](./get_heightrule/)() | Получает или задает правило определения высоты строки таблицы. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowBreakAcrossPages](./set_allowbreakacrosspages/)(bool) | Сеттер для [Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages](./get_allowbreakacrosspages/). |
| [set_HeadingFormat](./set_headingformat/)(bool) | Сеттер для [Aspose::Words::Tables::RowFormat::get_HeadingFormat](./get_headingformat/). |
| [set_Height](./set_height/)(double) | Сеттер для [Aspose::Words::Tables::RowFormat::get_Height](./get_height/). |
| [set_HeightRule](./set_heightrule/)(Aspose::Words::HeightRule) | Сеттер для [Aspose::Words::Tables::RowFormat::get_HeightRule](./get_heightrule/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как построить таблицу с пользовательскими границами.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// Установка параметров форматирования таблицы для DocumentBuilder
// будет применять их к каждой строке и ячейке, которые мы добавляем с его помощью.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// Изменение форматирования будет применено к текущей ячейке,
// и к любым новым ячейкам, которые мы создаём с помощью билдера позже.
// Это не повлияет на ячейки, которые мы добавили ранее.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// Увеличьте высоту строки, чтобы разместить вертикальный текст.
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTable.docx");
```


Показывает, как изменить формат строк и ячеек в таблице.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"City");
builder->InsertCell();
builder->Write(u"Country");
builder->EndRow();
builder->InsertCell();
builder->Write(u"London");
builder->InsertCell();
builder->Write(u"U.K.");
builder->EndTable();

// Используйте свойство "RowFormat" первой строки, чтобы изменить форматирование
// содержимого всех ячеек в этой строке.
System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = table->get_FirstRow()->get_RowFormat();
rowFormat->set_Height(25);
rowFormat->get_Borders()->idx_get(Aspose::Words::BorderType::Bottom)->set_Color(System::Drawing::Color::get_Red());

// Используйте свойство "CellFormat" первой ячейки в последней строке, чтобы изменить форматирование содержимого этой ячейки.
System::SharedPtr<Aspose::Words::Tables::CellFormat> cellFormat = table->get_LastRow()->get_FirstCell()->get_CellFormat();
cellFormat->set_Width(100);
cellFormat->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());

doc->Save(get_ArtifactsDir() + u"Table.RowCellFormat.docx");
```


Показывает, как изменить форматирование строки таблицы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Используйте свойство "RowFormat" первой строки, чтобы задать форматирование, изменяющее внешний вид всей строки.
System::SharedPtr<Aspose::Words::Tables::Row> firstRow = table->get_FirstRow();
firstRow->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::None);
firstRow->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Auto);
firstRow->get_RowFormat()->set_AllowBreakAcrossPages(true);

doc->Save(get_ArtifactsDir() + u"Table.RowFormat.docx");
```

## См. также

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
