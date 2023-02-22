---
title: StyleCollection.GetEnumerator
second_title: Référence de l'API Aspose.Words pour .NET
description: StyleCollection méthode. Obtient un objet énumérateur qui énumérera les styles dans lordre alphabétique de leurs noms.
type: docs
weight: 90
url: /fr/net/aspose.words/stylecollection/getenumerator/
---
## StyleCollection.GetEnumerator method

Obtient un objet énumérateur qui énumérera les styles dans l'ordre alphabétique de leurs noms.

```csharp
public IEnumerator<Style> GetEnumerator()
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

* class [Style](../../style/)
* class [StyleCollection](../)
* espace de noms [Aspose.Words](../../stylecollection/)
* Assemblée [Aspose.Words](../../../)


