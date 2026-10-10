---
title: "Metodo Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel"
linktitle: "get_CompressionLevel"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel. Specifica il livello di compressione usato per salvare il documento. Il valore predefinito è Normal in C++."
type: docs
weight: 2250
url: /it/cpp/aspose.words.saving/xpssaveoptions/get_compressionlevel/
---
## XpsSaveOptions::get_CompressionLevel method


Specifica il livello di compressione usato per salvare il documento. Il valore predefinito è [Normal](../../compressionlevel/).

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel() const
```


## Esempi



Mostra come controllare il livello di compressione durante il salvataggio di un documento in formato XPS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample document for XPS compression test.");

// Crea un oggetto XpsSaveOptions e imposta il livello di compressione.
auto options = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();
options->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.CompressionLevelXps.xps", options);
```

## Vedi anche

* Enum [CompressionLevel](../../compressionlevel/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
