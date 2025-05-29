---
title: OpenAiModel Class
linktitle: OpenAiModel
articleTitle: OpenAiModel
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.AI.OpenAiModel, votre passerelle vers une intégration transparente avec les puissants modèles de langage d'OpenAI pour un traitement amélioré des documents.
type: docs
weight: 90
url: /fr/net/aspose.words.ai/openaimodel/
---
## OpenAiModel class

Une classe abstraite représentant l'intégration avec les grands modèles de langage d'OpenAI dans Aspose.Words.

```csharp
public abstract class OpenAiModel : AiModel, IAiModelText
```

## Méthodes

| Nom | La description |
| --- | --- |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | Définit une clé API spécifiée pour le modèle. |
| [WithOrganization](../../aspose.words.ai/openaimodel/withorganization/)(*string*) | Définit une organisation spécifiée sur le modèle. |
| [WithProject](../../aspose.words.ai/openaimodel/withproject/)(*string*) | Définit un projet spécifié sur le modèle. |

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
