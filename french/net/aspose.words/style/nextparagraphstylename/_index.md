---
title: Style.NextParagraphStyleName
linktitle: NextParagraphStyleName
articleTitle: NextParagraphStyleName
second_title: Aspose.Words pour .NET
description: Découvrez comment utiliser efficacement la propriété NextParagraphStyleName pour automatiser l'application de style pour les nouveaux paragraphes, améliorant ainsi la mise en forme de votre document.
type: docs
weight: 140
url: /fr/net/aspose.words/style/nextparagraphstylename/
---
## Style.NextParagraphStyleName property

Obtient/définit le nom du style à appliquer automatiquement à un nouveau paragraphe inséré après un paragraphe formaté avec le style spécifié.

```csharp
public string NextParagraphStyleName { get; set; }
```

## Remarques

Cette propriété n'est pas utilisée par Aspose.Words. Le style de paragraphe suivant sera appliqué automatiquement uniquement lors de la modification du document dans MS Word.

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
