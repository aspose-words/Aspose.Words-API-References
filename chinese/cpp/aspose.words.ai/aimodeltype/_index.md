---
title: "Aspose::Words::AI::AiModelType enum"
linktitle: "AiModelType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::AI::AiModelType enum. 表示可以集成到 C++ 文档处理工作流中的 AiModel 类型。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.ai/aimodeltype/
---
## AiModelType enum


表示可以集成到文档处理工作流中的 [AiModel](../aimodel/) 类型。

```cpp
enum class AiModelType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Gpt4O | 0 | GPT-4o 生成模型类型。 |
| Gpt4OMini | 1 | GPT-4o mini 生成模型类型。 |
| Gpt4Turbo | 2 | GPT-4 Turbo 生成模型类型。 |
| Gpt35Turbo | 3 | GPT-3.5 Turbo 生成模型类型。 |
| GeminiFlashLatest | 4 | Gemini Flash 最新发布的生成模型类型。 |
| GeminiProLatest | 6 | Gemini Pro 最新发布的生成模型类型。 |
| Claude35Sonnet | 7 | Claude 3.5 Sonnet 生成模型类型。 |
| Claude35Haiku | 8 | Claude 3.5 Haiku 生成模型类型。 |
| Claude3Opus | 9 | Claude 3 Opus 生成模型类型。 |
| Claude3Sonnet | 10 | Claude 3 Sonnet 生成模型类型。 |
| Claude3Haiku | 11 | Claude 3 Haiku 生成模型类型。 |


## 示例



展示如何使用 OpenAI 和 Google 模型对文本进行摘要。
```cpp
auto firstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto secondDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// 使用 OpenAI 或 Google 生成式语言模型。
System::SharedPtr<Aspose::Words::AI::AiModel> model = (System::ExplicitCast<Aspose::Words::AI::OpenAiModel>(Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey)))->WithOrganization(u"Organization")->WithProject(u"Project");

auto options = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Short);
System::SharedPtr<Aspose::Words::Document> oneDocumentSummary = model->Summarize(firstDoc, options);
oneDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.One.docx");

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Long);
System::SharedPtr<Aspose::Words::Document> multiDocumentSummary = model->Summarize(System::MakeArray<System::SharedPtr<Aspose::Words::Document>>({firstDoc, secondDoc}), options);
multiDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.Multi.docx");
```

## 另见

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
