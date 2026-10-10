---
title: "Aspose::Words::AI::SummarizeOptions::SummarizeOptions konstruktör"
linktitle: "SummarizeOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::AI::SummarizeOptions::SummarizeOptions konstruktör. Initierar en ny instans av SummarizeOptions‑klassen i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.ai/summarizeoptions/summarizeoptions/
---
## SummarizeOptions::SummarizeOptions constructor


Initierar en ny instans av klassen [SummarizeOptions](../).

```cpp
Aspose::Words::AI::SummarizeOptions::SummarizeOptions()
```


## Exempel



Visar hur man sammanfattar text med hjälp av OpenAI- och Google-modeller.
```cpp
auto firstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto secondDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Använd generativa språkmodeller från OpenAI eller Google.
System::SharedPtr<Aspose::Words::AI::AiModel> model = (System::ExplicitCast<Aspose::Words::AI::OpenAiModel>(Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey)))->WithOrganization(u"Organization")->WithProject(u"Project");

auto options = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Short);
System::SharedPtr<Aspose::Words::Document> oneDocumentSummary = model->Summarize(firstDoc, options);
oneDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.One.docx");

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Long);
System::SharedPtr<Aspose::Words::Document> multiDocumentSummary = model->Summarize(System::MakeArray<System::SharedPtr<Aspose::Words::Document>>({firstDoc, secondDoc}), options);
multiDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.Multi.docx");
```

## Se även

* Class [SummarizeOptions](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
