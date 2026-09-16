---
title: "Aspose::Words::AI::AiModel 类"
linktitle: "AiModel"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::AI::AiModel 类。一个抽象类，表示在 C++ 的 Aspose.Words 中与各种 AI 模型的集成。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.ai/aimodel/
---
## AiModel class


一个抽象类，表示在 [Aspose.Words](../../aspose.words/) 中与各种 [AI](../) 模型的集成。

```cpp
class AiModel : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [CheckGrammar](./checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | 检查提供的文档的语法。此操作利用已连接的 [AI](../) 模型来检查文档的语法。 |
| static [Create](./create/)(Aspose::Words::AI::AiModelType) | 创建 [AiModel](./) 类的新实例。 |
| [get_Timeout](./get_timeout/)() const | 获取或设置在请求 [AI](../) 模型超时之前等待的毫秒数。默认值为 100,000 毫秒（100 秒）。 |
| virtual [get_Url](./get_url/)() | 获取或设置模型的 URL。默认值针对模型是特定的。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](./set_timeout/)(int32_t) | 用于 [Aspose::Words::AI::AiModel::get_Timeout](./get_timeout/) 的设置器。 |
| virtual [set_Url](./set_url/)(System::String) | 用于 [Aspose::Words::AI::AiModel::get_Url](./get_url/) 的设置器。 |
| virtual [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) | 生成指定文档的摘要，并提供调整摘要长度的选项。此操作利用已连接的 [AI](../) 模型进行内容处理。 |
| virtual [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) | 为文档数组生成摘要，并提供控制摘要长度及其他设置的选项。此方法利用已连接的 [AI](../) 模型处理数组中的每个文档。 |
| virtual [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) | 将提供的文档翻译成指定的目标语言。此操作利用已连接的 [AI](../) 模型进行内容翻译。 |
| static [Type](./type/)() |  |
| [WithApiKey](./withapikey/)(const System::String\&) | 为模型设置指定的 API 密钥。 |

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
