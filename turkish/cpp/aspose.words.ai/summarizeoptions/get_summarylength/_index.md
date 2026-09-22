---
title: "Aspose::Words::AI::SummarizeOptions::get_SummaryLength yöntemi"
linktitle: "get_SummaryLength"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::AI::SummarizeOptions::get_SummaryLength yöntemi. Özet uzunluğunu belirtmenizi sağlar. Varsayılan değer C++'da Medium'dur."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.ai/summarizeoptions/get_summarylength/
---
## SummarizeOptions::get_SummaryLength method


Özet uzunluğunu belirtmenizi sağlar. Varsayılan değer [Medium](../../summarylength/)dır.

```cpp
Aspose::Words::AI::SummaryLength Aspose::Words::AI::SummarizeOptions::get_SummaryLength() const
```


## Örnekler



OpenAI ve Google modellerini kullanarak metni nasıl özetleyeceğinizi gösterir.
```cpp
auto firstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto secondDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// OpenAI veya Google üretken dil modellerini kullanın.
System::SharedPtr<Aspose::Words::AI::AiModel> model = (System::ExplicitCast<Aspose::Words::AI::OpenAiModel>(Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey)))->WithOrganization(u"Organization")->WithProject(u"Project");

auto options = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Short);
System::SharedPtr<Aspose::Words::Document> oneDocumentSummary = model->Summarize(firstDoc, options);
oneDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.One.docx");

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Long);
System::SharedPtr<Aspose::Words::Document> multiDocumentSummary = model->Summarize(System::MakeArray<System::SharedPtr<Aspose::Words::Document>>({firstDoc, secondDoc}), options);
multiDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.Multi.docx");
```

## Ayrıca Bakınız

* Enum [SummaryLength](../../summarylength/)
* Class [SummarizeOptions](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
