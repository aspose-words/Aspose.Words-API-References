---
title: "Aspose::Words::AI::SummaryLength enum"
linktitle: "SummaryLength"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::AI::SummaryLength enum. Enumeriert mögliche Längen der Zusammenfassung in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words.ai/summarylength/
---
## SummaryLength enum


Enumeriert mögliche Längen der Zusammenfassung.

```cpp
enum class SummaryLength
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| VeryShort | 0 | Versuchen Sie, 1-2 Sätze zu erzeugen. |
| Short | 1 | Versuchen Sie, 3-4 Sätze zu erzeugen. |
| Medium | 2 | Versuchen Sie, 5-6 Sätze zu erzeugen. |
| Long | 3 | Versuchen Sie, 7-10 Sätze zu erzeugen. |
| VeryLong | 4 | Versuchen Sie, 11-20 Sätze zu erzeugen. |


## Beispiele



Zeigt, wie man Text mit OpenAI‑ und Google‑Modellen zusammenfasst.
```cpp
auto firstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto secondDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Verwenden Sie generative Sprachmodelle von OpenAI oder Google.
System::SharedPtr<Aspose::Words::AI::AiModel> model = (System::ExplicitCast<Aspose::Words::AI::OpenAiModel>(Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey)))->WithOrganization(u"Organization")->WithProject(u"Project");

auto options = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Short);
System::SharedPtr<Aspose::Words::Document> oneDocumentSummary = model->Summarize(firstDoc, options);
oneDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.One.docx");

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Long);
System::SharedPtr<Aspose::Words::Document> multiDocumentSummary = model->Summarize(System::MakeArray<System::SharedPtr<Aspose::Words::Document>>({firstDoc, secondDoc}), options);
multiDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.Multi.docx");
```

## Siehe auch

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
