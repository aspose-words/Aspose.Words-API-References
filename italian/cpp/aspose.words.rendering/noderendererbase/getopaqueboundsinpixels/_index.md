---
title: "Aspose::Words::Rendering::NodeRendererBase::GetOpaqueBoundsInPixels method"
linktitle: "GetOpaqueBoundsInPixels"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Rendering::NodeRendererBase::GetOpaqueBoundsInPixels method. Calcola i limiti opachi della forma in pixel per un fattore di zoom e una risoluzione specificati in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/
---
## NodeRendererBase::GetOpaqueBoundsInPixels(float, float) method


Calcola i limiti opachi della forma in pixel per un fattore di zoom e una risoluzione specificati.

```cpp
System::Drawing::Rectangle Aspose::Words::Rendering::NodeRendererBase::GetOpaqueBoundsInPixels(float scale, float dpi)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| scale | float | Il fattore di zoom (1.0 è 100%). |
| dpi | float | La risoluzione per convertire da punti a pixel (punti per pollice). |

### ReturnValue

Il rettangolo opaco della forma in pixel.
## Note


Questo metodo converte [OpaqueBoundsInPoints](../get_opaqueboundsinpoints/) in un rettangolo in pixel ed è utile quando si desidera creare un bitmap per il rendering della forma con solo la parte opaca della forma.

## Esempi



Mostra come misurare e scalare le forme.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));
auto renderer = System::MakeObject<Aspose::Words::Rendering::OfficeMathRenderer>(officeMath);

// Verifica le dimensioni dell'immagine che l'oggetto OfficeMath creerà quando la renderizziamo.
ASSERT_NEAR(122.0f, renderer->get_SizeInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_SizeInPoints().get_Height(), 0.15f);

ASSERT_NEAR(122.0f, renderer->get_BoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_BoundsInPoints().get_Height(), 0.15f);

// Le forme con parti trasparenti possono contenere valori diversi nella proprietà "OpaqueBoundsInPoints".
ASSERT_NEAR(119.5f, renderer->get_OpaqueBoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(14.2f, renderer->get_OpaqueBoundsInPoints().get_Height(), 0.1f);

// Ottieni le dimensioni della forma in pixel, con scala lineare a una DPI specifica.
System::Drawing::Rectangle bounds = renderer->GetBoundsInPixels(1.0f, 96.0f);
System::String dpi96 = u"DPI 96";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96);
ASSERT_EQ(18, bounds.get_Height()) << (dpi96);

// Ottieni le dimensioni della forma in pixel, ma con una DPI diversa per le dimensioni orizzontali e verticali.
bounds = renderer->GetBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150 = u"DPI 96 150";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96150);
ASSERT_EQ(27, bounds.get_Height()) << (dpi96150);

// I limiti opachi possono variare anche qui.
bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f);
System::String dpi96Opaque = u"DPI 96 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96Opaque);
ASSERT_EQ(19, bounds.get_Height()) << (dpi96Opaque);

bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150Opaque = u"DPI 96 150 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96150Opaque);
ASSERT_EQ(29, bounds.get_Height()) << (dpi96150Opaque);
```

## Vedi anche

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::GetOpaqueBoundsInPixels(float, float, float) method


Calcola i limiti opachi della forma in pixel per un fattore di zoom e una risoluzione specificati.

```cpp
System::Drawing::Rectangle Aspose::Words::Rendering::NodeRendererBase::GetOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| scale | float | Il fattore di zoom (1.0 è 100%). |
| horizontalDpi | float | La risoluzione orizzontale per convertire da punti a pixel (punti per pollice). |
| verticalDpi | float | La risoluzione verticale per convertire da punti a pixel (punti per pollice). |

### ReturnValue

Il rettangolo opaco della forma in pixel.
## Note


Questo metodo converte [OpaqueBoundsInPoints](../get_opaqueboundsinpoints/) in un rettangolo in pixel ed è utile quando si desidera creare un bitmap per il rendering della forma con solo la parte opaca della forma.

## Esempi



Mostra come misurare e scalare le forme.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));
auto renderer = System::MakeObject<Aspose::Words::Rendering::OfficeMathRenderer>(officeMath);

// Verifica le dimensioni dell'immagine che l'oggetto OfficeMath creerà quando la renderizziamo.
ASSERT_NEAR(122.0f, renderer->get_SizeInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_SizeInPoints().get_Height(), 0.15f);

ASSERT_NEAR(122.0f, renderer->get_BoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_BoundsInPoints().get_Height(), 0.15f);

// Le forme con parti trasparenti possono contenere valori diversi nella proprietà "OpaqueBoundsInPoints".
ASSERT_NEAR(119.5f, renderer->get_OpaqueBoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(14.2f, renderer->get_OpaqueBoundsInPoints().get_Height(), 0.1f);

// Ottieni le dimensioni della forma in pixel, con scala lineare a una DPI specifica.
System::Drawing::Rectangle bounds = renderer->GetBoundsInPixels(1.0f, 96.0f);
System::String dpi96 = u"DPI 96";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96);
ASSERT_EQ(18, bounds.get_Height()) << (dpi96);

// Ottieni le dimensioni della forma in pixel, ma con una DPI diversa per le dimensioni orizzontali e verticali.
bounds = renderer->GetBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150 = u"DPI 96 150";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96150);
ASSERT_EQ(27, bounds.get_Height()) << (dpi96150);

// I limiti opachi possono variare anche qui.
bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f);
System::String dpi96Opaque = u"DPI 96 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96Opaque);
ASSERT_EQ(19, bounds.get_Height()) << (dpi96Opaque);

bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150Opaque = u"DPI 96 150 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96150Opaque);
ASSERT_EQ(29, bounds.get_Height()) << (dpi96150Opaque);
```

## Vedi anche

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
