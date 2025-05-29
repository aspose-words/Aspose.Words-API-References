---
title: IAiModelText.Summarize
linktitle: Summarize
articleTitle: Summarize
second_title: Aspose.Words pour .NET
description: Résumez facilement vos documents avec IAiModelText. Personnalisez la longueur de vos résumés grâce à une IA avancée pour une extraction précise du contenu et une meilleure lisibilité.
type: docs
weight: 20
url: /fr/net/aspose.words.ai/iaimodeltext/summarize/
---
## Summarize(*[Document](../../../aspose.words/document/), [SummarizeOptions](../../summarizeoptions/)*) {#summarize}

Génère un résumé du document spécifié, avec des options pour ajuster la longueur du résumé. Cette opération exploite le modèle d'IA connecté pour le traitement du contenu.

```csharp
public Document Summarize(Document sourceDocument, SummarizeOptions options = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| sourceDocument | Document | Le document à résumer. |
| options | SummarizeOptions | Paramètres facultatifs pour contrôler la longueur du résumé et d'autres paramètres. |

### Return_Value

Une version résumée du contenu du document.

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

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* interface [IAiModelText](../)
* espace de noms [Aspose.Words.AI](../../../aspose.words.ai/)
* Assemblée [Aspose.Words](../../../)

---

## Summarize(*Document[], [SummarizeOptions](../../summarizeoptions/)*) {#summarize_1}

Génère des résumés pour un tableau de documents, avec des options pour contrôler la longueur du résumé et d'autres paramètres. Cette méthode utilise le modèle d'IA connecté pour traiter chaque document du tableau.

```csharp
public Document Summarize(Document[] sourceDocuments, SummarizeOptions options = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| sourceDocuments | Document[] | Un ensemble de documents à résumer. |
| options | SummarizeOptions | Paramètres facultatifs pour contrôler la longueur du résumé et d'autres paramètres |

### Return_Value

Une version résumée du contenu du document.

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

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* interface [IAiModelText](../)
* espace de noms [Aspose.Words.AI](../../../aspose.words.ai/)
* Assemblée [Aspose.Words](../../../)
