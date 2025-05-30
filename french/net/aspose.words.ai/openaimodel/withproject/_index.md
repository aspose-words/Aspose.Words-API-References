---
title: OpenAiModel.WithProject
linktitle: WithProject
articleTitle: WithProject
second_title: Aspose.Words pour .NET
description: Améliorez vos capacités d'IA avec la méthode WithProject d'OpenAiModel  attribuez facilement des projets pour optimiser les performances et rationaliser votre flux de travail.
type: docs
weight: 20
url: /fr/net/aspose.words.ai/openaimodel/withproject/
---
## OpenAiModel.WithProject method

Définit un projet spécifié sur le modèle.

```csharp
public OpenAiModel WithProject(string projectId)
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
