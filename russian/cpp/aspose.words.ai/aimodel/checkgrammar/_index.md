---
title: "Метод Aspose::Words::AI::AiModel::CheckGrammar"
linktitle: "CheckGrammar"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::AI::AiModel::CheckGrammar. Проверяет грамматику предоставленного документа. Эта операция использует подключенную модель AI для проверки грамматики документа на C++."
type: docs
weight: 2500
url: /ru/cpp/aspose.words.ai/aimodel/checkgrammar/
---
## AiModel::CheckGrammar method


Проверяет грамматику предоставленного документа. Эта операция использует подключенную модель [AI](../../) для проверки грамматики документа.

```cpp
virtual System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AiModel::CheckGrammar(System::SharedPtr<Aspose::Words::Document> sourceDocument, System::SharedPtr<Aspose::Words::AI::CheckGrammarOptions> options=nullptr)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | Документ, проверяемый на грамматику. |
| параметры | System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\> | Необязательные настройки, определяющие, как будет проверяться грамматика. |

### ReturnValue

Новый [Document](../../../aspose.words/document/) с проверенной грамматикой.

## Примеры



Показывает, как проверить грамматику документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Используйте генеративные языковые модели OpenAI.
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);

auto grammarOptions = System::MakeObject<Aspose::Words::AI::CheckGrammarOptions>();
grammarOptions->set_ImproveStylistics(true);

System::SharedPtr<Aspose::Words::Document> proofedDoc = model->CheckGrammar(doc, grammarOptions);
proofedDoc->Save(get_ArtifactsDir() + u"AI.AiGrammar.docx");
```

## См. также

* Class [Document](../../../aspose.words/document/)
* Class [CheckGrammarOptions](../../checkgrammaroptions/)
* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
