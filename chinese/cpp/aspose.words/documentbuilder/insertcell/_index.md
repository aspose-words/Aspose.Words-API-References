---
title: "Aspose::Words::DocumentBuilder::InsertCell 方法"
linktitle: "InsertCell"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::InsertCell 方法。 在 C++ 中向文档插入表格单元格。"
type: docs
weight: 29000
url: /zh/cpp/aspose.words/documentbuilder/insertcell/
---
## DocumentBuilder::InsertCell method


在文档中插入表格单元格。

```cpp
System::SharedPtr<Aspose::Words::Tables::Cell> Aspose::Words::DocumentBuilder::InsertCell()
```


### ReturnValue

刚刚插入的单元格节点。
## 备注


要开始表格，只需调用 [InsertCell](./)。之后，使用 [DocumentBuilder](../) 类的其他方法添加的任何内容都将被添加到当前单元格。

要在同一行开始新单元格，请再次调用 [InsertCell](./)。

要结束表格行，请调用 [EndRow](../endrow/)。

使用 [CellFormat](../get_cellformat/) 属性来指定单元格格式。

## 示例



展示如何使用自定义边框构建表格。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// 为文档生成器设置表格格式选项
// 它们将应用于我们使用它添加的每一行和每个单元格。
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// 更改格式将应用于当前单元格，
// 以及随后使用生成器创建的任何新单元格。
// 这不会影响我们之前添加的单元格。
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// 增加行高以适应竖排文本。
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTable.docx");
```


展示如何使用文档生成器创建表格。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 开始表格，然后用两个单元格填充第一行。
builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");

// 调用生成器的 "EndRow" 方法以开始新行。
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateTable.docx");
```

## 另见

* Class [Cell](../../../aspose.words.tables/cell/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
