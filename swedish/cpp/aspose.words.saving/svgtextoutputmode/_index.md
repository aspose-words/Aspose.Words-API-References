---
title: "Aspose::Words::Saving::SvgTextOutputMode enum"
linktitle: "SvgTextOutputMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::SvgTextOutputMode enum. Tillåter att ange hur text i ett dokument ska renderas vid sparande i SVG-format i C++."
type: docs
weight: 83000
url: /sv/cpp/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enum


Tillåter att ange hur text i ett dokument ska renderas vid sparande i SVG-format.

```cpp
enum class SvgTextOutputMode
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| UseSvgFonts | 0 | SVG-teckensnitt används för att rendera text. Observera att inte alla webbläsare stödjer SVG-teckensnitt. |
| UseTargetMachineFonts | 1 | [Fonts](../../aspose.words.fonts/) installerade på målmaskinen används för att rendera text. Observera att om vissa teckensnitt som används i dokumentet inte är tillgängliga på målmaskinen, kan dokumentet se annorlunda ut. |
| UsePlacedGlyphs | 2 | Text renderas med kurvor. Observera att textmarkering inte kommer att fungera om du använder detta alternativ. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
