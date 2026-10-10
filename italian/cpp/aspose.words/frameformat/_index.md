---
title: "classe Aspose::Words::FrameFormat"
linktitle: "FrameFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::FrameFormat. Rappresenta la formattazione relativa al frame per un paragrafo in C++."
type: docs
weight: 30000
url: /it/cpp/aspose.words/frameformat/
---
## FrameFormat class


Rappresenta la formattazione relativa al frame per un paragrafo.

```cpp
class FrameFormat : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Height](./get_height/)() | Restituisce l'altezza del frame specificato. |
| [get_HeightRule](./get_heightrule/)() | Restituisce la regola per determinare l'altezza del frame specificato. |
| [get_HorizontalAlignment](./get_horizontalalignment/)() | Restituisce l'allineamento orizzontale del frame specificato. |
| [get_HorizontalDistanceFromText](./get_horizontaldistancefromtext/)() | Restituisce la distanza orizzontale tra un frame e il testo circostante, in punti. |
| [get_HorizontalPosition](./get_horizontalposition/)() | Restituisce la distanza orizzontale tra il bordo del frame e l'elemento specificato dalla proprietà [RelativeHorizontalPosition](./get_relativehorizontalposition/). |
| [get_IsFrame](./get_isframe/)() | Restituisce **true** se il paragrafo è un frame. |
| [get_RelativeHorizontalPosition](./get_relativehorizontalposition/)() | Restituisce la posizione orizzontale relativa di un frame. |
| [get_RelativeVerticalPosition](./get_relativeverticalposition/)() | Restituisce la posizione verticale relativa di un frame. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Restituisce l'allineamento verticale del frame specificato. |
| [get_VerticalDistanceFromText](./get_verticaldistancefromtext/)() | Specifica la distanza verticale (in punti) tra un frame e il testo circostante. |
| [get_VerticalPosition](./get_verticalposition/)() | Restituisce la distanza verticale tra il bordo del frame e l'elemento specificato dalla proprietà [RelativeVerticalPosition](./get_relativeverticalposition/). |
| [get_Width](./get_width/)() | Restituisce la larghezza del frame specificato, in punti. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Note


Questo oggetto viene sempre creato. Se un paragrafo è un frame, tutte le proprietà conterranno i rispettivi valori; altrimenti tutte le proprietà sono impostate ai valori predefiniti.

Usa [IsFrame](./get_isframe/) per verificare se il paragrafo è un frame.

## Esempi



Mostra come ottenere informazioni sulle proprietà di formattazione dei paragrafi che sono frame.
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

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
