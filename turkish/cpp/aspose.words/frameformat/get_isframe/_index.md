---
title: "Aspose::Words::FrameFormat::get_IsFrame yöntemi"
linktitle: "get_IsFrame"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::FrameFormat::get_IsFrame metodu. Paragraf bir çerçeve ise C++'da true döndürür."
type: docs
weight: 7000
url: /tr/cpp/aspose.words/frameformat/get_isframe/
---
## FrameFormat::get_IsFrame method


Paragraf bir çerçeve ise **true** döndürür.

```cpp
bool Aspose::Words::FrameFormat::get_IsFrame()
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

* Class [FrameFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
