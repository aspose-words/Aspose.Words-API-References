---
title: Document.GrammarChecked
linktitle: GrammarChecked
articleTitle: GrammarChecked
second_title: Aspose.Words pour .NET
description: Assurez la qualité de votre document grâce à la fonction GrammarChecked. Vérifiez si la grammaire de votre texte est vérifiée pour un résultat impeccable et professionnel.
type: docs
weight: 190
url: /fr/net/aspose.words/document/grammarchecked/
---
## Document.GrammarChecked property

Retours`vrai` si le document a été vérifié pour la grammaire.

```csharp
public bool GrammarChecked { get; set; }
```

## Remarques

Pour revérifier la grammaire dans le document, définissez cette propriété sur`FAUX` .

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
