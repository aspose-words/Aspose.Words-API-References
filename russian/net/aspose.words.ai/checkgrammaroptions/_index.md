---
title: CheckGrammarOptions Class
linktitle: CheckGrammarOptions
articleTitle: CheckGrammarOptions
second_title: Aspose.Words для .NET
description: Оптимизируйте свои документы с помощью Aspose.Words.AI.CheckGrammarOptions. Откройте для себя настраиваемые проверки грамматики ИИ для безупречного письма и повышения ясности.
type: docs
weight: 50
url: /ru/net/aspose.words.ai/checkgrammaroptions/
---
## CheckGrammarOptions class

Позволяет указать различные параметры при проверке грамматики документа с использованием ИИ.

```csharp
public class CheckGrammarOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [CheckGrammarOptions](checkgrammaroptions/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [ImproveStylistics](../../aspose.words.ai/checkgrammaroptions/improvestylistics/) { get; set; } | Позволяет указать, будет ли ИИ пытаться улучшить стилистику проверяемого текста. Значение по умолчанию:`ЛОЖЬ` . |
| [MakeRevisions](../../aspose.words.ai/checkgrammaroptions/makerevisions/) { get; set; } | Позволяет указать окончательный или пересмотренный документ, который будет возвращен с проверенным текстом. Значение по умолчанию:`ЛОЖЬ` . |
| [PreserveFormatting](../../aspose.words.ai/checkgrammaroptions/preserveformatting/) { get; set; } | Позволяет указать либо[`CheckGrammar`](../iaimodeltext/checkgrammar/)попытается сохранить макет и форматирование исходного документа, или нет. Значение по умолчанию:`истинный` . |

## Примеры

Показывает, как проверить грамматику документа.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Используйте генеративные языковые модели OpenAI.
IAiModelText model = (OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey);

CheckGrammarOptions grammarOptions = new CheckGrammarOptions();
grammarOptions.ImproveStylistics = true;

Document proofedDoc = model.CheckGrammar(doc, grammarOptions);
proofedDoc.Save(ArtifactsDir + "AI.AiGrammar.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.AI](../../aspose.words.ai/)
* сборка [Aspose.Words](../../)
