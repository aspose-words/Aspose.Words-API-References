---
title: "Classe Aspose::Words::FrameFormat"
linktitle: "FrameFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::FrameFormat. Représente le formatage lié aux cadres pour un paragraphe en C++."
type: docs
weight: 30000
url: /fr/cpp/aspose.words/frameformat/
---
## FrameFormat class


Représente le formatage lié aux cadres pour un paragraphe.

```cpp
class FrameFormat : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Height](./get_height/)() | Obtient la hauteur du cadre spécifié. |
| [get_HeightRule](./get_heightrule/)() | Obtient la règle de détermination de la hauteur du cadre spécifié. |
| [get_HorizontalAlignment](./get_horizontalalignment/)() | Obtient l'alignement horizontal du cadre spécifié. |
| [get_HorizontalDistanceFromText](./get_horizontaldistancefromtext/)() | Obtient la distance horizontale entre un cadre et le texte environnant, en points. |
| [get_HorizontalPosition](./get_horizontalposition/)() | Obtient la distance horizontale entre le bord du cadre et l'élément spécifié par la propriété [RelativeHorizontalPosition](./get_relativehorizontalposition/). |
| [get_IsFrame](./get_isframe/)() | Renvoie **true** si le paragraphe est un cadre. |
| [get_RelativeHorizontalPosition](./get_relativehorizontalposition/)() | Obtient la position horizontale relative d'un cadre. |
| [get_RelativeVerticalPosition](./get_relativeverticalposition/)() | Obtient la position verticale relative d'un cadre. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Obtient l'alignement vertical du cadre spécifié. |
| [get_VerticalDistanceFromText](./get_verticaldistancefromtext/)() | Spécifie la distance verticale (en points) entre un cadre et le texte environnant. |
| [get_VerticalPosition](./get_verticalposition/)() | Obtient la distance verticale entre le bord du cadre et l'élément spécifié par la propriété [RelativeVerticalPosition](./get_relativeverticalposition/). |
| [get_Width](./get_width/)() | Obtient la largeur du cadre spécifié, en points. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Remarques


Cet objet est toujours créé. Si un paragraphe est un cadre, alors toutes les propriétés contiendront leurs valeurs respectives, sinon toutes les propriétés sont définies à leurs valeurs par défaut.

Utilisez [IsFrame](./get_isframe/) pour vérifier si le paragraphe est un cadre.

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
