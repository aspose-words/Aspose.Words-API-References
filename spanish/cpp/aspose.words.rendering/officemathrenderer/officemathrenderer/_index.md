---
title: "Constructor Aspose::Words::Rendering::OfficeMathRenderer::OfficeMathRenderer"
linktitle: "OfficeMathRenderer"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Constructor Aspose::Words::Rendering::OfficeMathRenderer::OfficeMathRenderer. Inicializa una nueva instancia de esta clase en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.rendering/officemathrenderer/officemathrenderer/
---
## OfficeMathRenderer::OfficeMathRenderer constructor


Inicializa una nueva instancia de esta clase.

```cpp
Aspose::Words::Rendering::OfficeMathRenderer::OfficeMathRenderer(const System::SharedPtr<Aspose::Words::Math::OfficeMath> &math)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| math | const System::SharedPtr\<Aspose::Words::Math::OfficeMath\>\& | El objeto [OfficeMath](../../../aspose.words.math/officemath/) que deseas renderizar. |

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

* Class [OfficeMath](../../../aspose.words.math/officemath/)
* Class [OfficeMathRenderer](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
