---
title: Style.Styles
second_title: Référence de l'API Aspose.Words pour .NET
description: Style propriété. Obtient la collection de styles à laquelle ce style appartient.
type: docs
weight: 150
url: /fr/net/aspose.words/style/styles/
---
## Style.Styles property

Obtient la collection de styles à laquelle ce style appartient.

```csharp
public StyleCollection Styles { get; }
```

### Exemples

Montre comment accéder à la collection de styles d'un document.

```csharp
Document doc = new Document();

Assert.AreEqual(4, doc.Styles.Count);

// Énumère et liste tous les styles qu'un document créé avec Aspose.Words contient par défaut.
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
* espace de noms [Aspose.Words](../../style/)
* Assemblée [Aspose.Words](../../../)


