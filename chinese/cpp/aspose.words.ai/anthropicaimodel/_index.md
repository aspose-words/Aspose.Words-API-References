---
title: "Aspose::Words::AI::AnthropicAiModel 类"
linktitle: "AnthropicAiModel"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::AI::AnthropicAiModel 类。一个抽象类，表示在 C++ 的 Aspose.Words 中与 Anthropic 的 AI 模型的集成。"
type: docs
weight: 1250
url: /zh/cpp/aspose.words.ai/anthropicaimodel/
---
## AnthropicAiModel class


一个抽象类，表示在 [Aspose.Words](../../aspose.words/) 中与 Anthropic 的 [AI](../) 模型的集成。

```cpp
class AnthropicAiModel : public Aspose::Words::AI::AiModel
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [AnthropicAiModel](./anthropicaimodel/)() |  |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | 检查提供的文档的语法。此操作利用已连接的 [AI](../) 模型来检查文档的语法。 |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | 创建一个新的 [AiModel](../aimodel/) 类实例。 |
| [get_Timeout](../aimodel/get_timeout/)() const | 获取或设置在请求 [AI](../) 模型超时之前等待的毫秒数。默认值为 100,000 毫秒（100 秒）。 |
| [get_Url](./get_url/)() override | 获取模型的 URL。默认值为 "https://api.anthropic.com/"。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | 用于设置 [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/) 的 setter。 |
| [set_Url](./set_url/)(System::String) override | 设置模型的 URL。默认值为 "https://api.anthropic.com/"。 |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | 生成指定文档的摘要，并提供调整摘要长度的选项。此操作利用已连接的 [AI](../) 模型进行内容处理。 |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | 为文档数组生成摘要，并提供控制摘要长度及其他设置的选项。此方法利用已连接的 [AI](../) 模型处理数组中的每个文档。 |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | 将提供的文档翻译成指定的目标语言。此操作利用已连接的 [AI](../) 模型进行内容翻译。 |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | 为模型设置指定的 API 密钥。 |
## 另见

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
