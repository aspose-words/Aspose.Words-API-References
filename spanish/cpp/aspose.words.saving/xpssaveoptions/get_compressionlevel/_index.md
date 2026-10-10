---
title: "Método Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel"
linktitle: "get_CompressionLevel"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel. Especifica el nivel de compresión utilizado para guardar el documento. El valor predeterminado es Normal en C++."
type: docs
weight: 2250
url: /es/cpp/aspose.words.saving/xpssaveoptions/get_compressionlevel/
---
## XpsSaveOptions::get_CompressionLevel method


Especifica el nivel de compresión utilizado para guardar el documento. El valor predeterminado es [Normal](../../compressionlevel/).

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel() const
```


## Ejemplos



Muestra cómo controlar el nivel de compresión al guardar un documento en formato XPS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample document for XPS compression test.");

// Cree un objeto XpsSaveOptions y establezca el nivel de compresión.
auto options = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();
options->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.CompressionLevelXps.xps", options);
```

## Ver también

* Enum [CompressionLevel](../../compressionlevel/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
