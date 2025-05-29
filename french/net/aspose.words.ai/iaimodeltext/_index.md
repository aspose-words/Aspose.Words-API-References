---
title: IAiModelText Interface
linktitle: IAiModelText
articleTitle: IAiModelText
second_title: Aspose.Words pour .NET
description: Libérez votre potentiel créatif avec Aspose.Words.AI.IAiModelText, l'interface polyvalente pour les modèles d'IA qui génèrent sans effort du contenu textuel diversifié et de haute qualité.
type: docs
weight: 70
url: /fr/net/aspose.words.ai/iaimodeltext/
---
## IAiModelText interface

L'interface commune pour les modèles d'IA conçus pour générer une variété de contenus textuels.

```csharp
public interface IAiModelText
```

## Méthodes

| Nom | La description |
| --- | --- |
| [CheckGrammar](../../aspose.words.ai/iaimodeltext/checkgrammar/)(*[Document](../../aspose.words/document/), [CheckGrammarOptions](../checkgrammaroptions/)*) | Vérifie la grammaire du document fourni. Cette opération exploite le modèle d'IA connecté pour vérifier la grammaire du document. |
| [Summarize](../../aspose.words.ai/iaimodeltext/summarize/#summarize)(*[Document](../../aspose.words/document/), [SummarizeOptions](../summarizeoptions/)*) | Génère un résumé du document spécifié, avec des options pour ajuster la longueur du résumé. Cette opération exploite le modèle d'IA connecté pour le traitement du contenu. |
| [Summarize](../../aspose.words.ai/iaimodeltext/summarize/#summarize_1)(*Document[], [SummarizeOptions](../summarizeoptions/)*) | Génère des résumés pour un tableau de documents, avec des options pour contrôler la longueur du résumé et d'autres paramètres. Cette méthode utilise le modèle d'IA connecté pour traiter chaque document du tableau. |
| [Translate](../../aspose.words.ai/iaimodeltext/translate/)(*[Document](../../aspose.words/document/), [Language](../language/)*) | Traduit le document fourni dans la langue cible spécifiée. Cette opération exploite le modèle d'IA connecté pour la traduction du contenu. |

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
