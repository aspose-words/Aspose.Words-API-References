---
title: "Aspose::Words::IDocumentConverterPlugin::ConvertToImages metod"
linktitle: "ConvertToImages"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::IDocumentConverterPlugin::ConvertToImages metod. Konverterar sidor från dokumentet från indataflöde till en array av bilder i C++."
type: docs
weight: 2500
url: /sv/cpp/aspose.words/idocumentconverterplugin/converttoimages/
---
## IDocumentConverterPlugin::ConvertToImages method


Konverterar sidor från dokumentet från indataflöde till en matris av bilder.

```cpp
virtual System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::IDocumentConverterPlugin::ConvertToImages(System::SharedPtr<System::IO::Stream> inputStream, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions)=0
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | System::SharedPtr\<System::IO::Stream\> | Inmatningsströmmen. |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | Dokumentets inläsningsalternativ. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> | Sparalternativen. |

### ReturnValue

Array av sidbildströmmar.

## Se även

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Interface [IDocumentConverterPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
