---
title: AiModel Class
linktitle: AiModel
articleTitle: AiModel
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.AI.AiModel, votre clé pour exploiter les modèles de langage génératif avancés pour une génération de texte et une automatisation améliorées.
type: docs
weight: 20
url: /fr/net/aspose.words.ai/aimodel/
---
## AiModel class

Représente des informations sur un modèle de langage génératif.

```csharp
public abstract class AiModel
```

## Méthodes

| Nom | La description |
| --- | --- |
| static [Create](../../aspose.words.ai/aimodel/create/)(*[AiModelType](../aimodeltype/)*) | Crée une nouvelle instance de`AiModel` classe. |
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

* espace de noms [Aspose.Words.AI](../../aspose.words.ai/)
* Assemblée [Aspose.Words](../../)
