---
title: IAiModelText.Translate
linktitle: Translate
articleTitle: Translate
second_title: Aspose.Words for .NET
description: IAiModelText Translate method. Translates the provided document into the specified target language. This operation leverages the connected AI model for content translating in C#.
type: docs
weight: 20
url: /net/aspose.words.ai/iaimodeltext/translate/
---
## IAiModelText.Translate method

Translates the provided document into the specified target language. This operation leverages the connected AI model for content translating.

```csharp
public Document Translate(Document sourceDocument, Language targetLanguage)
```

| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocument | Document | The document to be translated. |
| targetLanguage | Language | The language into which the document will be translated. |

### Return Value

A new [`Document`](../../../aspose.words/document/) object containing the translated document.

## Examples

Shows how to translate text using Google models.

```csharp
Document doc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Use Google generative language models.
IAiModelText model = (IAiModelText)AiModel.Create(AiModelType.Gemini15Flash).WithApiKey(apiKey);

Document translatedDoc = model.Translate(doc, Language.Arabic);
translatedDoc.Save(ArtifactsDir + "AI.AiTranslate.docx");
```

### See Also

* class [Document](../../../aspose.words/document/)
* enum [Language](../../language/)
* interface [IAiModelText](../)
* namespace [Aspose.Words.AI](../../../aspose.words.ai/)
* assembly [Aspose.Words](../../../)
