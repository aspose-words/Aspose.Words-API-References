---
title: AiModelType Enum
linktitle: AiModelType
articleTitle: AiModelType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.AI.AiModelType pour une intégration transparente des modèles d'IA dans le traitement des documents, améliorant ainsi l'efficacité et la productivité.
type: docs
weight: 30
url: /fr/net/aspose.words.ai/aimodeltype/
---
## AiModelType enumeration

Représente les types de[`AiModel`](../aimodel/) qui peut être intégré dans le flux de travail de traitement des documents.

```csharp
public enum AiModelType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Gpt4O | `0` | Type de modèle génératif GPT-4o. |
| Gpt4OMini | `1` | Type de modèle génératif mini GPT-4o. |
| Gpt4Turbo | `2` | Type de modèle génératif GPT-4 Turbo. |
| Gpt35Turbo | `3` | Type de modèle génératif GPT-3.5 Turbo. |
| Gemini15Flash | `4` | Type de modèle génératif Flash Gemini 1.5. |
| Gemini15Flash8B | `5` | Type de modèle génératif Gemini 1.5 Flash-8B. |
| Gemini15Pro | `6` | Type de modèle génératif Gemini 1.5 Pro. |
| Claude35Sonnet | `7` | Claude 3.5 Type de modèle génératif Sonnet. |
| Claude35Haiku | `8` | Claude 3.5 Type de modèle génératif Haiku. |
| Claude3Opus | `9` | Type de modèle génératif Claude 3 Opus. |
| Claude3Sonnet | `10` | Claude 3 Sonnet type de modèle génératif. |
| Claude3Haiku | `11` | Claude 3 Type de modèle génératif Haiku. |

## Remarques

Cette énumération est utilisée pour définir quel grand modèle de langage (LLM) doit être utilisé pour des tâches telles que le résumé, la traduction et la génération de contenu.

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
