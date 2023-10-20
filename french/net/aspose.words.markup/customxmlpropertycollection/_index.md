---
title: CustomXmlPropertyCollection Class
linktitle: CustomXmlPropertyCollection
articleTitle: CustomXmlPropertyCollection
second_title: Aspose.Words pour .NET
description: Aspose.Words.Markup.CustomXmlPropertyCollection classe. Représente une collection dattributs XML personnalisés ou de propriétés de balises intelligentes en C#.
type: docs
weight: 3950
url: /fr/net/aspose.words.markup/customxmlpropertycollection/
---
## CustomXmlPropertyCollection class

Représente une collection d'attributs XML personnalisés ou de propriétés de balises intelligentes.

Pour en savoir plus, visitez le[Balises de documents structurés ou contrôle de contenu](https://docs.aspose.com/words/net/working-with-content-control-sdt/) article documentaire.

```csharp
public class CustomXmlPropertyCollection : IEnumerable<CustomXmlProperty>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlpropertycollection/count/) { get; } | Obtient le nombre d'éléments contenus dans la collection. |
| [Item](../../aspose.words.markup/customxmlpropertycollection/item/) { get; } | Obtient une propriété avec le nom spécifié. (2 indexers) |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlpropertycollection/add/)(*[CustomXmlProperty](../customxmlproperty/)*) | Ajoute une propriété à la collection. |
| [Clear](../../aspose.words.markup/customxmlpropertycollection/clear/)() | Supprime tous les éléments de la collection. |
| [Contains](../../aspose.words.markup/customxmlpropertycollection/contains/)(*string*) | Détermine si la collection contient une propriété portant le nom donné. |
| [GetEnumerator](../../aspose.words.markup/customxmlpropertycollection/getenumerator/)() | Renvoie un objet énumérateur qui peut être utilisé pour parcourir tous les éléments de la collection. |
| [IndexOfKey](../../aspose.words.markup/customxmlpropertycollection/indexofkey/)(*string*) | Renvoie l'index de base zéro de la propriété spécifiée dans la collection. |
| [Remove](../../aspose.words.markup/customxmlpropertycollection/remove/)(*string*) | Supprime une propriété portant le nom spécifié de la collection. |
| [RemoveAt](../../aspose.words.markup/customxmlpropertycollection/removeat/)(*int*) | Supprime une propriété à l'index spécifié. |

## Remarques

Les articles sont[`CustomXmlProperty`](../customxmlproperty/) objets.

## Exemples

Montre comment utiliser les propriétés des balises actives pour obtenir des informations détaillées sur les balises actives.

```csharp
Document doc = new Document(MyDir + "Smart tags.doc");

// Une balise active apparaît dans un document avec Microsoft Word qui reconnaît une partie de son texte comme une forme de données,
// tel qu'un nom, une date ou une adresse, et le convertit en un lien hypertexte affichant un soulignement en pointillés violets.
// Dans Word 2003, nous pouvons activer les balises intelligentes via "Outils" -> "Options de correction automatique..." -> "Étiquettes intelligentes".
// Dans notre document d'entrée, il y a trois objets que Microsoft Word a enregistrés en tant que balises actives.
// Les balises intelligentes peuvent être imbriquées, cette collection en contient donc davantage.
SmartTag[] smartTags = doc.GetChildNodes(NodeType.SmartTag, true).OfType<SmartTag>().ToArray();

Assert.AreEqual(8, smartTags.Length);

// Le membre "Propriétés" d'une balise active contient ses métadonnées, qui seront différentes pour chaque type de balise active.
// Les propriétés d'une balise active de type "date" contiennent son année, son mois et son jour.
CustomXmlPropertyCollection properties = smartTags[7].Properties;

Assert.AreEqual(4, properties.Count);

using (IEnumerator<CustomXmlProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Property name: {enumerator.Current.Name}, value: {enumerator.Current.Value}");
        Assert.AreEqual("", enumerator.Current.Uri);
    }
}

// Nous pouvons également accéder aux propriétés de différentes manières, comme par exemple une paire clé-valeur.
Assert.True(properties.Contains("Day"));
Assert.AreEqual("22", properties["Day"].Value);
Assert.AreEqual("2003", properties[2].Value);
Assert.AreEqual(1, properties.IndexOfKey("Month"));

// Vous trouverez ci-dessous trois façons de supprimer des éléments de la collection de propriétés.
// 1 - Supprimer par index :
properties.RemoveAt(3);

Assert.AreEqual(3, properties.Count);

// 2 - Supprimer par nom :
properties.Remove("Year");

Assert.AreEqual(2, properties.Count);

// 3 - Effacer toute la collection en même temps :
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Voir également

* class [CustomXmlProperty](../customxmlproperty/)
* espace de noms [Aspose.Words.Markup](../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../)
