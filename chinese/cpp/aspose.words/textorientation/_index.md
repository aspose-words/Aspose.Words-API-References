---
title: "Aspose::Words::TextOrientation 枚举"
linktitle: "TextOrientation"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TextOrientation 枚举。指定页面、表格单元格或 C++ 中文本框中文本的方向。"
type: docs
weight: 124000
url: /zh/cpp/aspose.words/textorientation/
---
## TextOrientation enum


指定页面上、表格单元格中或文本框中的文本方向。

```cpp
enum class TextOrientation
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Horizontal | 0 | 文本水平排列 (lr-tb)。 |
| 向下 | 1 | 文本向右旋转 90 度，以从上到下显示 (tb-rl)。 |
| 向上 | 3 | 文本向左旋转 90 度，以从下到上显示 (bt-lr)。 |
| HorizontalRotatedFarEast | 4 | 文本水平排列，但东亚字符向左旋转 90 度 (lr-tb-v)。 |
| VerticalFarEast | 5 | 东亚字符垂直显示，其他文本向右旋转 90 度，以从上到下显示 (tb-rl-v)。 |
| VerticalRotatedFarEast | 7 | 东亚字符垂直显示，其他文本向右旋转 90 度，以从上到下垂直显示，然后水平从左到右排列 (tb-lr-v)。 |


## 示例



展示如何构建一个格式化的 2x2 表格。
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

// 在构建表格时，文档生成器将把其当前的 RowFormat/CellFormat 属性值应用于
// 光标所在的当前行/单元格以及在创建时的任何新行/单元格。
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

// 先前添加的行和单元格不会因构建器格式的更改而被追溯影响。
ASPOSE_ASSERT_EQ(0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());
ASPOSE_ASSERT_EQ(100, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::TextOrientation::Upward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation());
ASSERT_EQ(Aspose::Words::TextOrientation::Downward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.BuildTable.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
