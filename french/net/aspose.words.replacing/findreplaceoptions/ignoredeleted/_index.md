---
title: FindReplaceOptions.IgnoreDeleted
linktitle: IgnoreDeleted
articleTitle: IgnoreDeleted
second_title: Aspose.Words pour .NET
description: Découvrez la propriété IgnoreDeleted de FindReplaceOptions et contrôlez la visibilité du texte dans les révisions supprimées grâce à une simple option booléenne. Améliorez votre expérience d'édition !
type: docs
weight: 60
url: /fr/net/aspose.words.replacing/findreplaceoptions/ignoredeleted/
---
## FindReplaceOptions.IgnoreDeleted property

Obtient ou définit une valeur booléenne indiquant d'ignorer le texte à l'intérieur des révisions de suppression. La valeur par défaut est`FAUX` .

```csharp
public bool IgnoreDeleted { get; set; }
```

## Exemples

Montre comment inclure ou ignorer du texte dans les révisions de suppression lors d'une opération de recherche et de remplacement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Commencez à suivre les révisions et supprimez le deuxième paragraphe, ce qui créera une révision de suppression.
// Ce paragraphe persistera dans le document jusqu'à ce que nous acceptions la révision de suppression.
doc.StartTrackRevisions("John Doe", DateTime.Now);
doc.FirstSection.Body.Paragraphs[1].Remove();
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsDeleteRevision);

// Nous pouvons utiliser un objet « FindReplaceOptions » pour modifier le processus de recherche et de remplacement.
FindReplaceOptions options = new FindReplaceOptions();

// Définissez l'indicateur « IgnoreDeleted » sur « true » pour obtenir la fonction de recherche et de remplacement
// opération pour ignorer les paragraphes qui sont des révisions de suppression.
// Définissez l'indicateur « IgnoreDeleted » sur « false » pour obtenir la fonction de recherche et de remplacement
// opération permettant également de rechercher du texte à l'intérieur des révisions de suppression.
options.IgnoreDeleted = ignoreTextInsideDeleteRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideDeleteRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### Voir également

* class [FindReplaceOptions](../)
* espace de noms [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Assemblée [Aspose.Words](../../../)
