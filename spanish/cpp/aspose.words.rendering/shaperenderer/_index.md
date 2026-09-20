---
title: "Aspose::Words::Rendering::ShapeRenderer class"
linktitle: "ShapeRenderer"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Rendering::ShapeRenderer class. Proporciona métodos para renderizar una Shape o GroupShape individual a una imagen raster o vectorial o a un objeto Graphics. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.rendering/shaperenderer/
---
## ShapeRenderer class


Proporciona métodos para renderizar una [Shape](../../aspose.words.drawing/shape/) o [GroupShape](../../aspose.words.drawing/groupshape/) individual a una imagen raster o vectorial o a un objeto Graphics. Para obtener más información, visite el artículo de documentación [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class ShapeRenderer : public Aspose::Words::Rendering::NodeRendererBase
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_BoundsInPoints](../noderendererbase/get_boundsinpoints/)() const | Obtiene los límites reales de la forma en puntos. |
| [get_OpaqueBoundsInPoints](../noderendererbase/get_opaqueboundsinpoints/)() | Obtiene los límites opacos de la forma en puntos. |
| [get_SizeInPoints](../noderendererbase/get_sizeinpoints/)() | Obtiene el tamaño real de la forma en puntos. |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float) | Calcula los límites de la forma en píxeles para un factor de zoom y resolución especificados. |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float, float) | Calcula los límites de la forma en píxeles para un factor de zoom y resolución especificados. |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float) | Calcula los límites opacos de la forma en píxeles para un factor de zoom y resolución especificados. |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float, float) | Calcula los límites opacos de la forma en píxeles para un factor de zoom y resolución especificados. |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float) | Calcula el tamaño de la forma en píxeles para un factor de zoom y resolución especificados. |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float, float) | Calcula el tamaño de la forma en píxeles para un factor de zoom y resolución especificados. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeRendererBase](../noderendererbase/noderendererbase/)() |  |
| [RenderToScale](../noderendererbase/rendertoscale/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | Renderiza la forma en un objeto **Graphics** a una escala especificada. |
| [RenderToSize](../noderendererbase/rendertosize/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | Renderiza la forma en un objeto **Graphics** a un tamaño especificado. |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Renderiza la forma en una imagen y la guarda en un archivo. |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Renderiza la forma en una imagen SVG y la guarda en un archivo. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Renderiza la forma en una imagen y la guarda en un flujo. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Renderiza la forma en una imagen SVG y la guarda en un flujo. |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) |  |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) |  |
| [ShapeRenderer](./shaperenderer/)(const System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\&) | Inicializa una nueva instancia de esta clase. |
| static [Type](./type/)() |  |
## Ver también

* Class [NodeRendererBase](../noderendererbase/)
* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
