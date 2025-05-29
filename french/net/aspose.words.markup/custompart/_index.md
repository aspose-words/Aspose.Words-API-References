---
title: CustomPart Class
linktitle: CustomPart
articleTitle: CustomPart
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Markup.CustomPart pour une gestion de contenu flexible. Créez facilement des composants uniques et non standard, au-delà de la norme ISO/IEC 29500 !
type: docs
weight: 4590
url: /fr/net/aspose.words.markup/custompart/
---
## CustomPart class

Représente une partie personnalisée (contenu arbitraire), qui n'est pas définie par la norme ISO/IEC 29500.

Pour en savoir plus, visitez le[Balises de documents structurés ou contrôle de contenu](https://docs.aspose.com/words/net/working-with-content-control-sdt/) article de documentation.

```csharp
public class CustomPart
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [CustomPart](custompart/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [ContentType](../../aspose.words.markup/custompart/contenttype/) { get; set; } | Spécifie le type de contenu de cette partie personnalisée. |
| [Data](../../aspose.words.markup/custompart/data/) { get; set; } | Contient les données de cette pièce personnalisée. |
| [IsExternal](../../aspose.words.markup/custompart/isexternal/) { get; set; } | Faux si cette partie personnalisée est stockée dans le package OOXML. Vrai si cette partie personnalisée est une cible externe. |
| [Name](../../aspose.words.markup/custompart/name/) { get; set; } | Obtient ou définit le nom absolu de cette partie dans le package OOXML ou l'URL cible. |
| [RelationshipType](../../aspose.words.markup/custompart/relationshiptype/) { get; set; } | Obtient ou définit le type de relation de la partie parent à cette partie personnalisée. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Clone](../../aspose.words.markup/custompart/clone/)() | Effectue une copie « suffisamment profonde » de l'objet. Ne duplique pas les octets de l'objet.[`Data`](./data/) valeur. |

## Remarques

Cette classe représente une partie OOXML qui est la cible d'une « relation inconnue ». Toutes les relations non définies dans la norme ISO/IEC 29500 sont considérées comme des « relations inconnues ». Les relations inconnues sont autorisées dans un document Office Open XML à condition qu'elles soient conformes aux directives de balisage des relations.

Microsoft Word conserve les parties personnalisées lors des cycles d'ouverture et d'enregistrement. Vous trouverez des informations complémentaires ici : http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

Aspose.Words effectue également des allers-retours entre les parties personnalisées et permet en outre d'accéder par programmation à ces parties via le`CustomPart` et[`CustomPartCollection`](../custompartcollection/) objets.

Ne confondez pas les composants personnalisés avec les données XML personnalisées.[`CustomXmlPart`](../customxmlpart/) si vous avez besoin de pour accéder aux données XML personnalisées.

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

* espace de noms [Aspose.Words.Markup](../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../)
