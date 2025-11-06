---
title: AiModel.Translate
linktitle: Translate
articleTitle: Translate
second_title: Aspose.Words for .NET
description: Professional document translation API supporting multiple languages. Translate Word documents accurately with AI-powered language processing.
type: docs
weight: 60
url: /net/aspose.words.ai/aimodel/translate/
---
## AiModel.Translate method

Translates the provided document into the specified target language. This operation leverages the connected AI model for content translating.

```csharp
public abstract Document Translate(Document sourceDocument, Language targetLanguage)
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
AiModel model = AiModel.Create(AiModelType.Gemini15Flash).WithApiKey(apiKey);

Document translatedDoc = model.Translate(doc, Language.Arabic);
translatedDoc.Save(ArtifactsDir + "AI.AiTranslate.docx");
```

### See Also

* class [Document](../../../aspose.words/document/)
* enum [Language](../../language/)
* class [AiModel](../)
* namespace [Aspose.Words.AI](../../../aspose.words.ai/)
* assembly [Aspose.Words](../../../)
