---
title: "Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell 方法"
linktitle: "get_IsLayoutInCell"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell 方法。获取或设置一个标志，指示形状是在表格内部还是外部显示（在 C++ 中）。"
type: docs
weight: 32000
url: /zh/cpp/aspose.words.drawing/shapebase/get_islayoutincell/
---
## ShapeBase::get_IsLayoutInCell method


获取或设置指示形状是显示在表格内部还是外部的标志。

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell()
```

## 备注


默认值为 **true**。

仅对顶层形状有效，且其属性 [WrapType](../get_wraptype/) 的值设置为非 [Inline](../../../aspose.words/inline/) 时。

## 示例



演示如何确定在表格单元格中显示形状的方式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_BottomPadding(20);
tableStyle->set_LeftPadding(10);
tableStyle->set_RightPadding(10);
tableStyle->set_TopPadding(20);
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Single);

table->set_Style(tableStyle);

builder->MoveTo(table->get_FirstRow()->get_FirstCell()->get_FirstParagraph());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 50, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);

// 将 "IsLayoutInCell" 属性设置为 "true"，以在单元格的段落中将形状显示为内联元素。
// 决定形状位置的坐标原点将是该形状所在单元格的左上角。
// 如果我们重新调整单元格大小，形状将移动以保持从单元格左上角开始的相同位置。
// 将 "IsLayoutInCell" 属性设置为 "false"，以将形状显示为独立的浮动形状。
// 决定形状位置的坐标原点将是页面的左上角，
// 并且该形状不会响应其单元格的任何大小调整。
shape->set_IsLayoutInCell(isLayoutInCell);

// 我们只能将 "IsLayoutInCell" 属性应用于浮动形状。
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

doc->Save(get_ArtifactsDir() + u"Shape.LayoutInTableCell.docx");
```

## 另见

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
