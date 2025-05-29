---
title: AiModel.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words pour .NET
description: Découvrez la méthode AiModel Create pour générer sans effort de nouvelles instances de classe AiModel, améliorant ainsi votre développement d'IA avec une efficacité rationalisée.
type: docs
weight: 10
url: /fr/net/aspose.words.ai/aimodel/create/
---
## AiModel.Create method

Crée une nouvelle instance de[`AiModel`](../) classe.

```csharp
public static AiModel Create(AiModelType modelType)
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

* enum [AiModelType](../../aimodeltype/)
* class [AiModel](../)
* espace de noms [Aspose.Words.AI](../../../aspose.words.ai/)
* Assemblée [Aspose.Words](../../../)
