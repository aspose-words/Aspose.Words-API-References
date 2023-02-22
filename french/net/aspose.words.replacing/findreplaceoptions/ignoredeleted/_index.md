---
title: FindReplaceOptions.IgnoreDeleted
second_title: Référence de l'API Aspose.Words pour .NET
description: FindReplaceOptions propriété. Obtient ou définit une valeur booléenne indiquant soit dignorer le texte à lintérieur des révisions de suppression. La valeur par défaut estfaux .
type: docs
weight: 60
url: /fr/net/aspose.words.replacing/findreplaceoptions/ignoredeleted/
---
## FindReplaceOptions.IgnoreDeleted property

Obtient ou définit une valeur booléenne indiquant soit d'ignorer le texte à l'intérieur des révisions de suppression. La valeur par défaut est`faux` .

```csharp
public bool IgnoreDeleted { get; set; }
```

### Exemples

Montre comment inclure ou ignorer du texte dans les révisions de suppression lors d'une opération de recherche et de remplacement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Démarrez le suivi des révisions et supprimez le deuxième paragraphe, ce qui créera une révision de suppression.
// Ce paragraphe persistera dans le document jusqu'à ce que nous acceptions la suppression de la révision.
doc.StartTrackRevisions("John Doe", DateTime.Now);
doc.FirstSection.Body.Paragraphs[1].Remove();
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsDeleteRevision);

// Nous pouvons utiliser un objet "FindReplaceOptions" pour modifier le processus de recherche et de remplacement.
FindReplaceOptions options = new FindReplaceOptions();

// Définissez le drapeau "IgnoreDeleted" sur "true" pour obtenir la recherche et le remplacement
// opération pour ignorer les paragraphes qui sont des révisions de suppression.
// Définissez le drapeau "IgnoreDeleted" sur "false" pour obtenir la recherche et le remplacement
// opération pour rechercher également du texte dans les révisions de suppression.
options.IgnoreDeleted = ignoreTextInsideDeleteRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideDeleteRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### Voir également

* class [FindReplaceOptions](../)
* espace de noms [Aspose.Words.Replacing](../../findreplaceoptions/)
* Assemblée [Aspose.Words](../../../)


