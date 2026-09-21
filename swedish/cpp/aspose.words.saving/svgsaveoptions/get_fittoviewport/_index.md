---
title: "Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort metod"
linktitle: "get_FitToViewPort"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort metod. Anger om den exporterade SVG:n ska fylla hela tillgängliga visningsområde (webbläsarfönster eller behållare). När den är satt till true sätts bredd och höjd på SVG:n till 100 %. Standardvärdet är false i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.saving/svgsaveoptions/get_fittoviewport/
---
## SvgSaveOptions::get_FitToViewPort method


Anger om den exporterade SVG:n ska fylla det tillgängliga visningsområdet (webbläsarfönster eller behållare). När den är satt till **true** sätts bredd och höjd på den exporterade SVG:n till 100 %. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort() const
```


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

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
