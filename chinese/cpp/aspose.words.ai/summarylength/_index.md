---
title: "Aspose::Words::AI::SummaryLength 枚举"
linktitle: "SummaryLength"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::AI::SummaryLength 枚举。枚举 C++ 中摘要的可能长度。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.ai/summarylength/
---
## SummaryLength enum


枚举摘要的可能长度。

```cpp
enum class SummaryLength
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| VeryShort | 0 | 尝试生成 1-2 句。 |
| Short | 1 | 尝试生成 3-4 句。 |
| Medium | 2 | 尝试生成 5-6 句。 |
| Long | 3 | 尝试生成 7-10 句。 |
| VeryLong | 4 | 尝试生成 11-20 句。 |


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
