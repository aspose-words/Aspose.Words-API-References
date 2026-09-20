---
title: "Aspose::Words::DocumentBuilder::get_ParagraphFormat 方法"
linktitle: "get_ParagraphFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::get_ParagraphFormat 方法。返回一个对象，表示 C++ 中当前段落格式属性。"
type: docs
weight: 24000
url: /zh/cpp/aspose.words/documentbuilder/get_paragraphformat/
---
## DocumentBuilder::get_ParagraphFormat method


返回表示当前段落格式属性的对象。

```cpp
System::SharedPtr<Aspose::Words::ParagraphFormat> Aspose::Words::DocumentBuilder::get_ParagraphFormat()
```


## 示例



展示如何使用 [DocumentBuilder](../) 创建格式化表格。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
table->set_LeftIndent(20);

// 设置一些文本和表格外观的格式选项。
builder->get_RowFormat()->set_Height(40);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::AtLeast);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::FromArgb(198, 217, 241));

builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->get_Font()->set_Size(16);
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Bold(true);

// 在文档生成器中配置格式选项将会应用它们
// 到光标所在的当前单元格/行，
// 以及使用该生成器创建的任何新单元格和行。
builder->Write(u"Header Row,\n Cell 1");
builder->InsertCell();
builder->Write(u"Header Row,\n Cell 2");
builder->InsertCell();
builder->Write(u"Header Row,\n Cell 3");
builder->EndRow();

// 重新配置生成器的格式对象，以便用于即将创建的新行和单元格。
// 生成器不会将这些应用于已创建的第一行，以使其突出显示为标题行。
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_White());
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_RowFormat()->set_Height(30);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Auto);
builder->InsertCell();
builder->get_Font()->set_Size(12);
builder->get_Font()->set_Bold(false);

builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 3.");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 3.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateFormattedTable.docx");
```

## 另见

* Class [ParagraphFormat](../../paragraphformat/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
