---
title: "Aspose::Words::Tables::TableAlignment enum"
linktitle: "TableAlignment"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::TableAlignment enum. Указывает выравнивание встроенной таблицы в C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words.tables/tablealignment/
---
## TableAlignment enum


Указывает выравнивание встроенной таблицы.

```cpp
enum class TableAlignment
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Слева | 0 | Таблица выровнена по левому краю. |
| По центру | 1 | Таблица центрирована. |
| Справа | 2 | Таблица выровнена по правому краю. |


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
