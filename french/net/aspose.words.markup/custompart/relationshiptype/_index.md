---
title: CustomPart.RelationshipType
linktitle: RelationshipType
articleTitle: RelationshipType
second_title: Aspose.Words pour .NET
description: Découvrez la propriété CustomPart RelationshipType pour gérer et définir facilement les relations entre les pièces parentes et personnalisées pour des fonctionnalités améliorées.
type: docs
weight: 60
url: /fr/net/aspose.words.markup/custompart/relationshiptype/
---
## CustomPart.RelationshipType property

Obtient ou définit le type de relation de la partie parent à cette partie personnalisée.

```csharp
public string RelationshipType { get; set; }
```

## Remarques

Le type de relation pour une pièce personnalisée doit être « inconnu », par exemple un type de relation personnalisé, , et non l'un des types de relation définis dans la norme ISO/IEC 29500.

La valeur par défaut est une chaîne vide. Une valeur valide doit être une chaîne non vide.

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

* class [CustomPart](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
