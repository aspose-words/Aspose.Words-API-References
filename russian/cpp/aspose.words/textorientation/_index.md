---
title: "Aspose::Words::TextOrientation enum"
linktitle: "TextOrientation"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::TextOrientation enum. Указывает ориентацию текста на странице, в ячейке таблицы или в текстовом кадре в C++."
type: docs
weight: 124000
url: /ru/cpp/aspose.words/textorientation/
---
## TextOrientation enum


Указывает ориентацию текста на странице, в ячейке таблицы или в текстовом фрейме.

```cpp
enum class TextOrientation
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Горизонтальная | 0 | Текст располагается горизонтально (lr-tb). |
| Вниз | 1 | Текст повернут на 90 градусов вправо, чтобы отображаться сверху вниз (tb-rl). |
| Вверх | 3 | Текст повернут на 90 градусов влево, чтобы отображаться снизу вверх (bt-lr). |
| HorizontalRotatedFarEast | 4 | Текст располагается горизонтально, но символы Far East повернуты на 90 градусов влево (lr-tb-v). |
| VerticalFarEast | 5 | Символы Дальнего Востока отображаются вертикально, остальной текст вращается на 90 градусов вправо, чтобы отображаться сверху вниз (tb-rl-v). |
| VerticalRotatedFarEast | 7 | Символы Дальнего Востока отображаются вертикально, остальной текст вращается на 90 градусов вправо, чтобы отображаться сверху вниз вертикально, затем слева направо горизонтально (tb-lr-v). |


## Примеры



Показывает, как построить отформатированную таблицу 2x2.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();

// Во время построения таблицы документный построитель применит текущие значения свойств RowFormat/CellFormat.
// к текущей строке/ячейке, в которой находится курсор, и к любым новым строкам/ячейкам при их создании.
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(0)->get_CellFormat()->get_VerticalAlignment());
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(1)->get_CellFormat()->get_VerticalAlignment());

builder->InsertCell();
builder->get_RowFormat()->set_Height(100);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 2, cell 2.");
builder->EndRow();
builder->EndTable();

// Ранее добавленные строки и ячейки не подвергаются ретроспективному изменению из‑за изменений форматирования построителя.
ASPOSE_ASSERT_EQ(0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());
ASPOSE_ASSERT_EQ(100, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::TextOrientation::Upward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation());
ASSERT_EQ(Aspose::Words::TextOrientation::Downward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.BuildTable.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
