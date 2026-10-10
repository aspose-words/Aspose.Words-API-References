---
title: "Aspose::Words::Saving::DoclingSaveOptions::get_SaveFormat metod"
linktitle: "get_SaveFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::DoclingSaveOptions::get_SaveFormat metod. Anger det format som dokumentet kommer att sparas i om detta spara‑alternativ‑objekt används. Kan endast vara Docling i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.saving/doclingsaveoptions/get_saveformat/
---
## DoclingSaveOptions::get_SaveFormat method


Anger det format som dokumentet kommer att sparas i om detta spara‑alternativ‑objekt används. Kan endast vara [Docling](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::DoclingSaveOptions::get_SaveFormat() override
```


## Exempel



Visar hur man sparar ett dokument i ett Docling JSON-format.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::DoclingSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docling);
// Ställ in på true för att rendera former som inte är bilder och inkludera dem i utdata.
// Ställ in på false (standard) för att utesluta former som inte är bilder från utdata.
saveOptions->set_RenderNonImageShapes(true);

doc->Save(get_ArtifactsDir() + u"Document.DoclingJson.json", saveOptions);
```

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [DoclingSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
