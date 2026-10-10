---
title: "Aspose::Words::BorderCollection::get_Horizontal 方法"
linktitle: "get_Horizontal"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BorderCollection::get_Horizontal 方法。获取在 C++ 中用于单元格之间或相邻段落之间的水平边框。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words/bordercollection/get_horizontal/
---
## BorderCollection::get_Horizontal method


获取用于单元格或相邻段落之间的水平边框。

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::get_Horizontal()
```


## 示例



展示如何将设置应用于段落格式的水平边框。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 为段落创建红色水平边框。之后创建的任何段落都将继承这些边框设置。
System::SharedPtr<Aspose::Words::BorderCollection> borders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();
borders->get_Horizontal()->set_Color(System::Drawing::Color::get_Red());
borders->get_Horizontal()->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
borders->get_Horizontal()->set_LineWidth(3);

// 向文档写入文本，而不在之后创建新段落。
// 由于下面没有段落，水平边框将不可见。
builder->Write(u"Paragraph above horizontal border.");

// 一旦我们添加第二个段落，第一个段落的边框将变得可见。
builder->InsertParagraph();
builder->Write(u"Paragraph below horizontal border.");

doc->Save(get_ArtifactsDir() + u"Border.HorizontalBorders.docx");
```


展示如何将设置应用于表格行格式的垂直边框。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 创建一个具有红色和蓝色内部边框的表格。
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

for (int32_t i = 0; i < 3; i++)
{
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, Column 1", i + 1));
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, Column 2", i + 1));

    System::SharedPtr<Aspose::Words::Tables::Row> row = builder->EndRow();
    System::SharedPtr<Aspose::Words::BorderCollection> borders = row->get_RowFormat()->get_Borders();

    // 调整将在行之间出现的边框外观。
    borders->get_Horizontal()->set_Color(System::Drawing::Color::get_Red());
    borders->get_Horizontal()->set_LineStyle(Aspose::Words::LineStyle::Dot);
    borders->get_Horizontal()->set_LineWidth(2.0);

    // 调整将在单元格之间出现的边框外观。
    borders->get_Vertical()->set_Color(System::Drawing::Color::get_Blue());
    borders->get_Vertical()->set_LineStyle(Aspose::Words::LineStyle::Dot);
    borders->get_Vertical()->set_LineWidth(2.0);
}

// 行格式和单元格内部段落使用不同的边框设置。
System::SharedPtr<Aspose::Words::Border> border = table->get_FirstRow()->get_FirstCell()->get_LastParagraph()->get_ParagraphFormat()->get_Borders()->get_Vertical();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), border->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0.0, border->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::None, border->get_LineStyle());

doc->Save(get_ArtifactsDir() + u"Border.VerticalBorders.docx");
```

## 另见

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
