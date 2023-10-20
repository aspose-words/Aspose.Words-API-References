---
title: Document.SpellingChecked
linktitle: SpellingChecked
articleTitle: SpellingChecked
second_title: Aspose.Words pour .NET
description: Document SpellingChecked propriété. Retoursvrai si lorthographe du document a été vérifiée en C#.
type: docs
weight: 410
url: /fr/net/aspose.words/document/spellingchecked/
---
## Document.SpellingChecked property

Retours`vrai` si l'orthographe du document a été vérifiée.

```csharp
public bool SpellingChecked { get; set; }
```

## Remarques

Pour revérifier l'orthographe dans le document, définissez cette propriété sur`FAUX` .

## Exemples

Montre comment définir la vérification orthographique ou grammaticale.

```csharp
Document doc = new Document();

// La chaîne avec les fautes d'orthographe.
doc.FirstSection.Body.FirstParagraph.Runs.Add(new Run(doc, "The speeling in this documentz is all broked."));

 // La vérification orthographique/grammaire démarre si nous définissons les propriétés sur false.
// Nous pouvons voir toutes les erreurs dans Microsoft Word via Review -> Orthographe et amp; Grammaire.
// Notez que Microsoft Word ne démarre pas automatiquement la vérification grammaticale/orthographe pour les formats de document DOC et RTF.
doc.SpellingChecked = checkSpellingGrammar;
doc.GrammarChecked = checkSpellingGrammar;

doc.Save(ArtifactsDir + "Document.SpellingOrGrammar.docx");
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
