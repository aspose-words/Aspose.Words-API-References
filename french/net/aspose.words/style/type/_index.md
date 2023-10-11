---
title: Style.Type
second_title: Référence de l'API Aspose.Words pour .NET
description: Style propriété. Obtient le type de style paragraphe ou caractère.
type: docs
weight: 180
url: /fr/net/aspose.words/style/type/
---
## Style.Type property

Obtient le type de style (paragraphe ou caractère).

```csharp
public StyleType Type { get; }
```

### Exemples

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

* enum [StyleType](../../styletype/)
* class [Style](../)
* espace de noms [Aspose.Words](../../style/)
* Assemblée [Aspose.Words](../../../)


