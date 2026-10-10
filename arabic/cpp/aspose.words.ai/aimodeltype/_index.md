---
title: "تعداد Aspose::Words::AI::AiModelType"
linktitle: "AiModelType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "تعداد Aspose::Words::AI::AiModelType. يمثل أنواع AiModel التي يمكن دمجها في سير عمل معالجة المستندات في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.ai/aimodeltype/
---
## AiModelType enum


يمثل أنواع [AiModel](../aimodel/) التي يمكن دمجها في سير عمل معالجة المستندات.

```cpp
enum class AiModelType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Gpt4O | 0 | نوع نموذج توليدي GPT-4o. |
| Gpt4OMini | 1 | نوع نموذج توليدي GPT-4o mini. |
| Gpt4Turbo | 2 | نوع نموذج توليدي GPT-4 Turbo. |
| Gpt35Turbo | 3 | نوع نموذج توليدي GPT-3.5 Turbo. |
| GeminiFlashLatest | 4 | نوع نموذج توليدي Gemini Flash الإصدار الأخير. |
| GeminiProLatest | 6 | نوع نموذج توليدي Gemini Pro الإصدار الأخير. |
| Claude35Sonnet | 7 | Claude 3.5 Sonnet نوع نموذج توليدي. |
| Claude35Haiku | 8 | Claude 3.5 Haiku نوع نموذج توليدي. |
| Claude3Opus | 9 | Claude 3 Opus نوع نموذج توليدي. |
| Claude3Sonnet | 10 | Claude 3 Sonnet نوع نموذج توليدي. |
| Claude3Haiku | 11 | Claude 3 Haiku نوع نموذج توليدي. |


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

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
