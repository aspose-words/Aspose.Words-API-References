---
title: "Aspose::Words::Saving::ImageSaveOptions::get_PageLayout-Methode"
linktitle: "get_PageLayout"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ImageSaveOptions::get_PageLayout-Methode. Gibt das Layout zurück oder legt es fest, das beim Rendern mehrerer Seiten in eine einzelne Ausgabe in C++ verwendet wird."
type: docs
weight: 9500
url: /de/cpp/aspose.words.saving/imagesaveoptions/get_pagelayout/
---
## ImageSaveOptions::get_PageLayout method


Liest oder setzt das Layout, das beim Rendern mehrerer Seiten in eine einzelne Ausgabe verwendet wird.

```cpp
System::SharedPtr<Aspose::Words::Saving::MultiPageLayout> Aspose::Words::Saving::ImageSaveOptions::get_PageLayout() const
```

## Hinweise


Verwenden Sie eine der Fabrikmethoden von [MultiPageLayout](../../multipagelayout/), um diese Eigenschaft zu konfigurieren.

Für [Tiff](../../../aspose.words/saveformat/) ist der Standardwert [TiffFrames](../../multipagelayout/tiffframes/). Für andere Formate ist der Standardwert [SinglePage](../../multipagelayout/singlepage/).

Diese Eigenschaft wirkt nur beim Speichern in die folgenden Formate: [Jpeg](../../../aspose.words/saveformat/), [Gif](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Tiff](../../../aspose.words/saveformat/), [WebP](../)

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

* Class [MultiPageLayout](../../multipagelayout/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
