---
title: FindReplaceOptions.IgnoreInserted
linktitle: IgnoreInserted
articleTitle: IgnoreInserted
second_title: Aspose.Words pour .NET
description: Découvrez la propriété IgnoreInserted de FindReplaceOptions et contrôlez la gestion du texte lors des révisions d'insertion grâce à ce simple paramètre booléen. La valeur par défaut est « false ».
type: docs
weight: 100
url: /fr/net/aspose.words.replacing/findreplaceoptions/ignoreinserted/
---
## FindReplaceOptions.IgnoreInserted property

Obtient ou définit une valeur booléenne indiquant d'ignorer le texte à l'intérieur des révisions d'insertion. La valeur par défaut est`FAUX` .

```csharp
public bool IgnoreInserted { get; set; }
```

## Exemples

Montre comment inclure ou ignorer du texte dans les révisions d'insertion lors d'une opération de recherche et de remplacement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Commencez à suivre les révisions et insérez un paragraphe. Ce paragraphe sera une révision d'insertion.
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("Hello again!");
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsInsertRevision);

// Nous pouvons utiliser un objet « FindReplaceOptions » pour modifier le processus de recherche et de remplacement.
FindReplaceOptions options = new FindReplaceOptions();

// Définissez l'indicateur « IgnoreInserted » sur « true » pour obtenir la fonction de recherche et de remplacement
// opération pour ignorer les paragraphes qui sont des révisions d'insertion.
// Définissez l'indicateur « IgnoreInserted » sur « false » pour obtenir la fonction de recherche et de remplacement
// opération permettant également de rechercher du texte à l'intérieur des révisions d'insertion.
options.IgnoreInserted = ignoreTextInsideInsertRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideInsertRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### Voir également

* class [FindReplaceOptions](../)
* espace de noms [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Assemblée [Aspose.Words](../../../)
