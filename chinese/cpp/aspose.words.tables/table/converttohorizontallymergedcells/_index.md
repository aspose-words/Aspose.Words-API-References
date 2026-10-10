---
title: "Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells 方法"
linktitle: "ConvertToHorizontallyMergedCells"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells 方法。将按宽度水平合并的单元格转换为按 HorizontalMerge 合并的单元格（C++）。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table::ConvertToHorizontallyMergedCells method


将按宽度水平合并的单元格转换为按 [HorizontalMerge](../../cellformat/get_horizontalmerge/) 合并的单元格。

```cpp
void Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells()
```

## 备注


[Table](../) cells can be horizontally merged either using merge flags [HorizontalMerge](../../cellformat/get_horizontalmerge/) or using cell width [Width](../../cellformat/get_width/).

当表格单元格通过宽度属性合并时，[HorizontalMerge](../../cellformat/get_horizontalmerge/) 没有意义，但有时使用合并标志更方便。

使用此方法将按宽度水平合并的表格单元格转换为通过合并标志合并的单元格。

## 示例



展示如何将按宽度水平合并的单元格转换为通过 CellFormat.HorizontalMerge 合并的单元格。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table with merged cells.docx");

// Microsoft Word 不再写入合并标志，而是通过宽度定义合并的单元格。
// Aspose.Words 默认在一行中仅定义 5 个单元格，且它们都没有水平合并标志，
// 即使在进行水平合并之前，该行中有 7 个单元格。
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_Rows()->idx_get(0);

ASSERT_EQ(5, row->get_Cells()->get_Count());
ASSERT_TRUE(row->get_Cells()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> c)>>([](System::SharedPtr<Aspose::Words::Node> c) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Tables::Cell>(c))->get_CellFormat()->get_HorizontalMerge() == Aspose::Words::Tables::CellMerge::None;
}))));

// 使用 "ConvertToHorizontallyMergedCells" 方法将水平合并的单元格转换
// 通过其宽度转换为通过标志水平合并的单元格。
// 现在，我们有 7 个单元格，其中一些具有水平合并值。
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

## 另见

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
