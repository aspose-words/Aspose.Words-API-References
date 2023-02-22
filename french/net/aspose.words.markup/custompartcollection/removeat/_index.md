---
title: CustomPartCollection.RemoveAt
second_title: Référence de l'API Aspose.Words pour .NET
description: CustomPartCollection méthode. Supprime un élément à lindex spécifié.
type: docs
weight: 80
url: /fr/net/aspose.words.markup/custompartcollection/removeat/
---
## CustomPartCollection.RemoveAt method

Supprime un élément à l'index spécifié.

```csharp
public void RemoveAt(int index)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| index | Int32 | L'indice de base zéro. |

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

* class [CustomPartCollection](../)
* espace de noms [Aspose.Words.Markup](../../custompartcollection/)
* Assemblée [Aspose.Words](../../../)


