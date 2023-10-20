---
title: CustomPartCollection Class
linktitle: CustomPartCollection
articleTitle: CustomPartCollection
second_title: Aspose.Words pour .NET
description: Aspose.Words.Markup.CustomPartCollection classe. Représente une collection deCustomPart objets en C#.
type: docs
weight: 3910
url: /fr/net/aspose.words.markup/custompartcollection/
---
## CustomPartCollection class

Représente une collection de[`CustomPart`](../custompart/) objets.

Pour en savoir plus, visitez le[Balises de documents structurés ou contrôle de contenu](https://docs.aspose.com/words/net/working-with-content-control-sdt/) article documentaire.

```csharp
public class CustomPartCollection : IEnumerable<CustomPart>
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [CustomPartCollection](custompartcollection/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.markup/custompartcollection/count/) { get; } | Obtient le nombre d'éléments contenus dans la collection. |
| [Item](../../aspose.words.markup/custompartcollection/item/) { get; set; } | Obtient ou définit un élément à l'index spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words.markup/custompartcollection/add/)(*[CustomPart](../custompart/)*) | Ajoute un élément à la collection. |
| [Clear](../../aspose.words.markup/custompartcollection/clear/)() | Supprime tous les éléments de la collection. |
| [Clone](../../aspose.words.markup/custompartcollection/clone/)() | Crée une copie complète de cette collection et de ses éléments. |
| [GetEnumerator](../../aspose.words.markup/custompartcollection/getenumerator/)() | Renvoie un objet énumérateur qui peut être utilisé pour parcourir tous les éléments de la collection. |
| [RemoveAt](../../aspose.words.markup/custompartcollection/removeat/)(*int*) | Supprime un élément à l'index spécifié. |

## Remarques

Vous n'avez normalement pas besoin de créer des instances de cette classe. Vous accédez aux parties personnalisées liées au package OOXML via le[`PackageCustomParts`](../../aspose.words/document/packagecustomparts/) propriété.

## Exemples

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

* class [CustomPart](../custompart/)
* espace de noms [Aspose.Words.Markup](../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../)
