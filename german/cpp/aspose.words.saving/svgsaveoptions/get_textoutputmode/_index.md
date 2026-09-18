---
title: "Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode Methode"
linktitle: "get_TextOutputMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode Methode. Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie Text in SVG in C++ gerendert werden soll."
type: docs
weight: 10000
url: /de/cpp/aspose.words.saving/svgsaveoptions/get_textoutputmode/
---
## SvgSaveOptions::get_TextOutputMode method


Liest oder setzt einen Wert, der bestimmt, wie Text in SVG gerendert werden soll.

```cpp
Aspose::Words::Saving::SvgTextOutputMode Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode() const
```

## Hinweise


Verwenden Sie diese Eigenschaft, um den Modus zu erhalten oder festzulegen, wie Text in einem Dokument beim Speichern im SVG-Format gerendert werden soll.

Der Standardwert ist [UseTargetMachineFonts](../../svgtextoutputmode/).

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

* Enum [SvgTextOutputMode](../../svgtextoutputmode/)
* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
