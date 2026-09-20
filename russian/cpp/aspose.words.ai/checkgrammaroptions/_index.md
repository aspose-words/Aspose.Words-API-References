---
title: "Aspose::Words::AI::CheckGrammarOptions класс"
linktitle: "CheckGrammarOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::AI::CheckGrammarOptions класс. Позволяет задавать различные параметры при проверке грамматики документа с использованием AI в C++."
type: docs
weight: 1500
url: /ru/cpp/aspose.words.ai/checkgrammaroptions/
---
## CheckGrammarOptions class


Позволяет задавать различные параметры при проверке грамматики документа с использованием [AI](../).

```cpp
class CheckGrammarOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [CheckGrammarOptions](./checkgrammaroptions/)() |  |
| [get_ImproveStylistics](./get_improvestylistics/)() const | Позволяет указать, что [AI](../) будет пытаться улучшить стилистику проверяемого текста. Значение по умолчанию — **false**. |
| [get_MakeRevisions](./get_makerevisions/)() const | Позволяет указать, какой документ — окончательный или исправленный — будет возвращён с проверенным текстом. Значение по умолчанию — **false**. |
| [get_PreserveFormatting](./get_preserveformatting/)() const | Позволяет указать, будет ли [CheckGrammar()](../aimodel/checkgrammar/) пытаться сохранить макет и форматирование оригинального документа или нет. Значение по умолчанию — **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ImproveStylistics](./set_improvestylistics/)(bool) | Позволяет указать, что [AI](../) будет пытаться улучшить стилистику проверяемого текста. Значение по умолчанию — **false**. |
| [set_MakeRevisions](./set_makerevisions/)(bool) | Позволяет указать, какой документ — окончательный или исправленный — будет возвращён с проверенным текстом. Значение по умолчанию — **false**. |
| [set_PreserveFormatting](./set_preserveformatting/)(bool) | Позволяет указать, будет ли [CheckGrammar()](../aimodel/checkgrammar/) пытаться сохранить макет и форматирование оригинального документа или нет. Значение по умолчанию — **true**. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
