---
title: "Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode metod"
linktitle: "get_TextOutputMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode metod. Hämtar eller anger ett värde som bestämmer hur text ska renderas i SVG i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words.saving/svgsaveoptions/get_textoutputmode/
---
## SvgSaveOptions::get_TextOutputMode method


Hämtar eller anger ett värde som bestämmer hur text ska renderas i SVG.

```cpp
Aspose::Words::Saving::SvgTextOutputMode Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode() const
```

## Anmärkningar


Använd den här egenskapen för att hämta eller ange läget för hur text i ett dokument ska renderas när den sparas i SVG-format.

Standardvärdet är [UseTargetMachineFonts](../../svgtextoutputmode/).

## Exempel



Visar hur man efterliknar bildegenskaper när man konverterar ett .docx-dokument till .svg.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Konfigurera SvgSaveOptions-objektet för att spara utan sidramar eller markerbar text.
auto options = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
options->set_FitToViewPort(true);
options->set_ShowPageBorder(false);
options->set_TextOutputMode(Aspose::Words::Saving::SvgTextOutputMode::UsePlacedGlyphs);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.SaveLikeImage.svg", options);
```

## Se även

* Enum [SvgTextOutputMode](../../svgtextoutputmode/)
* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
