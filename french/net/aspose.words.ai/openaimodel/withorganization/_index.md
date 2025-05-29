---
title: OpenAiModel.WithOrganization
linktitle: WithOrganization
articleTitle: WithOrganization
second_title: Aspose.Words pour .NET
description: Découvrez comment la méthode OpenAiModel WithOrganization améliore votre expérience d'IA en configurant facilement votre organisation pour des performances optimisées.
type: docs
weight: 10
url: /fr/net/aspose.words.ai/openaimodel/withorganization/
---
## OpenAiModel.WithOrganization method

Définit une organisation spécifiée sur le modèle.

```csharp
public OpenAiModel WithOrganization(string organizationId)
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

* class [OpenAiModel](../)
* espace de noms [Aspose.Words.AI](../../../aspose.words.ai/)
* Assemblée [Aspose.Words](../../../)
