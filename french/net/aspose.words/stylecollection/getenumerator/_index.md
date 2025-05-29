---
title: StyleCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words pour .NET
description: Découvrez la méthode GetEnumerator de StyleCollection pour répertorier facilement les styles par ordre alphabétique. Améliorez votre efficacité de codage dès aujourd'hui !
type: docs
weight: 90
url: /fr/net/aspose.words/stylecollection/getenumerator/
---
## StyleCollection.GetEnumerator method

Obtient un objet énumérateur qui énumérera les styles dans l'ordre alphabétique de leurs noms.

```csharp
public IEnumerator<Style> GetEnumerator()
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

* class [Style](../../style/)
* class [StyleCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
