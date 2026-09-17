---
title: "Aspose::Words::FrameFormat::get_RelativeVerticalPosition méthode"
linktitle: "get_RelativeVerticalPosition"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::FrameFormat::get_RelativeVerticalPosition méthode. Obtient la position verticale relative d'un cadre en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words/frameformat/get_relativeverticalposition/
---
## FrameFormat::get_RelativeVerticalPosition method


Obtient la position verticale relative d'un cadre.

```cpp
Aspose::Words::Drawing::RelativeVerticalPosition Aspose::Words::FrameFormat::get_RelativeVerticalPosition()
```


## Exemples



Montre comment obtenir des informations sur les propriétés de mise en forme des paragraphes qui sont des cadres.
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

## Voir aussi

* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Class [FrameFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
