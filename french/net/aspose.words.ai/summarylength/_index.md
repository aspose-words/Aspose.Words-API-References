---
title: SummaryLength Enum
linktitle: SummaryLength
articleTitle: SummaryLength
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.AI.SummaryLength, offrant des options de longueur de résumé flexibles pour un résumé amélioré des documents et une clarté du contenu améliorée.
type: docs
weight: 110
url: /fr/net/aspose.words.ai/summarylength/
---
## SummaryLength enumeration

Énumère les longueurs possibles du résumé.

```csharp
public enum SummaryLength
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| VeryShort | `0` | Essayez de générer 1 à 2 phrases. |
| Short | `1` | Essayez de générer 3 à 4 phrases. |
| Medium | `2` | Essayez de générer 5 à 6 phrases. |
| Long | `3` | Essayez de générer 7 à 10 phrases. |
| VeryLong | `4` | Essayez de générer 11 à 20 phrases. |

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
