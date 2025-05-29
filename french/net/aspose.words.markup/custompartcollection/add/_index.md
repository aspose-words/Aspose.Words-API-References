---
title: CustomPartCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words pour .NET
description: Améliorez sans effort votre projet avec la méthode CustomPartCollection Add : ajoutez rapidement des éléments à votre collection pour une intégration et une efficacité transparentes.
type: docs
weight: 40
url: /fr/net/aspose.words.markup/custompartcollection/add/
---
## CustomPartCollection.Add method

Ajoute un élément à la collection.

```csharp
public void Add(CustomPart part)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| part | CustomPart | L'élément à ajouter. |

## Exemples

Montre comment accéder à la collection de parties personnalisées arbitraires d'un document.

```csharp
Document doc = new Document(MyDir + "Custom parts OOXML package.docx");

Assert.AreEqual(2, doc.PackageCustomParts.Count);

// Clonez la deuxième partie, puis ajoutez le clone à la collection.
CustomPart clonedPart = doc.PackageCustomParts[1].Clone();
doc.PackageCustomParts.Add(clonedPart);
Assert.AreEqual(3, doc.PackageCustomParts.Count);

// Énumérer la collection et imprimer chaque partie.
using (IEnumerator<CustomPart> enumerator = doc.PackageCustomParts.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Part index {index}:");
        Console.WriteLine($"\tName:\t\t\t\t{enumerator.Current.Name}");
        Console.WriteLine($"\tContent type:\t\t{enumerator.Current.ContentType}");
        Console.WriteLine($"\tRelationship type:\t{enumerator.Current.RelationshipType}");
        Console.WriteLine(enumerator.Current.IsExternal ?
            "\tSourced from outside the document" :
            $"\tStored within the document, length: {enumerator.Current.Data.Length} bytes");
        index++;
    }
}

// Nous pouvons supprimer des éléments de cette collection individuellement ou tous à la fois.
doc.PackageCustomParts.RemoveAt(2);

Assert.AreEqual(2, doc.PackageCustomParts.Count);

doc.PackageCustomParts.Clear();

Assert.AreEqual(0, doc.PackageCustomParts.Count);
```

### Voir également

* class [CustomPart](../../custompart/)
* class [CustomPartCollection](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
