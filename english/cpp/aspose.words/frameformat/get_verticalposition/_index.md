---
title: Aspose::Words::FrameFormat::get_VerticalPosition method
linktitle: get_VerticalPosition
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::FrameFormat::get_VerticalPosition method. Gets vertical distance between the edge of the frame and the item specified by the RelativeVerticalPosition property in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words/frameformat/get_verticalposition/
---
## FrameFormat::get_VerticalPosition method


Gets vertical distance between the edge of the frame and the item specified by the [RelativeVerticalPosition](../get_relativeverticalposition/) property.

```cpp
double Aspose::Words::FrameFormat::get_VerticalPosition()
```

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

* Class [FrameFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
