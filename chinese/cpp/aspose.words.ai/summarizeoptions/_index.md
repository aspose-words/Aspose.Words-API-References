---
title: "Aspose::Words::AI::SummarizeOptions class"
linktitle: "SummarizeOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::AI::SummarizeOptions class. 允许在 C++ 中指定用于摘要文档内容的各种选项。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.ai/summarizeoptions/
---
## SummarizeOptions class


允许指定用于摘要文档内容的各种选项。

```cpp
class SummarizeOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_SummaryLength](./get_summarylength/)() const | 允许指定摘要长度。默认值是 [Medium](../summarylength/)。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SummaryLength](./set_summarylength/)(Aspose::Words::AI::SummaryLength) | 用于设置 [Aspose::Words::AI::SummarizeOptions::get_SummaryLength](./get_summarylength/)。 |
| [SummarizeOptions](./summarizeoptions/)() | 初始化一个新的 [SummarizeOptions](./) 类实例。 |
| static [Type](./type/)() |  |

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
