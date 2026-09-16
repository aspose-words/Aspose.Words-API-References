---
title: "Aspose::Words::Drawing::ShapeBase::get_IsInline 方法"
linktitle: "get_IsInline"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_IsInline 方法。快速判断此形状在 C++ 中是否与文本内联定位。"
type: docs
weight: 30000
url: /zh/cpp/aspose.words.drawing/shapebase/get_isinline/
---
## ShapeBase::get_IsInline method


一种快速判断此形状是否与文本内联定位的方法。

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsInline()
```

## 备注


仅对顶层形状有效。

## 示例



展示如何判断形状是内联还是浮动。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 以下是形状可能具有的两种环绕类型。
// 1 -  内联：
builder->Write(u"Hello world! ");
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);
shape->set_FillColor(System::Drawing::Color::get_LightBlue());
builder->Write(u" Hello again.");

// 内联形状位于段落内部，与其他段落元素（例如文本运行）一起。
// 在 Microsoft Word 中，我们可以像对待字符一样点击并拖动形状到任意段落。
// 如果形状较大，它会影响段落的垂直间距。
// 我们无法将此形状移动到没有段落的地方。
ASSERT_EQ(Aspose::Words::Drawing::WrapType::Inline, shape->get_WrapType());
ASSERT_TRUE(shape->get_IsInline());

// 2 -  浮动：
shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 200, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 200, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_Orange());

// 浮动形状属于我们插入它的段落，
// 我们可以通过点击形状时出现的锚点符号来确定。
// 如果形状左侧没有可见的锚点符号，
// 我们需要通过 \"Options\" -> \"Display\" -> \"Object Anchors\" 来启用可见锚点。
// 在 Microsoft Word 中，我们可以左键点击并自由拖动此形状到任意位置。
ASSERT_EQ(Aspose::Words::Drawing::WrapType::None, shape->get_WrapType());
ASSERT_FALSE(shape->get_IsInline());

doc->Save(get_ArtifactsDir() + u"Shape.IsInline.docx");
```

## 另见

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
