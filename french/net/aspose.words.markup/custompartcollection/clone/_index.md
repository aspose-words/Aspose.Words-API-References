---
title: CustomPartCollection.Clone
second_title: Référence de l'API Aspose.Words pour .NET
description: CustomPartCollection méthode. Crée une copie complète de cette collection et de ses éléments.
type: docs
weight: 60
url: /fr/net/aspose.words.markup/custompartcollection/clone/
---
## CustomPartCollection.Clone method

Crée une copie complète de cette collection et de ses éléments.

```csharp
public CustomPartCollection Clone()
```

### Exemples

Montre comment accéder à la collection de pièces personnalisées arbitraires d’un document.

```csharp
Document doc = new Document(MyDir + "Custom parts OOXML package.docx");

Assert.AreEqual(2, doc.PackageCustomParts.Count);

// Clonez la deuxième partie, puis ajoutez le clone à la collection.
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

// Nous pouvons supprimer des éléments de cette collection individuellement ou tous en même temps.
doc.PackageCustomParts.RemoveAt(2);

Assert.AreEqual(2, doc.PackageCustomParts.Count);

doc.PackageCustomParts.Clear();

Assert.AreEqual(0, doc.PackageCustomParts.Count);
```

### Voir également

* class [CustomPartCollection](../)
* espace de noms [Aspose.Words.Markup](../../custompartcollection/)
* Assemblée [Aspose.Words](../../../)


