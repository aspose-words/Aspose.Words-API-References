---
title: "Aspose::Words::AI::GoogleAiModel 类"
linktitle: "GoogleAiModel"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::AI::GoogleAiModel 类。类表示在 C++ 中 Aspose.Words 中的 Google AI 模型（Gemini）集成。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.ai/googleaimodel/
---
## GoogleAiModel class


类表示 Google [AI](../) 模型（Gemini）在 [Aspose.Words](../../aspose.words/) 中的集成。

```cpp
class GoogleAiModel : public Aspose::Words::AI::AiModel
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | 检查提供的文档的语法。此操作利用已连接的 [AI](../) 模型来检查文档的语法。 |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | 创建一个新的 [AiModel](../aimodel/) 类实例。 |
| [get_Timeout](../aimodel/get_timeout/)() const | 获取或设置在请求 [AI](../) 模型超时之前等待的毫秒数。默认值为 100,000 毫秒（100 秒）。 |
| [get_Url](./get_url/)() override | 获取模型的 URL。默认值为 "https://generativelanguage.googleapis.com/v1beta/models/"。 |
| [GetType](./gettype/)() const override |  |
| [GoogleAiModel](./googleaimodel/)(const System::String\&) | 初始化 [GoogleAiModel](./) 类的新实例。 |
| [GoogleAiModel](./googleaimodel/)(const System::String\&, const System::String\&) | 初始化 [GoogleAiModel](./) 类的新实例。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | 用于设置 [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/) 的 setter。 |
| [set_Url](./set_url/)(System::String) override | 设置模型的 URL。默认值为 "https://generativelanguage.googleapis.com/v1beta/models/"。 |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | 汇总指定的 [Document](../../aspose.words/document/) 对象。 |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | 汇总指定的 [Document](../../aspose.words/document/) 对象。 |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | 翻译指定的文档。 |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | 为模型设置指定的 API 密钥。 |

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


展示如何使用 Google [AI](../) 模型。
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## 另见

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
