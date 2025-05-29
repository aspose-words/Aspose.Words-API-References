---
title: GoogleAiModel Class
linktitle: GoogleAiModel
articleTitle: GoogleAiModel
second_title: Aspose.Words pour .NET
description: Libérez la puissance de la classe Aspose.Words.AI.GoogleAiModel pour intégrer de manière transparente les modèles Google AI, améliorant ainsi vos capacités de traitement de documents sans effort.
type: docs
weight: 60
url: /fr/net/aspose.words.ai/googleaimodel/
---
## GoogleAiModel class

Une classe abstraite représentant l'intégration avec les modèles d'IA de Google dans Aspose.Words.

```csharp
public abstract class GoogleAiModel : AiModel, IAiModelText
```

## Méthodes

| Nom | La description |
| --- | --- |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | Définit une clé API spécifiée pour le modèle. |

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

* class [AiModel](../aimodel/)
* interface [IAiModelText](../iaimodeltext/)
* espace de noms [Aspose.Words.AI](../../aspose.words.ai/)
* Assemblée [Aspose.Words](../../)
