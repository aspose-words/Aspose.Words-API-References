---
title: "Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles metod"
linktitle: "get_AlwaysCompressMetafiles"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles metod. När falskt komprimeras inte små metafiler av prestandaskäl. Standardvärdet är true, alla metafiler komprimeras oavsett storlek i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.saving/docsaveoptions/get_alwayscompressmetafiles/
---
## DocSaveOptions::get_AlwaysCompressMetafiles method


När **false** komprimeras inte små metafiler av prestandaskäl. Standardvärdet är **true**, alla metafiler komprimeras oavsett storlek.

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles() const
```


## Exempel



Visar hur man ändrar komprimering av metafiler i ett dokument vid sparande.
```cpp
// Öppna ett dokument som innehåller en Microsoft Equation 3.0‑formel.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Microsoft equation object.docx");

// När vi sparar ett dokument komprimeras mindre metafiler inte av prestandaskäl.
// Vi kan sätta en flagga i ett SaveOptions‑objekt för att komprimera varje metafil vid sparande.
// Vissa redigerare, såsom LibreOffice, kan inte läsa okomprimerade metafiler.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_AlwaysCompressMetafiles(compressAllMetafiles);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);
```

## Se även

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
