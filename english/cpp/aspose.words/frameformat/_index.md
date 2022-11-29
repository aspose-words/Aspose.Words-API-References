---
title: FrameFormat
second_title: Aspose.Words for C++ API Reference
description: Represents frame related formatting for a paragraph.
type: docs
weight: 378
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
| [get_IsFrame](./get_isframe/)() | Returns true if the paragraph is a frame. |
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
auto doc = MakeObject<Document>(MyDir + u"Paragraph frame.docx");

SharedPtr<Paragraph> paragraphFrame = doc->get_FirstSection()->get_Body()->get_Paragraphs()->LINQ_OfType<SharedPtr<Paragraph>>()->LINQ_First(
    [](SharedPtr<Paragraph> p) { return p->get_FrameFormat()->get_IsFrame(); });

ASPOSE_ASSERT_EQ(233.3, paragraphFrame->get_FrameFormat()->get_Width());
ASPOSE_ASSERT_EQ(138.8, paragraphFrame->get_FrameFormat()->get_Height());
ASSERT_EQ(HeightRule::AtLeast, paragraphFrame->get_FrameFormat()->get_HeightRule());
ASSERT_EQ(HorizontalAlignment::Default, paragraphFrame->get_FrameFormat()->get_HorizontalAlignment());
ASSERT_EQ(VerticalAlignment::Default, paragraphFrame->get_FrameFormat()->get_VerticalAlignment());
ASPOSE_ASSERT_EQ(34.05, paragraphFrame->get_FrameFormat()->get_HorizontalPosition());
ASSERT_EQ(RelativeHorizontalPosition::Page, paragraphFrame->get_FrameFormat()->get_RelativeHorizontalPosition());
ASPOSE_ASSERT_EQ(9.0, paragraphFrame->get_FrameFormat()->get_HorizontalDistanceFromText());
ASPOSE_ASSERT_EQ(20.5, paragraphFrame->get_FrameFormat()->get_VerticalPosition());
ASSERT_EQ(RelativeVerticalPosition::Paragraph, paragraphFrame->get_FrameFormat()->get_RelativeVerticalPosition());
ASPOSE_ASSERT_EQ(0.0, paragraphFrame->get_FrameFormat()->get_VerticalDistanceFromText());
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words](../../)
