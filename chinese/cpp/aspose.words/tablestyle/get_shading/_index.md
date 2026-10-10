---
title: "Aspose::Words::TableStyle::get_Shading 方法"
linktitle: "get_Shading"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TableStyle::get_Shading 方法。获取一个 Shading 对象，该对象引用 C++ 中表格单元格的阴影格式。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words/tablestyle/get_shading/
---
## TableStyle::get_Shading method


获取一个 [Shading](../../shading/) 对象，该对象引用表格单元格的阴影格式。

```cpp
System::SharedPtr<Aspose::Words::Shading> Aspose::Words::TableStyle::get_Shading()
```


## 示例



展示如何为表格创建自定义样式设置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Name");
builder->InsertCell();
builder->Write(u"مرحبًا");
builder->EndRow();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_AllowBreakAcrossPages(true);
tableStyle->set_CellSpacing(5);
tableStyle->set_BottomPadding(20);
tableStyle->set_LeftPadding(5);
tableStyle->set_RightPadding(10);
tableStyle->set_TopPadding(20);
tableStyle->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AntiqueWhite());
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DotDash);
tableStyle->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);

table->set_Style(tableStyle);

// 设置表格的样式属性可能会影响表格本身的属性。
ASSERT_FALSE(table->get_Bidi());
ASPOSE_ASSERT_EQ(5.0, table->get_CellSpacing());
ASSERT_EQ(u"MyTableStyle1", table->get_StyleName());

doc->Save(get_ArtifactsDir() + u"Table.TableStyleCreation.docx");
```

## 另见

* Class [Shading](../../shading/)
* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
