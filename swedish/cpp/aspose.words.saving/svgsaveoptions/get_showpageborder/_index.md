---
title: "Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder metod"
linktitle: "get_ShowPageBorder"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder metod. Styr om en ram läggs till runt sidans kontur. Standard är true i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.saving/svgsaveoptions/get_showpageborder/
---
## SvgSaveOptions::get_ShowPageBorder method


Styr om en ram läggs till runt sidans kontur. Standard är **true**.

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder() const
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
