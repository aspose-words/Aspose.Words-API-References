---
title: IAiModelText.Translate
linktitle: Translate
articleTitle: Translate
second_title: Aspose.Words för .NET
description: Översätt dokument enkelt med vår IAiModelText Translate-metod. Utnyttja AI för korrekta och snabba översättningar till ditt önskade språk.
type: docs
weight: 30
url: /sv/net/aspose.words.ai/iaimodeltext/translate/
---
## IAiModelText.Translate method

Översätter det angivna dokumentet till det angivna målspråket. Denna åtgärd utnyttjar den anslutna AI-modellen för innehållsöversättning.

```csharp
public Document Translate(Document sourceDocument, Language targetLanguage)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| sourceDocument | Document | Dokumentet som ska översättas. |
| targetLanguage | Language | Det språk som dokumentet ska översättas till. |

### Returvärde

En ny[`Document`](../../../aspose.words/document/)objekt som innehåller det översatta dokumentet.

## Exempel

Visar hur man översätter text med hjälp av Google-modeller.

```csharp
Document doc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Använd Googles generativa språkmodeller.
IAiModelText model = (GoogleAiModel)AiModel.Create(AiModelType.Gemini15Flash).WithApiKey(apiKey);

Document translatedDoc = model.Translate(doc, Language.Arabic);
translatedDoc.Save(ArtifactsDir + "AI.AiTranslate.docx");
```

### Se även

* class [Document](../../../aspose.words/document/)
* enum [Language](../../language/)
* interface [IAiModelText](../)
* namnutrymme [Aspose.Words.AI](../../../aspose.words.ai/)
* hopsättning [Aspose.Words](../../../)
