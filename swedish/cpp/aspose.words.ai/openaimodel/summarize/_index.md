---
title: "Aspose::Words::AI::OpenAiModel::Summarize‑metod"
linktitle: "Sammanfatta"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::AI::OpenAiModel::Summarize‑metod. Genererar sammanfattningar för en matris av dokument, med alternativ för att styra sammanfattningens längd och andra inställningar. Denna metod använder den anslutna AI‑modellen för att bearbeta varje dokument i matrisen i C++."
type: docs
weight: 3334
url: /sv/cpp/aspose.words.ai/openaimodel/summarize/
---
## OpenAiModel::Summarize(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) method


Skapar sammanfattningar för en array av dokument, med alternativ för att kontrollera sammanfattningens längd och andra inställningar. Denna metod använder den anslutna [AI](../../)‑modellen för att bearbeta varje dokument i arrayen.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::OpenAiModel::Summarize(System::ArrayPtr<System::SharedPtr<Aspose::Words::Document>> sourceDocuments, System::SharedPtr<Aspose::Words::AI::SummarizeOptions> options=nullptr) override
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| sourceDocuments | System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\> | En array av dokument som ska sammanfattas. |
| options | System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\> | Valfria inställningar för att kontrollera sammanfattningens längd och andra parametrar |

### ReturnValue

En sammanfattad version av dokumentets innehåll.

## Se även

* Class [Document](../../../aspose.words/document/)
* Class [SummarizeOptions](../../summarizeoptions/)
* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## OpenAiModel::Summarize(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) method


Skapar en sammanfattning av det angivna dokumentet, med alternativ för att justera sammanfattningens längd. Denna operation utnyttjar den anslutna [AI](../../)‑modellen för innehållsbehandling.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::OpenAiModel::Summarize(System::SharedPtr<Aspose::Words::Document> sourceDocument, System::SharedPtr<Aspose::Words::AI::SummarizeOptions> options=nullptr) override
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | Dokumentet som ska sammanfattas. |
| options | System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\> | Valfria inställningar för att kontrollera sammanfattningens längd och andra parametrar. |

### ReturnValue

En sammanfattad version av dokumentets innehåll.

## Se även

* Class [Document](../../../aspose.words/document/)
* Class [SummarizeOptions](../../summarizeoptions/)
* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
