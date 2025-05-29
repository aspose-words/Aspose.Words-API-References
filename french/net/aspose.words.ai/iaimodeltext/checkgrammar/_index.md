---
title: IAiModelText.CheckGrammar
linktitle: CheckGrammar
articleTitle: CheckGrammar
second_title: Aspose.Words pour .NET
description: Améliorez votre rédaction grâce à la méthode CheckGrammar d'IAiModelText. Améliorez facilement la précision de vos documents grâce à la vérification grammaticale avancée de l'IA.
type: docs
weight: 10
url: /fr/net/aspose.words.ai/iaimodeltext/checkgrammar/
---
## IAiModelText.CheckGrammar method

Vérifie la grammaire du document fourni. Cette opération exploite le modèle d'IA connecté pour vérifier la grammaire du document.

```csharp
public Document CheckGrammar(Document sourceDocument, CheckGrammarOptions options = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| sourceDocument | Document | Le document est en cours de vérification grammaticale. |
| options | CheckGrammarOptions | Paramètres facultatifs pour contrôler la manière dont la grammaire sera vérifiée. |

### Return_Value

Un nouveau[`Document`](../../../aspose.words/document/) avec une grammaire vérifiée.

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

* class [Document](../../../aspose.words/document/)
* class [CheckGrammarOptions](../../checkgrammaroptions/)
* interface [IAiModelText](../)
* espace de noms [Aspose.Words.AI](../../../aspose.words.ai/)
* Assemblée [Aspose.Words](../../../)
