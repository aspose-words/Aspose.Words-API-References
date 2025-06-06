---
title: Style.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Nom du style, gérez et personnalisez facilement vos styles pour une flexibilité de conception et une expérience utilisateur améliorées.
type: docs
weight: 130
url: /fr/net/aspose.words/style/name/
---
## Style.Name property

Obtient ou définit le nom du style.

```csharp
public string Name { get; set; }
```

## Remarques

Ne peut pas être une chaîne vide.

Si un style portant ce nom existe déjà dans la collection, ce style le remplacera. Tous les nœuds concernés référenceront le nouveau style.

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

Montre comment cloner le style d'un document.

```csharp
Document doc = new Document();

// La méthode AddCopy crée une copie du style spécifié et
// génère automatiquement un nouveau nom pour le style, tel que « Titre 1_0 ».
Style newStyle = doc.Styles.AddCopy(doc.Styles["Heading 1"]);

// Utilisez la propriété « Nom » du style pour modifier le nom d'identification du style.
newStyle.Name = "My Heading 1";

// Notre document a maintenant deux styles identiques avec des noms différents.
// La modification des paramètres de l'un des styles n'affecte pas l'autre.
newStyle.Font.Color = Color.Red;

Assert.AreEqual("My Heading 1", newStyle.Name);
Assert.AreEqual("Heading 1", doc.Styles["Heading 1"].Name);

Assert.AreEqual(doc.Styles["Heading 1"].Type, newStyle.Type);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Name, newStyle.Font.Name);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Size, newStyle.Font.Size);
Assert.AreNotEqual(doc.Styles["Heading 1"].Font.Color, newStyle.Font.Color);
```

### Voir également

* class [Style](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
