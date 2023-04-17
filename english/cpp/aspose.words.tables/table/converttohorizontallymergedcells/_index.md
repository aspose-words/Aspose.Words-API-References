---
title: Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells method
linktitle: ConvertToHorizontallyMergedCells
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells method. Converts cells horizontally merged by width to cells merged by HorizontalMerge in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table::ConvertToHorizontallyMergedCells method


Converts cells horizontally merged by width to cells merged by [HorizontalMerge](../../cellformat/get_horizontalmerge/).

```cpp
void Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells()
```

## Remarks


[Table](../) cells can be horizontally merged either using merge flags [HorizontalMerge](../../cellformat/get_horizontalmerge/) or using cell width [Width](../../cellformat/get_width/).

When table cell is merged by width property [HorizontalMerge](../../cellformat/get_horizontalmerge/) is meaningless but sometimes having merge flags is more convenient way.

Use this method to transforms table cells horizontally merged by width to cells merged by merge flags.

## Examples



Shows how to convert cells horizontally merged by width to cells merged by CellFormat.HorizontalMerge. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Table with merged cells.docx");

// Microsoft Word does not write merge flags anymore, defining merged cells by width instead.
// Aspose.Words by default define only 5 cells in a row, and none of them have the horizontal merge flag,
// even though there were 7 cells in the row before the horizontal merging took place.
SharedPtr<Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
SharedPtr<Row> row = table->get_Rows()->idx_get(0);

ASSERT_EQ(5, row->get_Cells()->get_Count());
auto horizontalMergeIsNone = [](SharedPtr<Node> c)
{
    return (System::DynamicCast<Cell>(c))->get_CellFormat()->get_HorizontalMerge() == CellMerge::None;
};
ASSERT_TRUE(row->get_Cells()->LINQ_All(horizontalMergeIsNone));

// Use the "ConvertToHorizontallyMergedCells" method to convert cells horizontally merged
// by its width to the cell horizontally merged by flags.
// Now, we have 7 cells, and some of them have horizontal merge values.
table->ConvertToHorizontallyMergedCells();
row = table->get_Rows()->idx_get(0);

ASSERT_EQ(7, row->get_Cells()->get_Count());

ASSERT_EQ(CellMerge::None, row->get_Cells()->idx_get(0)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(CellMerge::First, row->get_Cells()->idx_get(1)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(CellMerge::Previous, row->get_Cells()->idx_get(2)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(CellMerge::None, row->get_Cells()->idx_get(3)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(CellMerge::First, row->get_Cells()->idx_get(4)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(CellMerge::Previous, row->get_Cells()->idx_get(5)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(CellMerge::None, row->get_Cells()->idx_get(6)->get_CellFormat()->get_HorizontalMerge());
```

## See Also

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
