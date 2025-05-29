---
title: IAiModelText.CheckGrammar
linktitle: CheckGrammar
articleTitle: CheckGrammar
second_title: Aspose.Words für .NET
description: Verbessern Sie Ihre Texte mit der CheckGrammar-Methode von IAiModelText. Verbessern Sie mühelos die Genauigkeit Ihrer Dokumente mithilfe der erweiterten KI-Grammatikprüfung.
type: docs
weight: 10
url: /de/net/aspose.words.ai/iaimodeltext/checkgrammar/
---
## IAiModelText.CheckGrammar method

Überprüft die Grammatik des bereitgestellten Dokuments. Dieser Vorgang nutzt das verbundene KI-Modell zur Überprüfung der Grammatik des Dokuments.

```csharp
public Document CheckGrammar(Document sourceDocument, CheckGrammarOptions options = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sourceDocument | Document | Das Dokument wird auf Grammatik geprüft. |
| options | CheckGrammarOptions | Optionale Einstellungen zur Steuerung der Grammatikprüfung. |

### Rückgabewert

Ein neues[`Document`](../../../aspose.words/document/) mit geprüfter Grammatik.

## Beispiele

Zeigt, wie die Grammatik eines Dokuments überprüft wird.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Verwenden Sie generative Sprachmodelle von OpenAI.
IAiModelText model = (OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey);

CheckGrammarOptions grammarOptions = new CheckGrammarOptions();
grammarOptions.ImproveStylistics = true;

Document proofedDoc = model.CheckGrammar(doc, grammarOptions);
proofedDoc.Save(ArtifactsDir + "AI.AiGrammar.docx");
```

### Siehe auch

* class [Document](../../../aspose.words/document/)
* class [CheckGrammarOptions](../../checkgrammaroptions/)
* interface [IAiModelText](../)
* namensraum [Aspose.Words.AI](../../../aspose.words.ai/)
* Montage [Aspose.Words](../../../)
