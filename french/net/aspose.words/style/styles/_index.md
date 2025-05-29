---
title: Style.Styles
linktitle: Styles
articleTitle: Styles
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Style Styles pour accéder à une collection organisée de styles, améliorant votre conception avec une esthétique unique et cohérente.
type: docs
weight: 190
url: /fr/net/aspose.words/style/styles/
---
## Style.Styles property

Obtient la collection de styles à laquelle appartient ce style.

```csharp
public StyleCollection Styles { get; }
```

## Exemples

Montre comment accéder à la collection de styles d'un document.

```csharp
Document doc = new Document();

Assert.AreEqual(4, doc.Styles.Count);

// Énumérer et lister tous les styles qu'un document créé à l'aide d'Aspose.Words contient par défaut.
using (IEnumerator<Style> stylesEnum = doc.Styles.GetEnumerator())
{
    while (stylesEnum.MoveNext())
    {
        Style curStyle = stylesEnum.Current;
        Console.WriteLine($"Style name:\t\"{curStyle.Name}\", of type \"{curStyle.Type}\"");
        Console.WriteLine($"\tSubsequent style:\t{curStyle.NextParagraphStyleName}");
        Console.WriteLine($"\tIs heading:\t\t\t{curStyle.IsHeading}");
        Console.WriteLine($"\tIs QuickStyle:\t\t{curStyle.IsQuickStyle}");

        Assert.AreEqual(doc, curStyle.Document);
    }
}
```

### Voir également

* class [StyleCollection](../../stylecollection/)
* class [Style](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
