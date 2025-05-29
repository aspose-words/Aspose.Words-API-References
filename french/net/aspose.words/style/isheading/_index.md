---
title: Style.IsHeading
linktitle: IsHeading
articleTitle: IsHeading
second_title: Aspose.Words pour .NET
description: Découvrez la propriété IsHeading. Identifiez facilement si un style est un style de titre intégré, améliorant ainsi la structure et la lisibilité de votre document.
type: docs
weight: 70
url: /fr/net/aspose.words/style/isheading/
---
## Style.IsHeading property

Vrai lorsque le style est l'un des styles de titre intégrés.

```csharp
public bool IsHeading { get; }
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

* class [Style](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
