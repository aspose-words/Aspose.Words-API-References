---
title: "Aspose::Words::AI::AiModel::Translate 方法"
linktitle: "翻译"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::AI::AiModel::Translate 方法。 将提供的文档翻译成指定的目标语言。 此操作在 C++ 中利用已连接的 AI 模型进行内容翻译。"
type: docs
weight: 4667
url: /zh/cpp/aspose.words.ai/aimodel/translate/
---
## AiModel::Translate method


将提供的文档翻译成指定的目标语言。此操作利用已连接的 [AI](../../) 模型进行内容翻译。

```cpp
virtual System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AiModel::Translate(System::SharedPtr<Aspose::Words::Document> sourceDocument, Aspose::Words::AI::Language targetLanguage)=0
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | 待翻译的文档。 |
| targetLanguage | Aspose::Words::AI::Language | 文档将被翻译成的语言。 |

### ReturnValue

一个包含已翻译文档的新 [Document](../../../aspose.words/document/) 对象。

## 示例



展示如何使用 Google 模型翻译文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// 使用 Google 生成式语言模型。
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::GeminiFlashLatest)->WithApiKey(apiKey);

System::SharedPtr<Aspose::Words::Document> translatedDoc = model->Translate(doc, Aspose::Words::AI::Language::Arabic);
translatedDoc->Save(get_ArtifactsDir() + u"AI.AiTranslate.docx");
```

## 另见

* Class [Document](../../../aspose.words/document/)
* Enum [Language](../../language/)
* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
