---
title: Document.SpellingChecked
linktitle: SpellingChecked
articleTitle: SpellingChecked
second_title: Aspose.Words pour .NET
description: Assurez-vous que votre document est exempt d'erreurs grâce à la fonctionnalité SpellingChecked. Vérifiez si votre contenu a été soigneusement vérifié pour garantir son professionnalisme.
type: docs
weight: 430
url: /fr/net/aspose.words/document/spellingchecked/
---
## Document.SpellingChecked property

Retours`vrai` si l'orthographe du document a été vérifiée.

```csharp
public bool SpellingChecked { get; set; }
```

## Remarques

Pour revérifier l'orthographe du document, définissez cette propriété sur`FAUX` .

## Exemples

Montre comment définir la vérification de l'orthographe ou de la grammaire.

```csharp
Document doc = new Document();

// La chaîne contenant des fautes d'orthographe.
doc.FirstSection.Body.FirstParagraph.Runs.Add(new Run(doc, "The speeling in this documentz is all broked."));

// La vérification de l'orthographe/de la grammaire démarre si nous définissons les propriétés sur false.
// Nous pouvons voir toutes les erreurs dans Microsoft Word via Révision -> Orthographe et grammaire.
// Notez que Microsoft Word ne démarre pas automatiquement la vérification grammaticale/orthographe pour les formats de document DOC et RTF.
doc.SpellingChecked = checkSpellingGrammar;
doc.GrammarChecked = checkSpellingGrammar;

doc.Save(ArtifactsDir + "Document.SpellingOrGrammar.docx");
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
