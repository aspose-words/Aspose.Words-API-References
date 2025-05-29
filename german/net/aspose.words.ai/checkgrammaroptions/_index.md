---
title: CheckGrammarOptions Class
linktitle: CheckGrammarOptions
articleTitle: CheckGrammarOptions
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Dokumente mit Aspose.Words.AI.CheckGrammarOptions. Entdecken Sie anpassbare KI-Grammatikprüfungen für fehlerfreies Schreiben und verbesserte Klarheit.
type: docs
weight: 50
url: /de/net/aspose.words.ai/checkgrammaroptions/
---
## CheckGrammarOptions class

Ermöglicht die Angabe verschiedener Optionen bei der Grammatikprüfung eines Dokuments mithilfe von KI.

```csharp
public class CheckGrammarOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [CheckGrammarOptions](checkgrammaroptions/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ImproveStylistics](../../aspose.words.ai/checkgrammaroptions/improvestylistics/) { get; set; } | Ermöglicht die Angabe, ob die KI versucht, die Stilistik des zu prüfenden Textes zu verbessern. Der Standardwert ist`FALSCH` . |
| [MakeRevisions](../../aspose.words.ai/checkgrammaroptions/makerevisions/) { get; set; } | Ermöglicht die Angabe, ob das endgültige oder das überarbeitete Dokument mit Korrekturtext zurückgegeben werden soll. Der Standardwert ist`FALSCH` . |
| [PreserveFormatting](../../aspose.words.ai/checkgrammaroptions/preserveformatting/) { get; set; } | Ermöglicht die Angabe von[`CheckGrammar`](../iaimodeltext/checkgrammar/)versucht, Layout und Formatierung des Originaldokuments beizubehalten, oder nicht. Der Standardwert ist`WAHR` . |

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

* namensraum [Aspose.Words.AI](../../aspose.words.ai/)
* Montage [Aspose.Words](../../)
