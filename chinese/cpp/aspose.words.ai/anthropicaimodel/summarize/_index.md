---
title: "Aspose::Words::AI::AnthropicAiModel::Summarize 方法"
linktitle: "摘要"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::AI::AnthropicAiModel::Summarize 方法。为文档数组生成摘要，可通过选项控制摘要长度和其他设置。此方法在 C++ 中使用已连接的 AI 模型处理数组中的每个文档。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.ai/anthropicaimodel/summarize/
---
## AnthropicAiModel::Summarize(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) method


为文档数组生成摘要，可通过选项控制摘要长度和其他设置。此方法利用已连接的 [AI](../../) 模型处理数组中的每个文档。

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AnthropicAiModel::Summarize(System::ArrayPtr<System::SharedPtr<Aspose::Words::Document>> sourceDocuments, System::SharedPtr<Aspose::Words::AI::SummarizeOptions> options=nullptr) override
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| sourceDocuments | System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\> | 待摘要的文档数组。 |
| options | System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\> | 用于控制摘要长度和其他参数的可选设置 |

### ReturnValue

文档内容的摘要版本。

## 另见

* Class [Document](../../../aspose.words/document/)
* Class [SummarizeOptions](../../summarizeoptions/)
* Class [AnthropicAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## AnthropicAiModel::Summarize(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) method


为指定文档生成摘要，可通过选项调整摘要长度。此操作利用已连接的 [AI](../../) 模型进行内容处理。

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AnthropicAiModel::Summarize(System::SharedPtr<Aspose::Words::Document> sourceDocument, System::SharedPtr<Aspose::Words::AI::SummarizeOptions> options=nullptr) override
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | 待摘要的文档。 |
| options | System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\> | 用于控制摘要长度和其他参数的可选设置。 |

### ReturnValue

文档内容的摘要版本。

## 另见

* Class [Document](../../../aspose.words/document/)
* Class [SummarizeOptions](../../summarizeoptions/)
* Class [AnthropicAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
