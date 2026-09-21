---
title: "Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel metod"
linktitle: "get_CompressionLevel"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel metod. Anger komprimeringsnivån som används för att spara dokumentet. Standardvärdet är Normal i C++."
type: docs
weight: 2250
url: /sv/cpp/aspose.words.saving/xpssaveoptions/get_compressionlevel/
---
## XpsSaveOptions::get_CompressionLevel method


Anger komprimeringsnivån som används för att spara dokumentet. Standardvärdet är [Normal](../../compressionlevel/).

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel() const
```


## Exempel



Visar hur man styr komprimeringsnivån när ett dokument sparas i XPS-format.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample document for XPS compression test.");

// Skapa ett XpsSaveOptions-objekt och ange komprimeringsnivån.
auto options = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();
options->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.CompressionLevelXps.xps", options);
```

## Se även

* Enum [CompressionLevel](../../compressionlevel/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
