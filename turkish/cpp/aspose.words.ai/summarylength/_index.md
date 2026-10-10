---
title: "Aspose::Words::AI::SummaryLength enum"
linktitle: "SummaryLength"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::AI::SummaryLength enum. C++'da özet uzunluklarının olası değerlerini listeler."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.ai/summarylength/
---
## SummaryLength enum


Özetin olası uzunluklarını listeler.

```cpp
enum class SummaryLength
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| VeryShort | 0 | 1-2 cümle üretmeye çalış. |
| Short | 1 | 3-4 cümle üretmeye çalış. |
| Medium | 2 | 5-6 cümle üretmeye çalış. |
| Uzun | 3 | 7-10 cümle üretmeyi deneyin. |
| ÇokUzun | 4 | 11-20 cümle üretmeyi deneyin. |


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

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
