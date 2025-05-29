---
title: SummarizeOptions.SummaryLength
linktitle: SummaryLength
articleTitle: SummaryLength
second_title: Aspose.Words pour .NET
description: Contrôlez la longueur de votre résumé avec la propriété SummarizeOptions SummaryLength. Personnalisez votre contenu pour plus de clarté et d'impact. La valeur par défaut est Moyenne.
type: docs
weight: 20
url: /fr/net/aspose.words.ai/summarizeoptions/summarylength/
---
## SummarizeOptions.SummaryLength property

Permet de spécifier la longueur du résumé. La valeur par défaut estMedium .

```csharp
public SummaryLength SummaryLength { get; set; }
```

## Exemples

Montre comment résumer du texte à l'aide des modèles OpenAI et Google.

```csharp
Document firstDoc = new Document(MyDir + "Big document.docx");
Document secondDoc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Utilisez les modèles de langage génératifs OpenAI ou Google.
IAiModelText model = ((OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey)).WithOrganization("Organization").WithProject("Project");

SummarizeOptions options = new SummarizeOptions();

options.SummaryLength = SummaryLength.Short;
Document oneDocumentSummary = model.Summarize(firstDoc, options);
oneDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.One.docx");

options.SummaryLength = SummaryLength.Long;
Document multiDocumentSummary = model.Summarize(new Document[] { firstDoc, secondDoc }, options);
multiDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.Multi.docx");
```

### Voir également

* enum [SummaryLength](../../summarylength/)
* class [SummarizeOptions](../)
* espace de noms [Aspose.Words.AI](../../../aspose.words.ai/)
* Assemblée [Aspose.Words](../../../)
