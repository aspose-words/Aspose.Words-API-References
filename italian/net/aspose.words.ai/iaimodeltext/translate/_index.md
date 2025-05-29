---
title: IAiModelText.Translate
linktitle: Translate
articleTitle: Translate
second_title: Aspose.Words per .NET
description: Traduci documenti senza sforzo con il nostro metodo IAiModelText Translate. Sfrutta l'intelligenza artificiale per traduzioni accurate e veloci nella lingua desiderata.
type: docs
weight: 30
url: /it/net/aspose.words.ai/iaimodeltext/translate/
---
## IAiModelText.Translate method

Traduce il documento fornito nella lingua di destinazione specificata. Questa operazione sfrutta il modello di intelligenza artificiale connesso per la traduzione dei contenuti.

```csharp
public Document Translate(Document sourceDocument, Language targetLanguage)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sourceDocument | Document | Il documento da tradurre. |
| targetLanguage | Language | La lingua in cui verrà tradotto il documento. |

### Valore di ritorno

Un nuovo[`Document`](../../../aspose.words/document/)oggetto contenente il documento tradotto.

## Esempi

Mostra come tradurre il testo utilizzando i modelli di Google.

```csharp
Document doc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Utilizza i modelli linguistici generativi di Google.
IAiModelText model = (GoogleAiModel)AiModel.Create(AiModelType.Gemini15Flash).WithApiKey(apiKey);

Document translatedDoc = model.Translate(doc, Language.Arabic);
translatedDoc.Save(ArtifactsDir + "AI.AiTranslate.docx");
```

### Guarda anche

* class [Document](../../../aspose.words/document/)
* enum [Language](../../language/)
* interface [IAiModelText](../)
* spazio dei nomi [Aspose.Words.AI](../../../aspose.words.ai/)
* assemblea [Aspose.Words](../../../)
