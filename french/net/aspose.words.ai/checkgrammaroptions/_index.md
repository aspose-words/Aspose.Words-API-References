---
title: CheckGrammarOptions Class
linktitle: CheckGrammarOptions
articleTitle: CheckGrammarOptions
second_title: Aspose.Words pour .NET
description: Optimisez vos documents avec Aspose.Words.AI.CheckGrammarOptions. Découvrez des vérifications grammaticales IA personnalisables pour une rédaction impeccable et une clarté accrue.
type: docs
weight: 50
url: /fr/net/aspose.words.ai/checkgrammaroptions/
---
## CheckGrammarOptions class

Permet de spécifier diverses options lors de la vérification de la grammaire d'un document à l'aide de l'IA.

```csharp
public class CheckGrammarOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [CheckGrammarOptions](checkgrammaroptions/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [ImproveStylistics](../../aspose.words.ai/checkgrammaroptions/improvestylistics/) { get; set; } | Permet de spécifier si l'IA essaiera d'améliorer la stylistique du texte en cours de vérification. La valeur par défaut est`FAUX` . |
| [MakeRevisions](../../aspose.words.ai/checkgrammaroptions/makerevisions/) { get; set; } | Permet de spécifier le document final ou révisé à renvoyer avec le texte vérifié. La valeur par défaut est`FAUX` . |
| [PreserveFormatting](../../aspose.words.ai/checkgrammaroptions/preserveformatting/) { get; set; } | Permet de spécifier soit[`CheckGrammar`](../iaimodeltext/checkgrammar/)essaiera de préserver la mise en page et le formatage du document d'origine, ou non. La valeur par défaut est`vrai` . |

## Exemples

Montre comment vérifier la grammaire d'un document.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Utiliser les modèles de langage génératifs OpenAI.
IAiModelText model = (OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey);

CheckGrammarOptions grammarOptions = new CheckGrammarOptions();
grammarOptions.ImproveStylistics = true;

Document proofedDoc = model.CheckGrammar(doc, grammarOptions);
proofedDoc.Save(ArtifactsDir + "AI.AiGrammar.docx");
```

### Voir également

* espace de noms [Aspose.Words.AI](../../aspose.words.ai/)
* Assemblée [Aspose.Words](../../)
