---
title: "Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells метод"
linktitle: "ConvertToHorizontallyMergedCells"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells метод. Преобразует ячейки, объединённые по ширине, в ячейки, объединённые с помощью HorizontalMerge в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table::ConvertToHorizontallyMergedCells method


Преобразует ячейки, объединённые по ширине, в ячейки, объединённые с помощью [HorizontalMerge](../../cellformat/get_horizontalmerge/).

```cpp
void Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells()
```

## Примечания


[Table](../) cells can be horizontally merged either using merge flags [HorizontalMerge](../../cellformat/get_horizontalmerge/) or using cell width [Width](../../cellformat/get_width/).

Когда ячейка таблицы объединена по ширине, свойство [HorizontalMerge](../../cellformat/get_horizontalmerge/) бессмысленно, но иногда наличие флагов объединения более удобно.

Используйте этот метод, чтобы преобразовать ячейки таблицы, объединённые по ширине, в ячейки, объединённые флагами объединения.

## Примеры



Показывает, как преобразовать ячейки, объединённые по ширине, в ячейки, объединённые с помощью CellFormat.HorizontalMerge.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table with merged cells.docx");

// Microsoft Word больше не записывает флаги объединения, вместо этого определяя объединённые ячейки по ширине.
// По умолчанию Aspose.Words определяет только 5 ячеек в строке, и ни одна из них не имеет флага горизонтального объединения,
// хотя в строке было 7 ячеек до выполнения горизонтального объединения.
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_Rows()->idx_get(0);

ASSERT_EQ(5, row->get_Cells()->get_Count());
ASSERT_TRUE(row->get_Cells()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> c)>>([](System::SharedPtr<Aspose::Words::Node> c) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Tables::Cell>(c))->get_CellFormat()->get_HorizontalMerge() == Aspose::Words::Tables::CellMerge::None;
}))));

// Используйте метод "ConvertToHorizontallyMergedCells", чтобы преобразовать горизонтально объединённые ячейки
// по её ширине к ячейке, горизонтально объединённой флагами.
// Теперь у нас 7 ячеек, и некоторые из них имеют значения горизонтального объединения.
table->ConvertToHorizontallyMergedCells();
row = table->get_Rows()->idx_get(0);

ASSERT_EQ(7, row->get_Cells()->get_Count());

ASSERT_EQ(Aspose::Words::Tables::CellMerge::None, row->get_Cells()->idx_get(0)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::First, row->get_Cells()->idx_get(1)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::Previous, row->get_Cells()->idx_get(2)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::None, row->get_Cells()->idx_get(3)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::First, row->get_Cells()->idx_get(4)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::Previous, row->get_Cells()->idx_get(5)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::None, row->get_Cells()->idx_get(6)->get_CellFormat()->get_HorizontalMerge());
```

## См. также

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
