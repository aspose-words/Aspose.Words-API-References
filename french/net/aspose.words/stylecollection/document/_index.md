---
title: StyleCollection.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words pour .NET
description: StyleCollection Document propriété. Obtient le document propriétaire en C#.
type: docs
weight: 40
url: /fr/net/aspose.words/stylecollection/document/
---
## StyleCollection.Document property

Obtient le document propriétaire.

```csharp
public DocumentBase Document { get; }
```

## Exemples

Montre comment accéder à la collection de styles d’un document.

```csharp
Document doc = new Document();

Assert.AreEqual(4, doc.Styles.Count);

// Énumère et répertorie tous les styles qu'un document créé à l'aide d'Aspose.Words contient par défaut.
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

* class [DocumentBase](../../documentbase/)
* class [StyleCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
