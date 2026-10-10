---
title: "Aspose::Words::Rendering::NodeRendererBase class"
linktitle: "NodeRendererBase"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Rendering::NodeRendererBase class. Classe base per ShapeRenderer e OfficeMathRenderer. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.rendering/noderendererbase/
---
## NodeRendererBase class


Classe base per [ShapeRenderer](../shaperenderer/) e [OfficeMathRenderer](../officemathrenderer/). Per saperne di più, visita l'articolo di documentazione [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class NodeRendererBase : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_BoundsInPoints](./get_boundsinpoints/)() const | Restituisce i limiti effettivi della forma in punti. |
| [get_OpaqueBoundsInPoints](./get_opaqueboundsinpoints/)() | Restituisce i limiti opachi della forma in punti. |
| [get_SizeInPoints](./get_sizeinpoints/)() | Restituisce le dimensioni effettive della forma in punti. |
| [GetBoundsInPixels](./getboundsinpixels/)(float, float) | Calcola i limiti della forma in pixel per un fattore di zoom e una risoluzione specificati. |
| [GetBoundsInPixels](./getboundsinpixels/)(float, float, float) | Calcola i limiti della forma in pixel per un fattore di zoom e una risoluzione specificati. |
| [GetOpaqueBoundsInPixels](./getopaqueboundsinpixels/)(float, float) | Calcola i limiti opachi della forma in pixel per un fattore di zoom e una risoluzione specificati. |
| [GetOpaqueBoundsInPixels](./getopaqueboundsinpixels/)(float, float, float) | Calcola i limiti opachi della forma in pixel per un fattore di zoom e una risoluzione specificati. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float) | Calcola le dimensioni della forma in pixel per un fattore di zoom e una risoluzione specificati. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float, float) | Calcola le dimensioni della forma in pixel per un fattore di zoom e una risoluzione specificati. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeRendererBase](./noderendererbase/)() |  |
| [RenderToScale](./rendertoscale/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | Renderizza la forma in un oggetto **Graphics** a una scala specificata. |
| [RenderToSize](./rendertosize/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | Renderizza la forma in un oggetto **Graphics** a una dimensione specificata. |
| [Save](./save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Renderizza la forma in un'immagine e la salva in un file. |
| [Save](./save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Renderizza la forma in un'immagine SVG e la salva in un file. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Renderizza la forma in un'immagine e la salva in uno stream. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Renderizza la forma in un'immagine SVG e la salva in uno stream. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) |  |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
