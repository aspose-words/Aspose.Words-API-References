---
title: "Aspose::Words::IDocumentConverterPlugin::ConvertToImages Methode"
linktitle: "ConvertToImages"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::IDocumentConverterPlugin::ConvertToImages-Methode. Konvertiert Seiten aus einem Dokument aus dem Eingabestream in ein Array von Bildern in C++."
type: docs
weight: 2500
url: /de/cpp/aspose.words/idocumentconverterplugin/converttoimages/
---
## IDocumentConverterPlugin::ConvertToImages method


Konvertiert Seiten aus einem Dokument vom Eingabestrom in ein Bildarray.

```cpp
virtual System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::IDocumentConverterPlugin::ConvertToImages(System::SharedPtr<System::IO::Stream> inputStream, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions)=0
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | System::SharedPtr\<System::IO::Stream\> | Der Eingabestream. |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | Die Dokument-Ladeoptionen. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> | Die Speicheroptionen. |

### ReturnValue

Array von Seitenbild-Streams.

## Siehe auch

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Interface [IDocumentConverterPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
