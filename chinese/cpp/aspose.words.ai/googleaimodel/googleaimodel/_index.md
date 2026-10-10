---
title: "Aspose::Words::AI::GoogleAiModel::GoogleAiModel 构造函数"
linktitle: "GoogleAiModel"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::AI::GoogleAiModel::GoogleAiModel 构造函数。初始化 GoogleAiModel 类的新实例，在 C++ 中使用。"
type: docs
weight: 1500
url: /zh/cpp/aspose.words.ai/googleaimodel/googleaimodel/
---
## GoogleAiModel::GoogleAiModel(const System::String\&) constructor


初始化 [GoogleAiModel](../) 类的新实例。

```cpp
Aspose::Words::AI::GoogleAiModel::GoogleAiModel(const System::String &name)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| name | const System::String\& | 模型的名称。例如，gemini-2.5-flash。 |

## 示例



展示如何使用 google [AI](../../) 模型。
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## 另见

* Class [GoogleAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## GoogleAiModel::GoogleAiModel(const System::String\&, const System::String\&) constructor


初始化 [GoogleAiModel](../) 类的新实例。

```cpp
Aspose::Words::AI::GoogleAiModel::GoogleAiModel(const System::String &name, const System::String &apiKey)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| name | const System::String\& | 模型的名称。例如，gemini-2.5-flash。 |
| apiKey | const System::String\& | 用于使用 Gemini API 的 API 密钥。详情请参阅 [https://ai.google.dev/gemini-api/docs/api-key](https://ai.google.dev/gemini-api/docs/api-key)。 |

## 示例



展示如何使用 google [AI](../../) 模型。
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## 另见

* Class [GoogleAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
