---
title: "Aspose::Words::Rendering::OfficeMathRenderer::OfficeMathRenderer constructor"
linktitle: "OfficeMathRenderer"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Rendering::OfficeMathRenderer::OfficeMathRenderer constructor. Initialise une nouvelle instance de cette classe en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.rendering/officemathrenderer/officemathrenderer/
---
## OfficeMathRenderer::OfficeMathRenderer constructor


Initialise une nouvelle instance de cette classe.

```cpp
Aspose::Words::Rendering::OfficeMathRenderer::OfficeMathRenderer(const System::SharedPtr<Aspose::Words::Math::OfficeMath> &math)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| math | const System::SharedPtr\<Aspose::Words::Math::OfficeMath\>\& | L'objet [OfficeMath](../../../aspose.words.math/officemath/) que vous souhaitez rendre. |

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

* Class [OfficeMath](../../../aspose.words.math/officemath/)
* Class [OfficeMathRenderer](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
