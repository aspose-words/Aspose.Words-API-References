---
title: "Aspose::Words::Rendering::NodeRendererBase::get_BoundsInPoints method"
linktitle: "get_BoundsInPoints"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Rendering::NodeRendererBase::get_BoundsInPoints method. Ottiene i limiti reali della forma in punti in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.rendering/noderendererbase/get_boundsinpoints/
---
## NodeRendererBase::get_BoundsInPoints method


Restituisce i limiti effettivi della forma in punti.

```cpp
System::Drawing::RectangleF Aspose::Words::Rendering::NodeRendererBase::get_BoundsInPoints() const
```

## Note


Questa proprietà restituisce l'area di delimitazione reale (come renderizzata nella pagina) della forma. I limiti tengono conto della rotazione della forma (se presente).

## Esempi



Mostra come misurare e scalare le forme.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));
auto renderer = System::MakeObject<Aspose::Words::Rendering::OfficeMathRenderer>(officeMath);

// Verifica le dimensioni dell'immagine che l'oggetto OfficeMath creerà quando la renderizziamo.
ASSERT_NEAR(122.0f, renderer->get_SizeInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_SizeInPoints().get_Height(), 0.15f);

ASSERT_NEAR(122.0f, renderer->get_BoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_BoundsInPoints().get_Height(), 0.15f);

// Le forme con parti trasparenti possono contenere valori diversi nella proprietà "OpaqueBoundsInPoints".
ASSERT_NEAR(119.5f, renderer->get_OpaqueBoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(14.2f, renderer->get_OpaqueBoundsInPoints().get_Height(), 0.1f);

// Ottieni le dimensioni della forma in pixel, con scala lineare a una DPI specifica.
System::Drawing::Rectangle bounds = renderer->GetBoundsInPixels(1.0f, 96.0f);
System::String dpi96 = u"DPI 96";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96);
ASSERT_EQ(18, bounds.get_Height()) << (dpi96);

// Ottieni le dimensioni della forma in pixel, ma con una DPI diversa per le dimensioni orizzontali e verticali.
bounds = renderer->GetBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150 = u"DPI 96 150";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96150);
ASSERT_EQ(27, bounds.get_Height()) << (dpi96150);

// I limiti opachi possono variare anche qui.
bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f);
System::String dpi96Opaque = u"DPI 96 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96Opaque);
ASSERT_EQ(19, bounds.get_Height()) << (dpi96Opaque);

bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150Opaque = u"DPI 96 150 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96150Opaque);
ASSERT_EQ(29, bounds.get_Height()) << (dpi96150Opaque);
```

## Vedi anche

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
