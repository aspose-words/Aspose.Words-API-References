---
title: IAiModelText.CheckGrammar
linktitle: CheckGrammar
articleTitle: CheckGrammar
second_title: Aspose.Words для .NET
description: Улучшите свой текст с помощью метода CheckGrammar от IAiModelText. Легко повышайте точность документа с помощью расширенной проверки грамматики с помощью ИИ.
type: docs
weight: 10
url: /ru/net/aspose.words.ai/iaimodeltext/checkgrammar/
---
## IAiModelText.CheckGrammar method

Проверяет грамматику предоставленного документа. Эта операция использует подключенную модель ИИ для проверки грамматики документа.

```csharp
public Document CheckGrammar(Document sourceDocument, CheckGrammarOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| sourceDocument | Document | Документ проверяется на грамматику. |
| options | CheckGrammarOptions | Дополнительные настройки для управления проверкой грамматики. |

### Возвращаемое значение

Новый[`Document`](../../../aspose.words/document/) с проверенной грамматикой.

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

* class [Document](../../../aspose.words/document/)
* class [CheckGrammarOptions](../../checkgrammaroptions/)
* interface [IAiModelText](../)
* пространство имен [Aspose.Words.AI](../../../aspose.words.ai/)
* сборка [Aspose.Words](../../../)
