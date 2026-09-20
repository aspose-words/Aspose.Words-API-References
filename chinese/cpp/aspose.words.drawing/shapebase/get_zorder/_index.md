---
title: "Aspose::Words::Drawing::ShapeBase::get_ZOrder 方法"
linktitle: "get_ZOrder"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_ZOrder 方法。确定在 C++ 中重叠形状的显示顺序。"
type: docs
weight: 57000
url: /zh/cpp/aspose.words.drawing/shapebase/get_zorder/
---
## ShapeBase::get_ZOrder method


确定重叠形状的显示顺序。

```cpp
int32_t Aspose::Words::Drawing::ShapeBase::get_ZOrder()
```

## 备注


仅对顶层形状有效。

默认值为 0。

该数字表示堆叠优先级。数字较高的形状将显示为覆盖（位于）数字较低的形状前面。

在文档的页眉和正文中的形状，其重叠顺序相互独立。

组形状中子形状的显示顺序由它们在组形状内部的顺序决定。

## 示例



展示如何操作形状的顺序。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入三个不同颜色的矩形，使它们部分重叠。
// 当我们插入一个与另一个形状重叠的形状时，Aspose.Words 会将较新的形状放在较旧的形状之上。
// 浅绿色矩形将覆盖浅蓝色矩形，并部分遮挡它，
// 并且浅蓝色矩形会遮挡橙色矩形。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_Orange());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 150, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 150, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 200, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 200, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_LightGreen());

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

// 形状的 "ZOrder" 属性决定其在其他重叠形状中的堆叠优先级。
// 如果两个重叠的形状具有不同的 "ZOrder" 值，
// Microsoft Word 会将具有更高值的形状放在具有较低值的形状之上。
// 设置我们形状的 "ZOrder" 值，以将第一个橙色矩形放在第二个浅蓝色矩形之上
// 并将第二个浅蓝色矩形放在第三个浅绿色矩形之上。
// 这将颠倒它们原来的堆叠顺序。
shapes[0]->set_ZOrder(3);
shapes[1]->set_ZOrder(2);
shapes[2]->set_ZOrder(1);

doc->Save(get_ArtifactsDir() + u"Shape.ZOrder.docx");
```

## 另见

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
