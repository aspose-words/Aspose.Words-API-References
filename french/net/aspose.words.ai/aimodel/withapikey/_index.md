---
title: AiModel.WithApiKey
linktitle: WithApiKey
articleTitle: WithApiKey
second_title: Aspose.Words pour .NET
description: Exploitez toute la puissance d'AiModel avec la méthode WithApiKey. Définissez facilement votre clé API pour des fonctionnalités améliorées et une intégration fluide.
type: docs
weight: 20
url: /fr/net/aspose.words.ai/aimodel/withapikey/
---
## AiModel.WithApiKey method

Définit une clé API spécifiée pour le modèle.

```csharp
public AiModel WithApiKey(string apiKey)
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

* class [AiModel](../)
* espace de noms [Aspose.Words.AI](../../../aspose.words.ai/)
* Assemblée [Aspose.Words](../../../)
