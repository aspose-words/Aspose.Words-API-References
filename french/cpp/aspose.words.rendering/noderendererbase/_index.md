---
title: "Aspose::Words::Rendering::NodeRendererBase class"
linktitle: "NodeRendererBase"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Rendering::NodeRendererBase class. Classe de base pour ShapeRenderer et OfficeMathRenderer. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.rendering/noderendererbase/
---
## NodeRendererBase class


Classe de base pour [ShapeRenderer](../shaperenderer/) et [OfficeMathRenderer](../officemathrenderer/). Pour en savoir plus, consultez l'article de documentation [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class NodeRendererBase : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_BoundsInPoints](./get_boundsinpoints/)() const | Obtient les limites réelles de la forme en points. |
| [get_OpaqueBoundsInPoints](./get_opaqueboundsinpoints/)() | Obtient les limites opaques de la forme en points. |
| [get_SizeInPoints](./get_sizeinpoints/)() | Obtient la taille réelle de la forme en points. |
| [GetBoundsInPixels](./getboundsinpixels/)(float, float) | Calcule les limites de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetBoundsInPixels](./getboundsinpixels/)(float, float, float) | Calcule les limites de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetOpaqueBoundsInPixels](./getopaqueboundsinpixels/)(float, float) | Calcule les limites opaques de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetOpaqueBoundsInPixels](./getopaqueboundsinpixels/)(float, float, float) | Calcule les limites opaques de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float) | Calcule la taille de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float, float) | Calcule la taille de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeRendererBase](./noderendererbase/)() |  |
| [RenderToScale](./rendertoscale/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | Rend la forme dans un objet **Graphics** à une échelle spécifiée. |
| [RenderToSize](./rendertosize/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | Rend la forme dans un objet **Graphics** à une taille spécifiée. |
| [Save](./save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Rend la forme dans une image et l'enregistre dans un fichier. |
| [Save](./save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Rend la forme dans une image SVG et l'enregistre dans un fichier. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Rend la forme dans une image et l'enregistre dans un flux. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Rend la forme dans une image SVG et l'enregistre dans un flux. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) |  |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) |  |
| static [Type](./type/)() |  |

## Exemples



Montre comment mesurer et mettre à l'échelle les formes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));
auto renderer = System::MakeObject<Aspose::Words::Rendering::OfficeMathRenderer>(officeMath);

// Vérifiez la taille de l'image que l'objet OfficeMath créera lorsqu'on le rend.
ASSERT_NEAR(122.0f, renderer->get_SizeInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_SizeInPoints().get_Height(), 0.15f);

ASSERT_NEAR(122.0f, renderer->get_BoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_BoundsInPoints().get_Height(), 0.15f);

// Les formes avec des parties transparentes peuvent contenir des valeurs différentes dans les propriétés "OpaqueBoundsInPoints".
ASSERT_NEAR(119.5f, renderer->get_OpaqueBoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(14.2f, renderer->get_OpaqueBoundsInPoints().get_Height(), 0.1f);

// Obtenez la taille de la forme en pixels, avec un redimensionnement linéaire à un DPI spécifique.
System::Drawing::Rectangle bounds = renderer->GetBoundsInPixels(1.0f, 96.0f);
System::String dpi96 = u"DPI 96";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96);
ASSERT_EQ(18, bounds.get_Height()) << (dpi96);

// Obtenez la taille de la forme en pixels, mais avec un DPI différent pour les dimensions horizontale et verticale.
bounds = renderer->GetBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150 = u"DPI 96 150";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96150);
ASSERT_EQ(27, bounds.get_Height()) << (dpi96150);

// Les limites opaques peuvent également varier ici.
bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f);
System::String dpi96Opaque = u"DPI 96 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96Opaque);
ASSERT_EQ(19, bounds.get_Height()) << (dpi96Opaque);

bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150Opaque = u"DPI 96 150 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96150Opaque);
ASSERT_EQ(29, bounds.get_Height()) << (dpi96150Opaque);
```

## Voir aussi

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
