---
title: CheckGrammarOptions Class
linktitle: CheckGrammarOptions
articleTitle: CheckGrammarOptions
second_title: Aspose.Words för .NET
description: Optimera dina dokument med Aspose.Words.AI.CheckGrammarOptions. Upptäck anpassningsbara AI-grammatikkontroller för felfritt skrivande och förbättrad tydlighet.
type: docs
weight: 50
url: /sv/net/aspose.words.ai/checkgrammaroptions/
---
## CheckGrammarOptions class

Gör det möjligt att ange olika alternativ vid grammatikkontroll i ett dokument med hjälp av AI.

```csharp
public class CheckGrammarOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [CheckGrammarOptions](checkgrammaroptions/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [ImproveStylistics](../../aspose.words.ai/checkgrammaroptions/improvestylistics/) { get; set; } | Gör det möjligt att ange om AI kommer att försöka förbättra stilen i den text som korrekturläses. Standardvärdet är`falsk` . |
| [MakeRevisions](../../aspose.words.ai/checkgrammaroptions/makerevisions/) { get; set; } | Gör det möjligt att ange om antingen slutgiltigt eller reviderat dokument ska returneras med korrekturläst text. Standardvärdet är`falsk` . |
| [PreserveFormatting](../../aspose.words.ai/checkgrammaroptions/preserveformatting/) { get; set; } | Gör det möjligt att ange antingen[`CheckGrammar`](../iaimodeltext/checkgrammar/)kommer att försöka bevara layout och formatering av originaldokumentet, eller inte. Standardvärdet är`sann` . |

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

* namnutrymme [Aspose.Words.AI](../../aspose.words.ai/)
* hopsättning [Aspose.Words](../../)
