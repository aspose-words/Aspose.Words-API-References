---
title: Aspose::Words::FrameFormat class
linktitle: FrameFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::FrameFormat class. Represents frame related formatting for a paragraph in C++.'
type: docs
weight: 30000
url: /cpp/aspose.words/frameformat/
---
## FrameFormat class


Represents frame related formatting for a paragraph.

```cpp
class FrameFormat : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_Height](./get_height/)() | Gets the height of the specified frame. |
| [get_HeightRule](./get_heightrule/)() | Gets the rule for determining the height of the specified frame. |
| [get_HorizontalAlignment](./get_horizontalalignment/)() | Gets horizontal alignment of the specified frame. |
| [get_HorizontalDistanceFromText](./get_horizontaldistancefromtext/)() | Gets horizontal distance between a frame and the surrounding text, in points. |
| [get_HorizontalPosition](./get_horizontalposition/)() | Gets horizontal distance between the edge of the frame and the item specified by the [RelativeHorizontalPosition](./get_relativehorizontalposition/) property. |
| [get_IsFrame](./get_isframe/)() | Returns **true** if the paragraph is a frame. |
| [get_RelativeHorizontalPosition](./get_relativehorizontalposition/)() | Gets the relative horizontal position of a frame. |
| [get_RelativeVerticalPosition](./get_relativeverticalposition/)() | Gets the relative vertical position of a frame. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Gets vertical alignment of the specified frame. |
| [get_VerticalDistanceFromText](./get_verticaldistancefromtext/)() | Specifies vertical distance (in points) between a frame and the surrounding text. |
| [get_VerticalPosition](./get_verticalposition/)() | Gets vertical distance between the edge of the frame and the item specified by the [RelativeVerticalPosition](./get_relativeverticalposition/) property. |
| [get_Width](./get_width/)() | Gets the width of the specified frame, in points. |
## Remarks


This object is always created. If a paragraph is a frame, then all properties will contain respective values, otherwise all properties are set to their defaults.

Use [IsFrame](./get_isframe/) to check whether paragraph is a frame.
## Examples


Shows how to get information about formatting properties of paragraphs that are frames.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Paragraph frame.docx"));

System::SharedPtr<Aspose::Words::Paragraph> paragraphFrame = doc->get_FirstSection()->get_Body()->get_Paragraphs()->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph>>()->LINQ_First(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_FrameFormat()->get_IsFrame();
})));

ASPOSE_ASSERT_EQ(paragraphFrame->get_FrameFormat()->get_Width(), 233.3);
ASPOSE_ASSERT_EQ(paragraphFrame->get_FrameFormat()->get_Height(), 138.8);
ASSERT_EQ(paragraphFrame->get_FrameFormat()->get_HeightRule(), HeightRule::AtLeast);
ASSERT_EQ(paragraphFrame->get_FrameFormat()->get_HorizontalAlignment(), HorizontalAlignment::Default);
ASSERT_EQ(paragraphFrame->get_FrameFormat()->get_VerticalAlignment(), VerticalAlignment::Default);
ASPOSE_ASSERT_EQ(paragraphFrame->get_FrameFormat()->get_HorizontalPosition(), 34.05);
ASSERT_EQ(paragraphFrame->get_FrameFormat()->get_RelativeHorizontalPosition(), RelativeHorizontalPosition::Page);
ASPOSE_ASSERT_EQ(paragraphFrame->get_FrameFormat()->get_HorizontalDistanceFromText(), 9.0);
ASPOSE_ASSERT_EQ(paragraphFrame->get_FrameFormat()->get_VerticalPosition(), 20.5);
ASSERT_EQ(paragraphFrame->get_FrameFormat()->get_RelativeVerticalPosition(), RelativeVerticalPosition::Paragraph);
ASPOSE_ASSERT_EQ(paragraphFrame->get_FrameFormat()->get_VerticalDistanceFromText(), 0.0);
```
## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
