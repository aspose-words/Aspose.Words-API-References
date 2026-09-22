---
title: "طريقة Aspose::Words::AI::OpenAiModel::WithOrganization"
linktitle: "WithOrganization"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::AI::OpenAiModel::WithOrganization. تعيين منظمة محددة للنموذج في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.ai/openaimodel/withorganization/
---
## OpenAiModel::WithOrganization method


يضبط منظمة محددة للنموذج.

```cpp
System::SharedPtr<Aspose::Words::AI::OpenAiModel> Aspose::Words::AI::OpenAiModel::WithOrganization(const System::String &organizationId)
```


## أمثلة



يُظهر كيفية تلخيص النص باستخدام نماذج OpenAI و Google.
```cpp
auto firstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto secondDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// استخدم نماذج اللغة التوليدية من OpenAI أو Google.
System::SharedPtr<Aspose::Words::AI::AiModel> model = (System::ExplicitCast<Aspose::Words::AI::OpenAiModel>(Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey)))->WithOrganization(u"Organization")->WithProject(u"Project");

auto options = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Short);
System::SharedPtr<Aspose::Words::Document> oneDocumentSummary = model->Summarize(firstDoc, options);
oneDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.One.docx");

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Long);
System::SharedPtr<Aspose::Words::Document> multiDocumentSummary = model->Summarize(System::MakeArray<System::SharedPtr<Aspose::Words::Document>>({firstDoc, secondDoc}), options);
multiDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.Multi.docx");
```

## انظر أيضًا

* Class [OpenAiModel](../)
* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
