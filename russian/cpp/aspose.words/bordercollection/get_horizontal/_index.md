---
title: "Aspose::Words::BorderCollection::get_Horizontal метод"
linktitle: "get_Horizontal"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::BorderCollection::get_Horizontal метод. Получает горизонтальную границу, используемую между ячейками или согласованными абзацами в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words/bordercollection/get_horizontal/
---
## BorderCollection::get_Horizontal method


Получает горизонтальную границу, используемую между ячейками или соответствующими абзацами.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::get_Horizontal()
```


## Примеры



Показывает, как применить настройки к горизонтальным границам в формате абзаца.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте красную горизонтальную границу для абзаца. Любые абзацы, созданные позже, унаследуют эти настройки границы.
System::SharedPtr<Aspose::Words::BorderCollection> borders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();
borders->get_Horizontal()->set_Color(System::Drawing::Color::get_Red());
borders->get_Horizontal()->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
borders->get_Horizontal()->set_LineWidth(3);

// Запишите текст в документ без создания нового абзаца после этого.
// Поскольку под ним нет абзаца, горизонтальная граница не будет видна.
builder->Write(u"Paragraph above horizontal border.");

// После добавления второго абзаца граница первого абзаца станет видимой.
builder->InsertParagraph();
builder->Write(u"Paragraph below horizontal border.");

doc->Save(get_ArtifactsDir() + u"Border.HorizontalBorders.docx");
```


Показывает, как применить настройки к вертикальным границам в формате строки таблицы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте таблицу с красными и синими внутренними границами.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

for (int32_t i = 0; i < 3; i++)
{
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, Column 1", i + 1));
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, Column 2", i + 1));

    System::SharedPtr<Aspose::Words::Tables::Row> row = builder->EndRow();
    System::SharedPtr<Aspose::Words::BorderCollection> borders = row->get_RowFormat()->get_Borders();

    // Настройте внешний вид границ, которые будут отображаться между строками.
    borders->get_Horizontal()->set_Color(System::Drawing::Color::get_Red());
    borders->get_Horizontal()->set_LineStyle(Aspose::Words::LineStyle::Dot);
    borders->get_Horizontal()->set_LineWidth(2.0);

    // Настройте внешний вид границ, которые будут отображаться между ячейками.
    borders->get_Vertical()->set_Color(System::Drawing::Color::get_Blue());
    borders->get_Vertical()->set_LineStyle(Aspose::Words::LineStyle::Dot);
    borders->get_Vertical()->set_LineWidth(2.0);
}

// Формат строки и внутренний абзац ячейки используют разные настройки границ.
System::SharedPtr<Aspose::Words::Border> border = table->get_FirstRow()->get_FirstCell()->get_LastParagraph()->get_ParagraphFormat()->get_Borders()->get_Vertical();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), border->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0.0, border->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::None, border->get_LineStyle());

doc->Save(get_ArtifactsDir() + u"Border.VerticalBorders.docx");
```

## См. также

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
