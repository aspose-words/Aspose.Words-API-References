---
title: "Aspose::Words::Rendering::NodeRendererBase::GetOpaqueBoundsInPixels Methode"
linktitle: "GetOpaqueBoundsInPixels"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Rendering::NodeRendererBase::GetOpaqueBoundsInPixels Methode. Berechnet die undurchsichtigen Begrenzungen der Form in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/
---
## NodeRendererBase::GetOpaqueBoundsInPixels(float, float) method


Berechnet die undurchsichtigen Begrenzungen der Form in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung.

```cpp
System::Drawing::Rectangle Aspose::Words::Rendering::NodeRendererBase::GetOpaqueBoundsInPixels(float scale, float dpi)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| scale | float | Der Zoomfaktor (1,0 entspricht 100 %). |
| dpi | float | Die Auflösung, um von Punkten zu Pixeln zu konvertieren (Punkte pro Zoll). |

### ReturnValue

Das undurchsichtige Rechteck der Form in Pixeln.
## Hinweise


Diese Methode konvertiert [OpaqueBoundsInPoints](../get_opaqueboundsinpoints/) in ein Rechteck in Pixeln und ist nützlich, wenn Sie ein Bitmap erstellen möchten, um die Form nur mit dem undurchsichtigen Teil zu rendern.

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
## NodeRendererBase::GetOpaqueBoundsInPixels(float, float, float) method


Berechnet die undurchsichtigen Begrenzungen der Form in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung.

```cpp
System::Drawing::Rectangle Aspose::Words::Rendering::NodeRendererBase::GetOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| scale | float | Der Zoomfaktor (1,0 entspricht 100 %). |
| horizontalDpi | float | Die horizontale Auflösung, um von Punkten zu Pixeln zu konvertieren (Punkte pro Zoll). |
| verticalDpi | float | Die vertikale Auflösung, um von Punkten zu Pixeln zu konvertieren (Punkte pro Zoll). |

### ReturnValue

Das undurchsichtige Rechteck der Form in Pixeln.
## Hinweise


Diese Methode konvertiert [OpaqueBoundsInPoints](../get_opaqueboundsinpoints/) in ein Rechteck in Pixeln und ist nützlich, wenn Sie ein Bitmap erstellen möchten, um die Form nur mit dem undurchsichtigen Teil zu rendern.

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
