---
title: "Aspose::Words::Rendering::NodeRendererBase class"
linktitle: "NodeRendererBase"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Rendering::NodeRendererBase class. Clase base para ShapeRenderer y OfficeMathRenderer. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.rendering/noderendererbase/
---
## NodeRendererBase class


Clase base para [ShapeRenderer](../shaperenderer/) y [OfficeMathRenderer](../officemathrenderer/). Para obtener más información, visite el artículo de documentación [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class NodeRendererBase : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_BoundsInPoints](./get_boundsinpoints/)() const | Obtiene los límites reales de la forma en puntos. |
| [get_OpaqueBoundsInPoints](./get_opaqueboundsinpoints/)() | Obtiene los límites opacos de la forma en puntos. |
| [get_SizeInPoints](./get_sizeinpoints/)() | Obtiene el tamaño real de la forma en puntos. |
| [GetBoundsInPixels](./getboundsinpixels/)(float, float) | Calcula los límites de la forma en píxeles para un factor de zoom y resolución especificados. |
| [GetBoundsInPixels](./getboundsinpixels/)(float, float, float) | Calcula los límites de la forma en píxeles para un factor de zoom y resolución especificados. |
| [GetOpaqueBoundsInPixels](./getopaqueboundsinpixels/)(float, float) | Calcula los límites opacos de la forma en píxeles para un factor de zoom y resolución especificados. |
| [GetOpaqueBoundsInPixels](./getopaqueboundsinpixels/)(float, float, float) | Calcula los límites opacos de la forma en píxeles para un factor de zoom y resolución especificados. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float) | Calcula el tamaño de la forma en píxeles para un factor de zoom y resolución especificados. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float, float) | Calcula el tamaño de la forma en píxeles para un factor de zoom y resolución especificados. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeRendererBase](./noderendererbase/)() |  |
| [RenderToScale](./rendertoscale/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | Renderiza la forma en un objeto **Graphics** a una escala especificada. |
| [RenderToSize](./rendertosize/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | Renderiza la forma en un objeto **Graphics** a un tamaño especificado. |
| [Save](./save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Renderiza la forma en una imagen y la guarda en un archivo. |
| [Save](./save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Renderiza la forma en una imagen SVG y la guarda en un archivo. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Renderiza la forma en una imagen y la guarda en un flujo. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Renderiza la forma en una imagen SVG y la guarda en un flujo. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) |  |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) |  |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo medir y escalar formas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));
auto renderer = System::MakeObject<Aspose::Words::Rendering::OfficeMathRenderer>(officeMath);

// Verifique el tamaño de la imagen que el objeto OfficeMath creará cuando lo rendericemos.
ASSERT_NEAR(122.0f, renderer->get_SizeInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_SizeInPoints().get_Height(), 0.15f);

ASSERT_NEAR(122.0f, renderer->get_BoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_BoundsInPoints().get_Height(), 0.15f);

// Las formas con partes transparentes pueden contener valores diferentes en las propiedades "OpaqueBoundsInPoints".
ASSERT_NEAR(119.5f, renderer->get_OpaqueBoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(14.2f, renderer->get_OpaqueBoundsInPoints().get_Height(), 0.1f);

// Obtenga el tamaño de la forma en píxeles, con escalado lineal a un DPI específico.
System::Drawing::Rectangle bounds = renderer->GetBoundsInPixels(1.0f, 96.0f);
System::String dpi96 = u"DPI 96";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96);
ASSERT_EQ(18, bounds.get_Height()) << (dpi96);

// Obtenga el tamaño de la forma en píxeles, pero con un DPI diferente para las dimensiones horizontal y vertical.
bounds = renderer->GetBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150 = u"DPI 96 150";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96150);
ASSERT_EQ(27, bounds.get_Height()) << (dpi96150);

// Los límites opacos también pueden variar aquí.
bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f);
System::String dpi96Opaque = u"DPI 96 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96Opaque);
ASSERT_EQ(19, bounds.get_Height()) << (dpi96Opaque);

bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150Opaque = u"DPI 96 150 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96150Opaque);
ASSERT_EQ(29, bounds.get_Height()) << (dpi96150Opaque);
```

## Ver también

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
