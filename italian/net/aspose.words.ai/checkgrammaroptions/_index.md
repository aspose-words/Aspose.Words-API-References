---
title: CheckGrammarOptions Class
linktitle: CheckGrammarOptions
articleTitle: CheckGrammarOptions
second_title: Aspose.Words per .NET
description: Ottimizza i tuoi documenti con Aspose.Words.AI.CheckGrammarOptions. Scopri i controlli grammaticali personalizzabili basati sull'intelligenza artificiale per una scrittura impeccabile e una maggiore chiarezza.
type: docs
weight: 50
url: /it/net/aspose.words.ai/checkgrammaroptions/
---
## CheckGrammarOptions class

Consente di specificare varie opzioni durante il controllo grammaticale di un documento tramite AI.

```csharp
public class CheckGrammarOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [CheckGrammarOptions](checkgrammaroptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [ImproveStylistics](../../aspose.words.ai/checkgrammaroptions/improvestylistics/) { get; set; } | Consente di specificare se l'IA tenterà di migliorare lo stile del testo in fase di correzione. Il valore predefinito è`falso` . |
| [MakeRevisions](../../aspose.words.ai/checkgrammaroptions/makerevisions/) { get; set; } | Consente di specificare il documento finale o rivisto da restituire con testo corretto. Il valore predefinito è`falso` . |
| [PreserveFormatting](../../aspose.words.ai/checkgrammaroptions/preserveformatting/) { get; set; } | Consente di specificare[`CheckGrammar`](../iaimodeltext/checkgrammar/)proverà a preservare il layout e la formattazione del documento originale, oppure no. Il valore predefinito è`VERO` . |

## Esempi

Mostra come controllare la grammatica di un documento.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Utilizza modelli linguistici generativi OpenAI.
IAiModelText model = (OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey);

CheckGrammarOptions grammarOptions = new CheckGrammarOptions();
grammarOptions.ImproveStylistics = true;

Document proofedDoc = model.CheckGrammar(doc, grammarOptions);
proofedDoc.Save(ArtifactsDir + "AI.AiGrammar.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.AI](../../aspose.words.ai/)
* assemblea [Aspose.Words](../../)
