---
title: "Aspose::Words::FrameFormat Klasse"
linktitle: "FrameFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::FrameFormat Klasse. Stellt rahmenbezogene Formatierung für einen Absatz in C++ dar."
type: docs
weight: 30000
url: /de/cpp/aspose.words/frameformat/
---
## FrameFormat class


Stellt rahmenbezogene Formatierung für einen Absatz dar.

```cpp
class FrameFormat : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Height](./get_height/)() | Ermittelt die Höhe des angegebenen Rahmens. |
| [get_HeightRule](./get_heightrule/)() | Ermittelt die Regel zur Bestimmung der Höhe des angegebenen Rahmens. |
| [get_HorizontalAlignment](./get_horizontalalignment/)() | Ermittelt die horizontale Ausrichtung des angegebenen Rahmens. |
| [get_HorizontalDistanceFromText](./get_horizontaldistancefromtext/)() | Ermittelt den horizontalen Abstand zwischen einem Rahmen und dem umgebenden Text, in Punkten. |
| [get_HorizontalPosition](./get_horizontalposition/)() | Ermittelt den horizontalen Abstand zwischen dem Rand des Rahmens und dem durch die Eigenschaft [RelativeHorizontalPosition](./get_relativehorizontalposition/) angegebenen Element. |
| [get_IsFrame](./get_isframe/)() | Gibt **true** zurück, wenn der Absatz ein Rahmen ist. |
| [get_RelativeHorizontalPosition](./get_relativehorizontalposition/)() | Ermittelt die relative horizontale Position eines Rahmens. |
| [get_RelativeVerticalPosition](./get_relativeverticalposition/)() | Ermittelt die relative vertikale Position eines Rahmens. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Ermittelt die vertikale Ausrichtung des angegebenen Rahmens. |
| [get_VerticalDistanceFromText](./get_verticaldistancefromtext/)() | Gibt den vertikalen Abstand (in Punkten) zwischen einem Rahmen und dem umgebenden Text an. |
| [get_VerticalPosition](./get_verticalposition/)() | Ermittelt den vertikalen Abstand zwischen dem Rand des Rahmens und dem durch die Eigenschaft [RelativeVerticalPosition](./get_relativeverticalposition/) angegebenen Element. |
| [get_Width](./get_width/)() | Ermittelt die Breite des angegebenen Rahmens, in Punkten. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Hinweise


Dieses Objekt wird immer erstellt. Ist ein Absatz ein Rahmen, enthalten alle Eigenschaften die jeweiligen Werte, andernfalls werden alle Eigenschaften auf ihre Standardwerte gesetzt.

Verwenden Sie [IsFrame](./get_isframe/), um zu prüfen, ob ein Absatz ein Rahmen ist.

## Beispiele



Zeigt, wie Informationen zu Formatierungseigenschaften von Absätzen, die Rahmen sind, abgerufen werden.
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

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
