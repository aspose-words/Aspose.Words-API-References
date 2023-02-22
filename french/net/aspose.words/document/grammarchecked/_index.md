---
title: Document.GrammarChecked
second_title: Référence de l'API Aspose.Words pour .NET
description: Document propriété. Retours vrai si le document a été vérifié pour la grammaire.
type: docs
weight: 180
url: /fr/net/aspose.words/document/grammarchecked/
---
## Document.GrammarChecked property

Retours **vrai** si le document a été vérifié pour la grammaire.

```csharp
public bool GrammarChecked { get; set; }
```

### Remarques

Pour revérifier la grammaire du document, définissez cette propriété sur **faux** .

### Exemples

Montre comment définir la vérification orthographique ou grammaticale.

```csharp
Document doc = new Document();

// La chaîne avec des fautes d'orthographe.
doc.FirstSection.Body.FirstParagraph.Runs.Add(new Run(doc, "The speeling in this documentz is all broked."));

 // La vérification orthographique/grammaticale commence si nous définissons les propriétés sur false.
// Nous pouvons voir toutes les erreurs dans Microsoft Word via Review -> Orthographe & Grammaire.
// Notez que Microsoft Word ne démarre pas automatiquement la vérification de la grammaire/orthographe pour les formats de document DOC et RTF.
doc.SpellingChecked = checkSpellingGrammar;
doc.GrammarChecked = checkSpellingGrammar;

doc.Save(ArtifactsDir + "Document.SpellingOrGrammar.docx");
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)


