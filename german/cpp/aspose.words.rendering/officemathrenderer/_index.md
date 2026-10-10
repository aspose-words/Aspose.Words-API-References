---
title: "Aspose::Words::Rendering::OfficeMathRenderer Klasse"
linktitle: "OfficeMathRenderer"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Rendering::OfficeMathRenderer Klasse. Stellt Methoden bereit, um ein einzelnes OfficeMath in ein Raster‑ oder Vektorbild oder in ein Graphics‑Objekt zu rendern. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.rendering/officemathrenderer/
---
## OfficeMathRenderer class


Stellt Methoden bereit, um ein einzelnes [OfficeMath](../../aspose.words.math/officemath/) in ein Raster‑ oder Vektorbild oder in ein Graphics‑Objekt zu rendern. Weitere Informationen finden Sie im [Working with OfficeMath](https://docs.aspose.com/words/cpp/working-with-officemath/) Dokumentationsartikel.

```cpp
class OfficeMathRenderer : public Aspose::Words::Rendering::NodeRendererBase
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_BoundsInPoints](../noderendererbase/get_boundsinpoints/)() const | Ermittelt die tatsächlichen Begrenzungen der Form in Punkten. |
| [get_OpaqueBoundsInPoints](../noderendererbase/get_opaqueboundsinpoints/)() | Ermittelt die undurchsichtigen Begrenzungen der Form in Punkten. |
| [get_SizeInPoints](../noderendererbase/get_sizeinpoints/)() | Ermittelt die tatsächliche Größe der Form in Punkten. |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float) | Berechnet die Begrenzungen der Form in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung. |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float, float) | Berechnet die Begrenzungen der Form in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung. |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float) | Berechnet die undurchsichtigen Begrenzungen der Form in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung. |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float, float) | Berechnet die undurchsichtigen Begrenzungen der Form in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung. |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float) | Berechnet die Größe der Form in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung. |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float, float) | Berechnet die Größe der Form in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeRendererBase](../noderendererbase/noderendererbase/)() |  |
| [OfficeMathRenderer](./officemathrenderer/)(const System::SharedPtr\<Aspose::Words::Math::OfficeMath\>\&) | Initialisiert eine neue Instanz dieser Klasse. |
| [RenderToScale](../noderendererbase/rendertoscale/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | Rendert die Form in ein **Graphics**-Objekt zu einem angegebenen Maßstab. |
| [RenderToSize](../noderendererbase/rendertosize/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | Rendert die Form in ein **Graphics**-Objekt mit einer angegebenen Größe. |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Rendert die Form in ein Bild und speichert es in einer Datei. |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Rendert die Form in ein SVG-Bild und speichert es in einer Datei. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Rendert die Form in ein Bild und speichert es in einen Stream. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Rendert die Form in ein SVG-Bild und speichert es in einen Stream. |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) |  |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) |  |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie Formen gemessen und skaliert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));
auto renderer = System::MakeObject<Aspose::Words::Rendering::OfficeMathRenderer>(officeMath);

// Überprüfen Sie die Größe des Bildes, das das OfficeMath-Objekt erstellt, wenn wir es rendern.
ASSERT_NEAR(122.0f, renderer->get_SizeInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_SizeInPoints().get_Height(), 0.15f);

ASSERT_NEAR(122.0f, renderer->get_BoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_BoundsInPoints().get_Height(), 0.15f);

// Formen mit transparenten Teilen können unterschiedliche Werte in den \"OpaqueBoundsInPoints\"-Eigenschaften enthalten.
ASSERT_NEAR(119.5f, renderer->get_OpaqueBoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(14.2f, renderer->get_OpaqueBoundsInPoints().get_Height(), 0.1f);

// Ermitteln Sie die Formgröße in Pixeln mit linearer Skalierung auf eine bestimmte DPI.
System::Drawing::Rectangle bounds = renderer->GetBoundsInPixels(1.0f, 96.0f);
System::String dpi96 = u"DPI 96";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96);
ASSERT_EQ(18, bounds.get_Height()) << (dpi96);

// Ermitteln Sie die Formgröße in Pixeln, jedoch mit einer anderen DPI für die horizontale und vertikale Dimension.
bounds = renderer->GetBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150 = u"DPI 96 150";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96150);
ASSERT_EQ(27, bounds.get_Height()) << (dpi96150);

// Die undurchsichtigen Begrenzungen können hier ebenfalls variieren.
bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f);
System::String dpi96Opaque = u"DPI 96 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96Opaque);
ASSERT_EQ(19, bounds.get_Height()) << (dpi96Opaque);

bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150Opaque = u"DPI 96 150 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96150Opaque);
ASSERT_EQ(29, bounds.get_Height()) << (dpi96150Opaque);
```

## Siehe auch

* Class [NodeRendererBase](../noderendererbase/)
* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
