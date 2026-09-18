---
title: "Aspose::Words::AI::OpenAiModel::Summarize-Methode"
linktitle: "Zusammenfassen"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::AI::OpenAiModel::Summarize-Methode. Erzeugt Zusammenfassungen für ein Array von Dokumenten, mit Optionen zur Steuerung der Zusammenfassungslänge und anderer Einstellungen. Diese Methode nutzt das verbundene KI‑Modell zur Verarbeitung jedes Dokuments im Array in C++."
type: docs
weight: 3334
url: /de/cpp/aspose.words.ai/openaimodel/summarize/
---
## OpenAiModel::Summarize(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) method


Erstellt Zusammenfassungen für ein Array von Dokumenten, mit Optionen zur Steuerung der Zusammenfassungslänge und anderer Einstellungen. Diese Methode nutzt das verbundene [AI](../../)-Modell zur Verarbeitung jedes Dokuments im Array.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::OpenAiModel::Summarize(System::ArrayPtr<System::SharedPtr<Aspose::Words::Document>> sourceDocuments, System::SharedPtr<Aspose::Words::AI::SummarizeOptions> options=nullptr) override
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sourceDocuments | System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\> | Ein Array von Dokumenten, die zusammengefasst werden sollen. |
| options | System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\> | Optionale Einstellungen zur Steuerung der Zusammenfassungslänge und anderer Parameter |

### ReturnValue

Eine zusammengefasste Version des Inhalts des Dokuments.

## Siehe auch

* Class [Document](../../../aspose.words/document/)
* Class [SummarizeOptions](../../summarizeoptions/)
* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## OpenAiModel::Summarize(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) method


Erstellt eine Zusammenfassung des angegebenen Dokuments, mit Optionen zur Anpassung der Zusammenfassungslänge. Dieser Vorgang nutzt das verbundene [AI](../../)-Modell zur Inhaltsverarbeitung.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::OpenAiModel::Summarize(System::SharedPtr<Aspose::Words::Document> sourceDocument, System::SharedPtr<Aspose::Words::AI::SummarizeOptions> options=nullptr) override
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | Das Dokument, das zusammengefasst werden soll. |
| options | System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\> | Optionale Einstellungen zur Steuerung der Zusammenfassungslänge und anderer Parameter. |

### ReturnValue

Eine zusammengefasste Version des Inhalts des Dokuments.

## Siehe auch

* Class [Document](../../../aspose.words/document/)
* Class [SummarizeOptions](../../summarizeoptions/)
* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
