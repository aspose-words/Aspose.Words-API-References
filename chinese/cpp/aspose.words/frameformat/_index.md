---
title: "Aspose::Words::FrameFormat class"
linktitle: "FrameFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::FrameFormat 类。表示 C++ 中段落的框架相关格式设置。"
type: docs
weight: 30000
url: /zh/cpp/aspose.words/frameformat/
---
## FrameFormat class


表示段落的框架相关格式。

```cpp
class FrameFormat : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Height](./get_height/)() | 获取指定框架的高度。 |
| [get_HeightRule](./get_heightrule/)() | 获取确定指定框架高度的规则。 |
| [get_HorizontalAlignment](./get_horizontalalignment/)() | 获取指定框架的水平对齐方式。 |
| [get_HorizontalDistanceFromText](./get_horizontaldistancefromtext/)() | 获取框架与周围文本之间的水平距离（以点为单位）。 |
| [get_HorizontalPosition](./get_horizontalposition/)() | 获取框架边缘与由 [RelativeHorizontalPosition](./get_relativehorizontalposition/) 属性指定的项目之间的水平距离。 |
| [get_IsFrame](./get_isframe/)() | 如果段落是框架，则返回 **true**。 |
| [get_RelativeHorizontalPosition](./get_relativehorizontalposition/)() | 获取框架的相对水平位置。 |
| [get_RelativeVerticalPosition](./get_relativeverticalposition/)() | 获取框架的相对垂直位置。 |
| [get_VerticalAlignment](./get_verticalalignment/)() | 获取指定框架的垂直对齐方式。 |
| [get_VerticalDistanceFromText](./get_verticaldistancefromtext/)() | 指定框架与周围文本之间的垂直距离（以点为单位）。 |
| [get_VerticalPosition](./get_verticalposition/)() | 获取框架边缘与由 [RelativeVerticalPosition](./get_relativeverticalposition/) 属性指定的项目之间的垂直距离。 |
| [get_Width](./get_width/)() | 获取指定框架的宽度（以点为单位）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## 备注


此对象始终被创建。如果段落是框架，则所有属性将包含相应的值，否则所有属性将设置为默认值。

使用 [IsFrame](./get_isframe/) 检查段落是否为框架。

## 示例



展示如何获取框架段落的格式属性信息。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraph frame.docx");

System::SharedPtr<Aspose::Words::Paragraph> paragraphFrame = doc->get_FirstSection()->get_Body()->get_Paragraphs()->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()->LINQ_First(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_FrameFormat()->get_IsFrame();
})));

ASPOSE_ASSERT_EQ(233.3, paragraphFrame->get_FrameFormat()->get_Width());
ASPOSE_ASSERT_EQ(138.8, paragraphFrame->get_FrameFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::AtLeast, paragraphFrame->get_FrameFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::Drawing::HorizontalAlignment::Default, paragraphFrame->get_FrameFormat()->get_HorizontalAlignment());
ASSERT_EQ(Aspose::Words::Drawing::VerticalAlignment::Default, paragraphFrame->get_FrameFormat()->get_VerticalAlignment());
ASPOSE_ASSERT_EQ(34.05, paragraphFrame->get_FrameFormat()->get_HorizontalPosition());
ASSERT_EQ(Aspose::Words::Drawing::RelativeHorizontalPosition::Page, paragraphFrame->get_FrameFormat()->get_RelativeHorizontalPosition());
ASPOSE_ASSERT_EQ(9.0, paragraphFrame->get_FrameFormat()->get_HorizontalDistanceFromText());
ASPOSE_ASSERT_EQ(20.5, paragraphFrame->get_FrameFormat()->get_VerticalPosition());
ASSERT_EQ(Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph, paragraphFrame->get_FrameFormat()->get_RelativeVerticalPosition());
ASPOSE_ASSERT_EQ(0.0, paragraphFrame->get_FrameFormat()->get_VerticalDistanceFromText());
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
