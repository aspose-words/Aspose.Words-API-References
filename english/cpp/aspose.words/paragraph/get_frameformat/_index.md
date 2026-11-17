---
title: Aspose::Words::Paragraph::get_FrameFormat method
linktitle: get_FrameFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Paragraph::get_FrameFormat method. Provides access to the frame formatting properties in C++.'
type: docs
weight: 34000
url: /cpp/aspose.words/paragraph/get_frameformat/
---
## Paragraph::get_FrameFormat method


Provides access to the frame formatting properties.

```cpp
System::SharedPtr<Aspose::Words::FrameFormat> Aspose::Words::Paragraph::get_FrameFormat()
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

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
