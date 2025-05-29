---
title: IAiModelText.CheckGrammar
linktitle: CheckGrammar
articleTitle: CheckGrammar
second_title: Aspose.Words för .NET
description: Förbättra ditt skrivande med IAiModelTexts CheckGrammar-metod. Förbättra enkelt dokumentnoggrannheten med avancerad AI-grammatikkontroll.
type: docs
weight: 10
url: /sv/net/aspose.words.ai/iaimodeltext/checkgrammar/
---
## IAiModelText.CheckGrammar method

Kontrollerar grammatiken i det angivna dokumentet. Den här åtgärden utnyttjar den anslutna AI-modellen för att kontrollera dokumentets grammatik.

```csharp
public Document CheckGrammar(Document sourceDocument, CheckGrammarOptions options = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| sourceDocument | Document | Dokumentet kontrolleras för grammatik. |
| options | CheckGrammarOptions | Valfria inställningar för att styra hur grammatik kontrolleras. |

### Returvärde

En ny[`Document`](../../../aspose.words/document/) med kontrollerad grammatik.

## Exempel

Visar hur man kontrollerar grammatiken i ett dokument.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Använd generativa språkmodeller från OpenAI.
IAiModelText model = (OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey);

CheckGrammarOptions grammarOptions = new CheckGrammarOptions();
grammarOptions.ImproveStylistics = true;

Document proofedDoc = model.CheckGrammar(doc, grammarOptions);
proofedDoc.Save(ArtifactsDir + "AI.AiGrammar.docx");
```

### Se även

* class [Document](../../../aspose.words/document/)
* class [CheckGrammarOptions](../../checkgrammaroptions/)
* interface [IAiModelText](../)
* namnutrymme [Aspose.Words.AI](../../../aspose.words.ai/)
* hopsättning [Aspose.Words](../../../)
