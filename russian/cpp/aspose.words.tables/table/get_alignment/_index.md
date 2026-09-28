---
title: "Aspose::Words::Tables::Table::get_Alignment метод"
linktitle: "get_Alignment"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::Table::get_Alignment метод. Указывает, как выравнивается встроенная таблица в документе в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.tables/table/get_alignment/
---
## Table::get_Alignment method


Указывает, как встроенная таблица выравнивается в документе.

```cpp
Aspose::Words::Tables::TableAlignment Aspose::Words::Tables::Table::get_Alignment()
```

## Примечания


Значение по умолчанию: [Слева](../../tablealignment/).

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

* Enum [TableAlignment](../../tablealignment/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
