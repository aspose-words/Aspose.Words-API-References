---
title: "Aspose::Words::DocumentBuilder::InsertCell method"
linktitle: "InsertCell"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::InsertCell method. Вставляет ячейку таблицы в документ в C++."
type: docs
weight: 29000
url: /ru/cpp/aspose.words/documentbuilder/insertcell/
---
## DocumentBuilder::InsertCell method


Вставляет ячейку таблицы в документ.

```cpp
System::SharedPtr<Aspose::Words::Tables::Cell> Aspose::Words::DocumentBuilder::InsertCell()
```


### ReturnValue

Узел ячейки, который только что был вставлен.
## Примечания


Чтобы начать таблицу, просто вызовите [InsertCell](./). После этого любой контент, который вы добавляете с помощью других методов класса [DocumentBuilder](../), будет добавлен в текущую ячейку.

Чтобы начать новую ячейку в той же строке, вызовите [InsertCell](./) снова.

Чтобы завершить строку таблицы, вызовите [EndRow](../endrow/).

Используйте свойство [CellFormat](../get_cellformat/), чтобы задать форматирование ячейки.

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


Показывает, как использовать DocumentBuilder для создания таблицы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Начните таблицу, затем заполните первую строку двумя ячейками.
builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");

// Вызовите метод билдера "EndRow", чтобы начать новую строку.
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateTable.docx");
```

## См. также

* Class [Cell](../../../aspose.words.tables/cell/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
