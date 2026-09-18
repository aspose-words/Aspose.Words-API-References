---
title: "Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort Methode"
linktitle: "get_FitToViewPort"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort Methode. Gibt an, ob das ausgegebene SVG den verfügbaren Viewport‑Bereich (Browser‑Fenster oder Container) ausfüllen soll. Wenn auf true gesetzt, werden Breite und Höhe des AusgabesVG auf 100 % gesetzt. Der Standardwert ist false in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.saving/svgsaveoptions/get_fittoviewport/
---
## SvgSaveOptions::get_FitToViewPort method


Gibt an, ob das ausgegebene SVG den verfügbaren Ansichtsbereich (Browserfenster oder Container) ausfüllen soll. Wenn es auf **true** gesetzt ist, werden Breite und Höhe des ausgegebenen SVG auf 100 % gesetzt. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort() const
```


## Beispiele



Zeigt, wie die Eigenschaften von Bildern beim Konvertieren eines .docx-Dokuments in .svg nachgeahmt werden können.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Konfigurieren Sie das SvgSaveOptions-Objekt, um ohne Seitenränder oder auswählbaren Text zu speichern.
auto options = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
options->set_FitToViewPort(true);
options->set_ShowPageBorder(false);
options->set_TextOutputMode(Aspose::Words::Saving::SvgTextOutputMode::UsePlacedGlyphs);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.SaveLikeImage.svg", options);
```

## Siehe auch

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
