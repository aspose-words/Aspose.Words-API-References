---
title: "Aspose::Words::Tables::CellVerticalAlignment 枚举"
linktitle: "CellVerticalAlignment"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::CellVerticalAlignment 枚举。指定 C++ 中表格单元格内文本的垂直对齐方式。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.tables/cellverticalalignment/
---
## CellVerticalAlignment enum


指定表格单元格内文本的垂直对齐方式。

```cpp
enum class CellVerticalAlignment
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 顶部 | 0 | 文本对齐在单元格的顶部。 |
| 居中 | 1 | 文本对齐在单元格的中部。 |
| 底部 | 2 | 文本对齐在单元格的底部。 |


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
