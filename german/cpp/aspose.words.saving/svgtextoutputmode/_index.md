---
title: "Aspose::Words::Saving::SvgTextOutputMode enum"
linktitle: "SvgTextOutputMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::SvgTextOutputMode enum. Ermöglicht die Angabe, wie Text innerhalb eines Dokuments beim Speichern im SVG-Format in C++ gerendert werden soll."
type: docs
weight: 83000
url: /de/cpp/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enum


Ermöglicht die Angabe, wie Text innerhalb eines Dokuments beim Speichern im SVG-Format gerendert werden soll.

```cpp
enum class SvgTextOutputMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| UseSvgFonts | 0 | SVG-Schriften werden zum Rendern von Text verwendet. Hinweis: Nicht alle Browser unterstützen SVG-Schriften. |
| UseTargetMachineFonts | 1 | [Fonts](../../aspose.words.fonts/) auf dem Zielrechner installierte Schriften werden zum Rendern von Text verwendet. Hinweis: Wenn einige der im Dokument verwendeten Schriften auf dem Zielrechner nicht verfügbar sind, kann das Dokument anders aussehen. |
| UsePlacedGlyphs | 2 | Text wird mit Kurven gerendert. Hinweis: Die Textauswahl funktioniert nicht, wenn Sie diese Option verwenden. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
