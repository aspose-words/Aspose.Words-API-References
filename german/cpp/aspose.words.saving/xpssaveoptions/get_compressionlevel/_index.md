---
title: "Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel Methode"
linktitle: "get_CompressionLevel"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel Methode. Gibt das Kompressionslevel an, das zum Speichern des Dokuments verwendet wird. Der Standardwert ist Normal in C++."
type: docs
weight: 2250
url: /de/cpp/aspose.words.saving/xpssaveoptions/get_compressionlevel/
---
## XpsSaveOptions::get_CompressionLevel method


Gibt das Kompressionslevel an, das zum Speichern des Dokuments verwendet wird. Der Standardwert ist [Normal](../../compressionlevel/).

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel() const
```


## Beispiele



Zeigt, wie man die Komprimierungsstufe beim Speichern eines Dokuments im XPS-Format steuert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample document for XPS compression test.");

// Erstellen Sie ein XpsSaveOptions-Objekt und setzen Sie die Komprimierungsstufe.
auto options = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();
options->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.CompressionLevelXps.xps", options);
```

## Siehe auch

* Enum [CompressionLevel](../../compressionlevel/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
