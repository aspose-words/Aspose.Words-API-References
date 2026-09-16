---
title: "Aspose::Words::Tables::AutoFitBehavior 枚举"
linktitle: "AutoFitBehavior"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::AutoFitBehavior 枚举。确定在 C++ 中调用 AutoFit() 方法时 Aspose.Words 如何调整表格大小。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.tables/autofitbehavior/
---
## AutoFitBehavior enum


确定在调用 [AutoFit()](../table/autofit/) 方法时 Aspose.Words 如何调整表格大小。

```cpp
enum class AutoFitBehavior
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| AutoFitToContents | 0 | Aspose.Words 启用 AutoFit 选项，移除表格和所有单元格的首选宽度，然后更新表格布局。在生成的表格中，单元格宽度会更新以适应表格内容。表格很可能会收缩。 |
| AutoFitToWindow | 1 | 使用此值时，Aspose.Words 启用 AutoFit 选项，将表格的首选宽度设置为 100%，移除所有单元格的首选宽度，然后更新表格布局。结果是表格占据所有可用宽度，单元格宽度会更新以适应表格内容。 |
| FixedColumnWidths | 2 | Aspose.Words 禁用 AutoFit 选项并移除表格的首选宽度。单元格的宽度保持为其在 [Width](../cellformat/get_width/) 属性中指定的值。 |


## 示例



展示如何在应用样式的同时构建新表格。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// 在设置任何表格格式之前，必须至少插入一行。
builder->InsertCell();

// 根据样式标识符设置使用的表格样式。
// 请注意，保存为 .doc 格式时并非所有表格样式都可用。
table->set_StyleIdentifier(Aspose::Words::StyleIdentifier::MediumShading1Accent1);

// 基于谓词将样式部分应用于表格的特性，然后构建表格。
table->set_StyleOptions(Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands | Aspose::Words::Tables::TableStyleOptions::FirstRow);
table->AutoFit(Aspose::Words::Tables::AutoFitBehavior::AutoFitToContents);

builder->Writeln(u"Item");
builder->get_CellFormat()->set_RightPadding(40);
builder->InsertCell();
builder->Writeln(u"Quantity (kg)");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Apples");
builder->InsertCell();
builder->Writeln(u"20");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Bananas");
builder->InsertCell();
builder->Writeln(u"40");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Carrots");
builder->InsertCell();
builder->Writeln(u"50");
builder->EndRow();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithStyle.docx");
```


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
