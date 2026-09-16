---
title: "Aspose::Words::AI::OpenAiModel::OpenAiModel 构造函数"
linktitle: "OpenAiModel"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::AI::OpenAiModel::OpenAiModel 构造函数。初始化 OpenAiModel 类在 C++ 中的新实例。"
type: docs
weight: 1334
url: /zh/cpp/aspose.words.ai/openaimodel/openaimodel/
---
## OpenAiModel::OpenAiModel(const System::String\&) constructor


初始化 [OpenAiModel](../) 类的新实例。

```cpp
Aspose::Words::AI::OpenAiModel::OpenAiModel(const System::String &name)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| name | const System::String\& | 模型的名称。例如，gpt-5.2-chat-latest。 |

## 另见

* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## OpenAiModel::OpenAiModel(const System::String\&, const System::String\&) constructor


初始化 [OpenAiModel](../) 类的新实例。

```cpp
Aspose::Words::AI::OpenAiModel::OpenAiModel(const System::String &name, const System::String &apiKey)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| name | const System::String\& | 模型的名称。例如，gpt-5.2-chat-latest。 |
| apiKey | const System::String\& | 用于 OpenAi API 的 API 密钥。 |

## 示例



展示如何直接使用 API 密钥和模型名称创建 OpenAI 模型实例。
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// 使用带有模型名称和 API 密钥的构造函数创建 OpenAI 模型实例。
auto model = System::MakeObject<Aspose::Words::AI::OpenAiModel>(u"gpt-4o-mini", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
// 使用短摘要长度的 OpenAI 模型对文档进行摘要。
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);

summary->Save(get_ArtifactsDir() + u"OpenAiModel.OpenAiModelConstructor.docx");
```

## 另见

* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
