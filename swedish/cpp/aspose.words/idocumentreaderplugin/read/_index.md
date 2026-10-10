---
title: "Aspose::Words::IDocumentReaderPlugin::Read metod"
linktitle: "Läs"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::IDocumentReaderPlugin::Read metod. Läser data från den angivna strömmen till Document‑instansen i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/idocumentreaderplugin/read/
---
## IDocumentReaderPlugin::Read method


Läser data från den angivna strömmen till [Document](../../document/)‑instansen.

```cpp
virtual void Aspose::Words::IDocumentReaderPlugin::Read(System::SharedPtr<System::IO::Stream> src, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<Aspose::Words::Document> document)=0
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| src | System::SharedPtr\<System::IO::Stream\> | Källströmmen för att läsa dokumentet från. |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | Ytterligare laddningsalternativ för att ladda dokumentet. |
| document | System::SharedPtr\<Aspose::Words::Document\> | Instansen av klassen [Document](../../document/) att läsa data till. Om instansen innehåller något innehåll kommer det att skrivas över av data från källströmmen. |

## Se även

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../../document/)
* Interface [IDocumentReaderPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
