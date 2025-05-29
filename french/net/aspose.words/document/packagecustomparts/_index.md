---
title: Document.PackageCustomParts
linktitle: PackageCustomParts
articleTitle: PackageCustomParts
second_title: Aspose.Words pour .NET
description: Gérez facilement les parties personnalisées de votre package OOXML. Accédez et modifiez facilement le contenu lié pour une flexibilité et des fonctionnalités accrues de vos documents.
type: docs
weight: 320
url: /fr/net/aspose.words/document/packagecustomparts/
---
## Document.PackageCustomParts property

Obtient ou définit la collection de parties personnalisées (contenu arbitraire) qui sont liées au package OOXML à l'aide de « relations inconnues ».

```csharp
public CustomPartCollection PackageCustomParts { get; set; }
```

## Remarques

Ne confondez pas ces parties personnalisées avec les données XML personnalisées. Pour accéder à ces parties, utilisez le[`CustomXmlParts`](../customxmlparts/) propriété.

Cette collection contient des parties OOXML dont le parent est le package OOXML et dont les cibles sont d'une « relation inconnue ». Pour plus d'informations, voir[`CustomPart`](../../../aspose.words.markup/custompart/).

Aspose.Words charge et enregistre les parties personnalisées uniquement dans les documents OOXML.

Cette propriété ne peut pas être`nul`.

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

* class [CustomPartCollection](../../../aspose.words.markup/custompartcollection/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
