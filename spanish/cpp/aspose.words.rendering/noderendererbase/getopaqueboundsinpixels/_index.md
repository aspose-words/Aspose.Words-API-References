---
title: "Aspose::Words::Rendering::NodeRendererBase::GetOpaqueBoundsInPixels method"
linktitle: "GetOpaqueBoundsInPixels"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Rendering::NodeRendererBase::GetOpaqueBoundsInPixels method. Calcula los límites opacos de la forma en píxeles para un factor de zoom y una resolución especificados en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/
---
## NodeRendererBase::GetOpaqueBoundsInPixels(float, float) method


Calcula los límites opacos de la forma en píxeles para un factor de zoom y resolución especificados.

```cpp
System::Drawing::Rectangle Aspose::Words::Rendering::NodeRendererBase::GetOpaqueBoundsInPixels(float scale, float dpi)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| scale | float | El factor de zoom (1.0 es 100%). |
| dpi | float | La resolución para convertir de puntos a píxeles (puntos por pulgada). |

### ReturnValue

El rectángulo opaco de la forma en píxeles.
## Observaciones


Este método convierte [OpaqueBoundsInPoints](../get_opaqueboundsinpoints/) en un rectángulo en píxeles y es útil cuando deseas crear un mapa de bits para renderizar la forma con solo la parte opaca de la forma.

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

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::GetOpaqueBoundsInPixels(float, float, float) method


Calcula los límites opacos de la forma en píxeles para un factor de zoom y resolución especificados.

```cpp
System::Drawing::Rectangle Aspose::Words::Rendering::NodeRendererBase::GetOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| scale | float | El factor de zoom (1.0 es 100%). |
| horizontalDpi | float | La resolución horizontal para convertir de puntos a píxeles (puntos por pulgada). |
| verticalDpi | float | La resolución vertical para convertir de puntos a píxeles (puntos por pulgada). |

### ReturnValue

El rectángulo opaco de la forma en píxeles.
## Observaciones


Este método convierte [OpaqueBoundsInPoints](../get_opaqueboundsinpoints/) en un rectángulo en píxeles y es útil cuando deseas crear un mapa de bits para renderizar la forma con solo la parte opaca de la forma.

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

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
