---
title: Aspose::Words::Saving::XpsSaveOptions::set_CompressionLevel method
linktitle: set_CompressionLevel
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::XpsSaveOptions::set_CompressionLevel method. Specifies the compression level used to save document. The default value is Normal in C++.'
type: docs
weight: 7250
url: /cpp/aspose.words.saving/xpssaveoptions/set_compressionlevel/
---
## XpsSaveOptions::set_CompressionLevel method


Specifies the compression level used to save document. The default value is [Normal](../../compressionlevel/).

```cpp
void Aspose::Words::Saving::XpsSaveOptions::set_CompressionLevel(Aspose::Words::Saving::CompressionLevel value)
```

## Examples


Shows how to control the compression level when saving a document to XPS format.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample document for XPS compression test.");

// Create an XpsSaveOptions object and set the compression level.
auto options = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();
options->set_CompressionLevel(CompressionLevel::Maximum);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.CompressionLevelXps.xps", options);
```
## See Also

* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
