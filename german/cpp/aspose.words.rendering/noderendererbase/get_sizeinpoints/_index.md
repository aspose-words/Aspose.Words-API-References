---
title: "Aspose::Words::Rendering::NodeRendererBase::get_SizeInPoints Methode"
linktitle: "get_SizeInPoints"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Rendering::NodeRendererBase::get_SizeInPoints Methode. Gibt die tatsächliche Größe der Form in Punkten in C++ zurück."
type: docs
weight: 5000
url: /de/cpp/aspose.words.rendering/noderendererbase/get_sizeinpoints/
---
## NodeRendererBase::get_SizeInPoints method


Ermittelt die tatsächliche Größe der Form in Punkten.

```cpp
System::Drawing::SizeF Aspose::Words::Rendering::NodeRendererBase::get_SizeInPoints()
```

## Hinweise


Diese Eigenschaft gibt die Größe des tatsächlichen (wie auf der Seite gerenderten) Begrenzungsrahmens der Form zurück. Die Größe berücksichtigt die Drehung der Form (falls vorhanden).

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

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
