---
title: "Aspose::Words::BorderCollection::get_Right 方法"
linktitle: "get_Right"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BorderCollection::get_Right 方法。获取 C++ 中的右边框。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words/bordercollection/get_right/
---
## BorderCollection::get_Right method


获取右侧边框。

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::get_Right()
```


## 示例



展示如何在构建表格时应用边框和阴影颜色。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 开始一个表格并为其边框设置默认颜色/粗细。
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
table->SetBorders(Aspose::Words::LineStyle::Single, 2.0, System::Drawing::Color::get_Black());

// 创建一行，其中两个单元格具有不同的背景颜色。
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSkyBlue());
builder->Writeln(u"Row 1, Cell 1.");
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());
builder->Writeln(u"Row 1, Cell 2.");
builder->EndRow();

// 重置单元格格式以禁用背景颜色
// 为构建器创建的所有新单元格设置自定义边框粗细，
// 然后构建第二行。
builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->get_Borders()->get_Left()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Right()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Top()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Bottom()->set_LineWidth(4.0);

builder->InsertCell();
builder->Writeln(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Writeln(u"Row 2, Cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.TableBordersAndShading.docx");
```

## 另见

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
