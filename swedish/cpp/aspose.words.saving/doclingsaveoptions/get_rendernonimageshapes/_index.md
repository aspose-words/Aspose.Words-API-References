---
title: "Metoden Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes"
linktitle: "get_RenderNonImageShapes"
second_title: "Aspose.Words för C++ API‑referens"
description: "Metoden Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes. Hämtar eller anger ett värde som indikerar om icke‑bildformer ska renderas och skrivas till utdata‑Docling‑JSON‑dokumentet i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.saving/doclingsaveoptions/get_rendernonimageshapes/
---
## DoclingSaveOptions::get_RenderNonImageShapes method


Hämtar eller anger ett värde som indikerar om icke‑bildformer ska renderas och skrivas till utdata Docling JSON‑dokumentet.

```cpp
bool Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes() const
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

* Class [DoclingSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
