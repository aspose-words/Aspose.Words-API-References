---
title: Clear
second_title: Référence de l'API Aspose.Words pour .NET
description: Supprime tous les éléments de la collection.
type: docs
weight: 50
url: /fr/net/aspose.words.markup/custompartcollection/clear/
---
## CustomPartCollection.Clear method

Supprime tous les éléments de la collection.

```csharp
public void Clear()
```

### Exemples

Montre comment accéder à la collection de parties personnalisées arbitraires d'un document.

```csharp
Document doc = new Document(MyDir + "Custom parts OOXML package.docx");

Assert.AreEqual(2, doc.PackageCustomParts.Count);

// Clone la deuxième partie, puis ajoute le clone à la collection.
CustomPart clonedPart = doc.PackageCustomParts[1].Clone();
doc.PackageCustomParts.Add(clonedPart);
Assert.AreEqual(3, doc.PackageCustomParts.Count);

// Énumère la collection et imprime chaque partie.
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

* class [CustomPartCollection](../../custompartcollection)
* espace de noms [Aspose.Words.Markup](../../custompartcollection)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
