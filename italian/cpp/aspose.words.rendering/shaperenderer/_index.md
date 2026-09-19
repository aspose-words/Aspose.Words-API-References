---
title: "Aspose::Words::Rendering::ShapeRenderer class"
linktitle: "ShapeRenderer"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Rendering::ShapeRenderer class. Fornisce metodi per renderizzare una singola Shape o GroupShape in un'immagine raster o vettoriale o in un oggetto **Graphics**. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.rendering/shaperenderer/
---
## ShapeRenderer class


Fornisce metodi per renderizzare una singola [Shape](../../aspose.words.drawing/shape/) o [GroupShape](../../aspose.words.drawing/groupshape/) in un'immagine raster o vettoriale o in un oggetto **Graphics**. Per saperne di più, visita l'articolo di documentazione [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class ShapeRenderer : public Aspose::Words::Rendering::NodeRendererBase
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_BoundsInPoints](../noderendererbase/get_boundsinpoints/)() const | Restituisce i limiti effettivi della forma in punti. |
| [get_OpaqueBoundsInPoints](../noderendererbase/get_opaqueboundsinpoints/)() | Restituisce i limiti opachi della forma in punti. |
| [get_SizeInPoints](../noderendererbase/get_sizeinpoints/)() | Restituisce le dimensioni effettive della forma in punti. |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float) | Calcola i limiti della forma in pixel per un fattore di zoom e una risoluzione specificati. |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float, float) | Calcola i limiti della forma in pixel per un fattore di zoom e una risoluzione specificati. |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float) | Calcola i limiti opachi della forma in pixel per un fattore di zoom e una risoluzione specificati. |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float, float) | Calcola i limiti opachi della forma in pixel per un fattore di zoom e una risoluzione specificati. |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float) | Calcola le dimensioni della forma in pixel per un fattore di zoom e una risoluzione specificati. |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float, float) | Calcola le dimensioni della forma in pixel per un fattore di zoom e una risoluzione specificati. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeRendererBase](../noderendererbase/noderendererbase/)() |  |
| [RenderToScale](../noderendererbase/rendertoscale/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | Renderizza la forma in un oggetto **Graphics** a una scala specificata. |
| [RenderToSize](../noderendererbase/rendertosize/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | Renderizza la forma in un oggetto **Graphics** a una dimensione specificata. |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Renderizza la forma in un'immagine e la salva in un file. |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Renderizza la forma in un'immagine SVG e la salva in un file. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Renderizza la forma in un'immagine e la salva in uno stream. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Renderizza la forma in un'immagine SVG e la salva in uno stream. |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) |  |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) |  |
| [ShapeRenderer](./shaperenderer/)(const System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\&) | Inizializza una nuova istanza di questa classe. |
| static [Type](./type/)() |  |
## Vedi anche

* Class [NodeRendererBase](../noderendererbase/)
* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
