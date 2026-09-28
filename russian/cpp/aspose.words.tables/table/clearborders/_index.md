---
title: "Метод Aspose::Words::Tables::Table::ClearBorders"
linktitle: "ClearBorders"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Tables::Table::ClearBorders. Удаляет все границы таблицы и ячеек в этой таблице в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.tables/table/clearborders/
---
## Table::ClearBorders method


Удаляет все границы таблицы и ячеек в этой таблице.

```cpp
void Aspose::Words::Tables::Table::ClearBorders()
```


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


Показывает, как удалить все границы из таблицы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Hello world!");
builder->EndTable();

// Измените цвет и толщину верхней границы.
System::SharedPtr<Aspose::Words::Border> topBorder = table->get_FirstRow()->get_RowFormat()->get_Borders()->idx_get(Aspose::Words::BorderType::Top);
table->SetBorder(Aspose::Words::BorderType::Top, Aspose::Words::LineStyle::Double, 1.5, System::Drawing::Color::get_Red(), true);

ASPOSE_ASSERT_EQ(1.5, topBorder->get_LineWidth());
ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), topBorder->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::LineStyle::Double, topBorder->get_LineStyle());

// Очистите границы всех ячеек в таблице, а затем сохраните документ.
table->ClearBorders();
doc->Save(get_ArtifactsDir() + u"Table.ClearBorders.docx");

// Проверьте значения свойств таблицы после повторного открытия документа.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Table.ClearBorders.docx");
table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
topBorder = table->get_FirstRow()->get_RowFormat()->get_Borders()->idx_get(Aspose::Words::BorderType::Top);

ASPOSE_ASSERT_EQ(0.0, topBorder->get_LineWidth());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), topBorder->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::LineStyle::None, topBorder->get_LineStyle());
```

## См. также

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
