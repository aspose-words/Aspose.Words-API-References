---
title: "Aspose::Words::AI::AiModel::CheckGrammar method"
linktitle: "CheckGrammar"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::AI::AiModel::CheckGrammar 方法。检查提供的文档的语法。此操作在 C++ 中利用已连接的 AI 模型对文档语法进行检查。"
type: docs
weight: 2500
url: /zh/cpp/aspose.words.ai/aimodel/checkgrammar/
---
## AiModel::CheckGrammar method


检查提供的文档的语法。此操作利用已连接的 [AI](../../) 模型对文档语法进行检查。

```cpp
virtual System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AiModel::CheckGrammar(System::SharedPtr<Aspose::Words::Document> sourceDocument, System::SharedPtr<Aspose::Words::AI::CheckGrammarOptions> options=nullptr)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | 正在检查语法的文档。 |
| options | System::SharedPtr\\<Aspose::Words::AI::CheckGrammarOptions\\> | 用于控制语法检查方式的可选设置。 |

### ReturnValue

一个已检查语法的新 [Document](../../../aspose.words/document/)。

## 示例



展示如何检查文档的语法。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// 使用 OpenAI 生成式语言模型。
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);

auto grammarOptions = System::MakeObject<Aspose::Words::AI::CheckGrammarOptions>();
grammarOptions->set_ImproveStylistics(true);

System::SharedPtr<Aspose::Words::Document> proofedDoc = model->CheckGrammar(doc, grammarOptions);
proofedDoc->Save(get_ArtifactsDir() + u"AI.AiGrammar.docx");
```

## 另见

* Class [Document](../../../aspose.words/document/)
* Class [CheckGrammarOptions](../../checkgrammaroptions/)
* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
