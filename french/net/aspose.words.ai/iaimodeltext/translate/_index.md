---
title: IAiModelText.Translate
linktitle: Translate
articleTitle: Translate
second_title: Aspose.Words pour .NET
description: Traduisez facilement vos documents grâce à notre méthode IAiModelText Translate. Exploitez l'IA pour des traductions précises et rapides dans la langue souhaitée.
type: docs
weight: 30
url: /fr/net/aspose.words.ai/iaimodeltext/translate/
---
## IAiModelText.Translate method

Traduit le document fourni dans la langue cible spécifiée. Cette opération exploite le modèle d'IA connecté pour la traduction du contenu.

```csharp
public Document Translate(Document sourceDocument, Language targetLanguage)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| sourceDocument | Document | Le document à traduire. |
| targetLanguage | Language | La langue dans laquelle le document sera traduit. |

### Return_Value

Un nouveau[`Document`](../../../aspose.words/document/)objet contenant le document traduit.

## Exemples

Montre comment traduire du texte à l'aide des modèles Google.

```csharp
Document doc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Utilisez les modèles de langage génératifs de Google.
IAiModelText model = (GoogleAiModel)AiModel.Create(AiModelType.Gemini15Flash).WithApiKey(apiKey);

Document translatedDoc = model.Translate(doc, Language.Arabic);
translatedDoc.Save(ArtifactsDir + "AI.AiTranslate.docx");
```

### Voir également

* class [Document](../../../aspose.words/document/)
* enum [Language](../../language/)
* interface [IAiModelText](../)
* espace de noms [Aspose.Words.AI](../../../aspose.words.ai/)
* Assemblée [Aspose.Words](../../../)
