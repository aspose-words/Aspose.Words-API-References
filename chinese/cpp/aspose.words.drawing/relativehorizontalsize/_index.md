---
title: "Aspose::Words::Drawing::RelativeHorizontalSize 枚举"
linktitle: "RelativeHorizontalSize"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::RelativeHorizontalSize 枚举。指定相对于什么在 C++ 中水平计算形状或文本框的宽度。"
type: docs
weight: 33500
url: /zh/cpp/aspose.words.drawing/relativehorizontalsize/
---
## RelativeHorizontalSize enum


指定形状或文本框的宽度在水平上相对于什么进行计算。

```cpp
enum class RelativeHorizontalSize
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 边距 | 0 | 指定宽度是相对于左边距和右边距之间的空间计算的。 |
| Page | 1 | 指定宽度是相对于页面宽度计算的。 |
| LeftMargin | 2 | 指定宽度是相对于左边距区域大小计算的。 |
| RightMargin | 3 | 指定宽度是相对于右边距区域大小计算的。 |
| InnerMargin | 4 | 指定宽度是相对于内侧边距区域大小计算的；奇数页使用左边距区域大小，偶数页使用右边距区域大小。 |
| OuterMargin | 5 | 指定宽度是相对于外侧边距区域大小计算的；奇数页使用右边距区域大小，偶数页使用左边距区域大小。 |
| Default | n/a | 默认值是 [Margin](./)。 |


## 示例



展示如何设置相对大小和位置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 添加一个具有绝对大小和位置的简单形状。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 40);
// 将 WrapType 设置为 WrapType.None，因为 Inline 形状会自动转换为绝对单位。
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// 检查并设置相对水平大小。
if (shape->get_RelativeHorizontalSize() == Aspose::Words::Drawing::RelativeHorizontalSize::Default)
{
    // 将水平大小绑定设置为 Margin。
    shape->set_RelativeHorizontalSize(Aspose::Words::Drawing::RelativeHorizontalSize::Margin);
    // 将宽度设置为 Margin 宽度的 50%。
    shape->set_WidthRelative(50.0f);
}

// 检查并设置相对垂直大小。
if (shape->get_RelativeVerticalSize() == Aspose::Words::Drawing::RelativeVerticalSize::Default)
{
    // 将垂直大小绑定设置为 Margin。
    shape->set_RelativeVerticalSize(Aspose::Words::Drawing::RelativeVerticalSize::Margin);
    // 将高度设置为 Margin 高度的 30%。
    shape->set_HeightRelative(30.0f);
}

// 检查并设置相对垂直位置。
if (shape->get_RelativeVerticalPosition() == Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph)
{
    // 将位置绑定设置为 TopMargin。
    shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin);
    // 将相对顶部设置为顶部边距位置的30%。
    shape->set_TopRelative(30.0f);
}

// 检查并设置相对水平位置。
if (shape->get_RelativeHorizontalPosition() == Aspose::Words::Drawing::RelativeHorizontalPosition::Default)
{
    // 将位置绑定设置为右边距。
    shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin);
    // 位置相对值可以为负数。
    shape->set_LeftRelative(-260.0f);
}

doc->Save(get_ArtifactsDir() + u"Shape.RelativeSizeAndPosition.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
