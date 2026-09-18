---
title: "Aspose::Words::Rendering::ShapeRenderer Klasse"
linktitle: "ShapeRenderer"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Rendering::ShapeRenderer Klasse. Bietet Methoden zum Rendern einer einzelnen Shape oder GroupShape in ein Raster- oder Vektorbild oder in ein **Graphics**-Objekt. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.rendering/shaperenderer/
---
## ShapeRenderer class


Bietet Methoden zum Rendern einer einzelnen [Shape](../../aspose.words.drawing/shape/) oder [GroupShape](../../aspose.words.drawing/groupshape/) in ein Raster- oder Vektorbild oder in ein **Graphics**-Objekt. Weitere Informationen finden Sie im Artikel [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/) der Dokumentation.

```cpp
class ShapeRenderer : public Aspose::Words::Rendering::NodeRendererBase
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
| [RenderToScale](../noderendererbase/rendertoscale/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | Rendert die Form in ein **Graphics**-Objekt zu einem angegebenen Maßstab. |
| [RenderToSize](../noderendererbase/rendertosize/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | Rendert die Form in ein **Graphics**-Objekt mit einer angegebenen Größe. |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Rendert die Form in ein Bild und speichert es in einer Datei. |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Rendert die Form in ein SVG-Bild und speichert es in einer Datei. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Rendert die Form in ein Bild und speichert es in einen Stream. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Rendert die Form in ein SVG-Bild und speichert es in einen Stream. |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) |  |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) |  |
| [ShapeRenderer](./shaperenderer/)(const System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\&) | Initialisiert eine neue Instanz dieser Klasse. |
| static [Type](./type/)() |  |
## Siehe auch

* Class [NodeRendererBase](../noderendererbase/)
* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
