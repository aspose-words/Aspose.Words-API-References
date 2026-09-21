---
title: "Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode‑metod"
linktitle: "get_ImlRenderingMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode‑metod. Hämtar eller anger ett värde som bestämmer hur bläck (InkML)-objekt renderas i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words.saving/saveoptions/get_imlrenderingmode/
---
## SaveOptions::get_ImlRenderingMode method


Hämtar eller anger ett värde som bestämmer hur bläck (InkML)-objekt renderas.

```cpp
Aspose::Words::Saving::ImlRenderingMode Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode() const
```

## Anmärkningar


Standardvärdet är [InkML](../../imlrenderingmode/).

Denna egenskap används när dokumentet exporteras till fasta sidformat.

## Exempel



Visar hur man renderar Ink-objekt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Ink object.docx");

// Ställ in 'ImlRenderingMode.InkML' ignorerar reservformen för bläck (InkML)-objektet och renderar InkML själv.
// Om renderingsresultatet är otillfredsställande,
// vänligen använd 'ImlRenderingMode.Fallback' för att få ett resultat liknande tidigare versioner.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
saveOptions->set_ImlRenderingMode(Aspose::Words::Saving::ImlRenderingMode::InkML);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

## Se även

* Enum [ImlRenderingMode](../../imlrenderingmode/)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
