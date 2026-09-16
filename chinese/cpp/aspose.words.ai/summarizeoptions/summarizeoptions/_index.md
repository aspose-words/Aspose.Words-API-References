---
title: "Aspose::Words::AI::SummarizeOptions::SummarizeOptions 构造函数"
linktitle: "SummarizeOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::AI::SummarizeOptions::SummarizeOptions 构造函数。初始化 SummarizeOptions 类的新实例（C++）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.ai/summarizeoptions/summarizeoptions/
---
## SummarizeOptions::SummarizeOptions constructor


初始化 [SummarizeOptions](../) 类的新实例。

```cpp
Aspose::Words::AI::SummarizeOptions::SummarizeOptions()
```


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

* Class [SummarizeOptions](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
