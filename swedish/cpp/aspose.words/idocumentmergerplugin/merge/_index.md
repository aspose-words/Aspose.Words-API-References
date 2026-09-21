---
title: "Aspose::Words::IDocumentMergerPlugin::Merge metod"
linktitle: "Sammanfoga"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::IDocumentMergerPlugin::Merge metod. Sammanfogar de angivna inmatnings‑PDF‑dokumenten till ett enda utdata‑PDF‑dokument med hjälp av specificerade in‑ och utmatningsströmmar i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/idocumentmergerplugin/merge/
---
## IDocumentMergerPlugin::Merge method


Slår ihop de angivna inmatnings‑PDF‑dokumenten till ett enda utmatnings‑PDF‑dokument med hjälp av specificerade in‑ och utströmar.

```cpp
virtual void Aspose::Words::IDocumentMergerPlugin::Merge(System::SharedPtr<System::IO::Stream> outputStream, System::ArrayPtr<System::SharedPtr<System::IO::Stream>> inputStreams, System::ArrayPtr<System::SharedPtr<Aspose::Words::Loading::LoadOptions>> loadOptions)=0
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| outputStream | System::SharedPtr\<System::IO::Stream\> | Utdataflödet. |
| inputStreams | System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\> | Inmatningsströmmarna. |
| loadOptions | System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\> | Laddningsalternativ för inmatningsfilerna. |

## Se även

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Interface [IDocumentMergerPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
