---
title: "Метод Aspose::Words::DocumentBuilder::get_Font"
linktitle: "get_Font"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DocumentBuilder::get_Font. Возвращает объект, представляющий текущие свойства форматирования шрифта в C++."
type: docs
weight: 17000
url: /ru/cpp/aspose.words/documentbuilder/get_font/
---
## DocumentBuilder::get_Font method


Возвращает объект, представляющий текущие свойства форматирования шрифта.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::DocumentBuilder::get_Font()
```

## Примечания


Используйте [Font](./) для доступа к свойствам форматирования шрифта и их изменения.

Укажите форматирование шрифта перед вставкой текста.

## Примеры



Показывает, как вставить строку, окружённую границей, в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```


Показывает, как создать отформатированную таблицу с помощью [DocumentBuilder](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
table->set_LeftIndent(20);

// Установите некоторые параметры форматирования текста и внешнего вида таблицы.
builder->get_RowFormat()->set_Height(40);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::AtLeast);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::FromArgb(198, 217, 241));

builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->get_Font()->set_Size(16);
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Bold(true);

// Настройка параметров форматирования в построителе документа применит их
// к текущей ячейке/строке, в которой находится курсор,
// а также к любым новым ячейкам и строкам, созданным с помощью этого построителя.
builder->Write(u"Header Row,\n Cell 1");
builder->InsertCell();
builder->Write(u"Header Row,\n Cell 2");
builder->InsertCell();
builder->Write(u"Header Row,\n Cell 3");
builder->EndRow();

// Перенастройте объекты форматирования построителя для новых строк и ячеек, которые мы собираемся создать.
// The builder will not apply these to the first row already created so that it will stand out as a header row.
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_White());
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_RowFormat()->set_Height(30);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Auto);
builder->InsertCell();
builder->get_Font()->set_Size(12);
builder->get_Font()->set_Bold(false);

builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 3.");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 3.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateFormattedTable.docx");
```

## См. также

* Class [Font](../../font/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
