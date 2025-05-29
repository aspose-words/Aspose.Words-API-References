---
title: IAiModelText.Translate
linktitle: Translate
articleTitle: Translate
second_title: Aspose.Words для .NET
description: Переводите документы без усилий с помощью нашего метода IAiModelText Translate. Используйте ИИ для точных и быстрых переводов на нужный вам язык.
type: docs
weight: 30
url: /ru/net/aspose.words.ai/iaimodeltext/translate/
---
## IAiModelText.Translate method

Переводит предоставленный документ на указанный целевой язык. Эта операция использует подключенную модель ИИ для перевода контента.

```csharp
public Document Translate(Document sourceDocument, Language targetLanguage)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| sourceDocument | Document | Документ, подлежащий переводу. |
| targetLanguage | Language | Язык, на который будет переведен документ. |

### Возвращаемое значение

Новый[`Document`](../../../aspose.words/document/)объект, содержащий переведенный документ.

## Примеры

Показывает, как переводить текст с использованием моделей Google.

```csharp
Document doc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Используйте генеративные языковые модели Google.
IAiModelText model = (GoogleAiModel)AiModel.Create(AiModelType.Gemini15Flash).WithApiKey(apiKey);

Document translatedDoc = model.Translate(doc, Language.Arabic);
translatedDoc.Save(ArtifactsDir + "AI.AiTranslate.docx");
```

### Смотрите также

* class [Document](../../../aspose.words/document/)
* enum [Language](../../language/)
* interface [IAiModelText](../)
* пространство имен [Aspose.Words.AI](../../../aspose.words.ai/)
* сборка [Aspose.Words](../../../)
