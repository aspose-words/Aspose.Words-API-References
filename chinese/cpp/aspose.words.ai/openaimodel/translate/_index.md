---
title: "Aspose::Words::AI::OpenAiModel::Translate 方法"
linktitle: "翻译"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::AI::OpenAiModel::Translate 方法。将提供的文档翻译成指定的目标语言。此操作在 C++ 中利用已连接的 AI 模型进行内容翻译。"
type: docs
weight: 3667
url: /zh/cpp/aspose.words.ai/openaimodel/translate/
---
## OpenAiModel::Translate method


将提供的文档翻译成指定的目标语言。此操作利用已连接的 [AI](../../) 模型进行内容翻译。

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::OpenAiModel::Translate(System::SharedPtr<Aspose::Words::Document> sourceDocument, Aspose::Words::AI::Language targetLanguage) override
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | 待翻译的文档。 |
| targetLanguage | Aspose::Words::AI::Language | 文档将被翻译成的语言。 |

### ReturnValue

一个包含已翻译文档的新 [Document](../../../aspose.words/document/) 对象。

## 另见

* Class [Document](../../../aspose.words/document/)
* Enum [Language](../../language/)
* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
