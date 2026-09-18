---
title: "Aspose::Words::Saving::MultiPageLayout Klasse"
linktitle: "MultiPageLayout"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::MultiPageLayout Klasse. Definiert ein Layout zum Rendern mehrerer Seiten in einer einzigen Ausgabe in C++."
type: docs
weight: 14500
url: /de/cpp/aspose.words.saving/multipagelayout/
---
## MultiPageLayout class


Definiert ein Layout zum Rendern mehrerer Seiten in einer einzigen Ausgabe.

```cpp
class MultiPageLayout : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_BackColor](./get_backcolor/)() | Ermittelt die Hintergrundfarbe der Ausgabe. Der Standardwert ist **Empty**. |
| [get_BorderColor](./get_bordercolor/)() | Ermittelt die Farbe des Seitenrandes. Der Standardwert ist **Empty**. |
| [get_BorderWidth](./get_borderwidth/)() const | Ermittelt die Breite des Seitenrandes. Der Standardwert ist 0. |
| [GetType](./gettype/)() const override |  |
| static [Grid](./grid/)(int32_t, float, float) | Erstellt ein Layout, in dem Seiten von links nach rechts und von oben nach unten in einem Raster mit der angegebenen Spaltenanzahl gerendert werden. |
| static [Horizontal](./horizontal/)(float) | Erstellt ein Layout, in dem alle angegebenen Seiten horizontal nebeneinander von links nach rechts in einer einzigen Ausgabe gerendert werden. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BackColor](./set_backcolor/)(System::Drawing::Color) | Legt die Hintergrundfarbe der Ausgabe fest. Der Standardwert ist **Empty**. |
| [set_BorderColor](./set_bordercolor/)(System::Drawing::Color) | Legt die Farbe des Seitenrandes fest. Der Standardwert ist **Empty**. |
| [set_BorderWidth](./set_borderwidth/)(float) | Legt die Breite des Seitenrandes fest. Der Standardwert ist 0. |
| static [SinglePage](./singlepage/)() | Erstellt ein Layout, das nur die erste der angegebenen Seiten rendert. |
| static [TiffFrames](./tiffframes/)() | Erstellt ein Layout, bei dem jede Seite als separates Bild in einem mehrrahmigen TIFF-Bild gerendert wird. Nur für TIFF-Bildformate anwendbar. |
| static [Type](./type/)() |  |
| static [Vertical](./vertical/)(float) | Erstellt ein Layout, bei dem alle angegebenen Seiten vertikal untereinander in einer einzigen Ausgabe gerendert werden. |

## Beispiele



Zeigt, wie das Dokument mit Multi-Page-Layout-Einstellungen in ein JPG-Bild gespeichert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Richten Sie ein Rasterlayout ein mit:
// - 3 Spalten pro Zeile.
// - 10pt Abstand zwischen den Seiten (horizontal und vertikal).
options->set_PageLayout(Aspose::Words::Saving::MultiPageLayout::Grid(3, 10.0f, 10.0f));

// Alternative Layouts:
// options.PageLayout = MultiPageLayout.Horizontal(10);
// options.PageLayout = MultiPageLayout.Vertical(10);

// Passen Sie den Hintergrund und den Rand an.
options->get_PageLayout()->set_BackColor(System::Drawing::Color::get_LightGray());
options->get_PageLayout()->set_BorderColor(System::Drawing::Color::get_Blue());
options->get_PageLayout()->set_BorderWidth(2.0f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.GridLayout.jpg", options);
```

## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
