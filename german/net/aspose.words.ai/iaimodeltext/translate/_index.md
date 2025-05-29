---
title: IAiModelText.Translate
linktitle: Translate
articleTitle: Translate
second_title: Aspose.Words für .NET
description: Übersetzen Sie Dokumente mühelos mit unserer IAiModelText Translate-Methode. Nutzen Sie KI für präzise und schnelle Übersetzungen in Ihrer gewünschten Sprache.
type: docs
weight: 30
url: /de/net/aspose.words.ai/iaimodeltext/translate/
---
## IAiModelText.Translate method

Übersetzt das bereitgestellte Dokument in die angegebene Zielsprache. Dieser Vorgang nutzt das verbundene KI-Modell zur Inhaltsübersetzung.

```csharp
public Document Translate(Document sourceDocument, Language targetLanguage)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sourceDocument | Document | Das zu übersetzende Dokument. |
| targetLanguage | Language | Die Sprache, in die das Dokument übersetzt wird. |

### Rückgabewert

Ein neues[`Document`](../../../aspose.words/document/)Objekt, das das übersetzte Dokument enthält.

## Beispiele

Zeigt, wie Text mithilfe von Google-Modellen übersetzt wird.

```csharp
Document doc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Verwenden Sie generative Sprachmodelle von Google.
IAiModelText model = (GoogleAiModel)AiModel.Create(AiModelType.Gemini15Flash).WithApiKey(apiKey);

Document translatedDoc = model.Translate(doc, Language.Arabic);
translatedDoc.Save(ArtifactsDir + "AI.AiTranslate.docx");
```

### Siehe auch

* class [Document](../../../aspose.words/document/)
* enum [Language](../../language/)
* interface [IAiModelText](../)
* namensraum [Aspose.Words.AI](../../../aspose.words.ai/)
* Montage [Aspose.Words](../../../)
