---
title: "Aspose::Words::FrameFormat::get_HeightRule metodu"
linktitle: "get_HeightRule"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::FrameFormat::get_HeightRule metodu. C++'ta belirtilen çerçevenin yüksekliğini belirleme kuralını alır."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/frameformat/get_heightrule/
---
## FrameFormat::get_HeightRule method


Belirtilen çerçevenin yüksekliğini belirleme kuralını alır.

```cpp
Aspose::Words::HeightRule Aspose::Words::FrameFormat::get_HeightRule()
```


## Örnekler



Çerçeve olan paragrafların biçimlendirme özellikleri hakkında bilgi almanın nasıl yapılacağını gösterir.
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

## Ayrıca Bakınız

* Enum [HeightRule](../../heightrule/)
* Class [FrameFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
