---
title: IAiModelText.CheckGrammar
linktitle: CheckGrammar
articleTitle: CheckGrammar
second_title: Aspose.Words per .NET
description: Migliora la tua scrittura con il metodo CheckGrammar di IAiModelText. Migliora senza sforzo la precisione dei documenti utilizzando un controllo grammaticale avanzato basato sull'intelligenza artificiale.
type: docs
weight: 10
url: /it/net/aspose.words.ai/iaimodeltext/checkgrammar/
---
## IAiModelText.CheckGrammar method

Controlla la grammatica del documento fornito. Questa operazione sfrutta il modello di intelligenza artificiale connesso per controllare la grammatica del documento.

```csharp
public Document CheckGrammar(Document sourceDocument, CheckGrammarOptions options = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sourceDocument | Document | Il documento viene sottoposto a controllo grammaticale. |
| options | CheckGrammarOptions | Impostazioni facoltative per controllare il modo in cui verrà controllata la grammatica. |

### Valore di ritorno

Un nuovo[`Document`](../../../aspose.words/document/) con grammatica controllata.

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

* class [Document](../../../aspose.words/document/)
* class [CheckGrammarOptions](../../checkgrammaroptions/)
* interface [IAiModelText](../)
* spazio dei nomi [Aspose.Words.AI](../../../aspose.words.ai/)
* assemblea [Aspose.Words](../../../)
