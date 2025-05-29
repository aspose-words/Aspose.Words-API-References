---
title: CustomXmlPropertyCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words pour .NET
description: Supprimez facilement les propriétés de votre CustomXmlPropertyCollection grâce à notre méthode Remove. Simplifiez la gestion de vos données dès aujourd'hui !
type: docs
weight: 80
url: /fr/net/aspose.words.markup/customxmlpropertycollection/remove/
---
## CustomXmlPropertyCollection.Remove method

Supprime une propriété portant le nom spécifié de la collection.

```csharp
public void Remove(string name)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| name | String | Le nom sensible à la casse de la propriété. |

## Exemples

Montre comment travailler avec les propriétés des balises intelligentes pour obtenir des informations détaillées sur les balises intelligentes.

```csharp
Document doc = new Document(MyDir + "Smart tags.doc");

// Une balise active apparaît dans un document avec Microsoft Word qui reconnaît une partie de son texte comme une forme de données,
// comme un nom, une date ou une adresse, et le convertit en un lien hypertexte qui affiche un soulignement en pointillé violet.
// Dans Word 2003, nous pouvons activer les balises actives via « Outils » -> « Options de correction automatique… » -> « Balises actives ».
// Dans notre document d'entrée, il y a trois objets que Microsoft Word a enregistrés comme balises intelligentes.
// Les balises intelligentes peuvent être imbriquées, cette collection en contient donc davantage.
SmartTag[] smartTags = doc.GetChildNodes(NodeType.SmartTag, true).OfType<SmartTag>().ToArray();

Assert.AreEqual(8, smartTags.Length);

// Le membre « Propriétés » d'une balise intelligente contient ses métadonnées, qui seront différentes pour chaque type de balise intelligente.
// Les propriétés d'une balise intelligente de type « date » contiennent son année, son mois et son jour.
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

// Nous pouvons également accéder aux propriétés de différentes manières, par exemple par une paire clé-valeur.
Assert.True(properties.Contains("Day"));
Assert.AreEqual("22", properties["Day"].Value);
Assert.AreEqual("2003", properties[2].Value);
Assert.AreEqual(1, properties.IndexOfKey("Month"));

// Vous trouverez ci-dessous trois manières de supprimer des éléments de la collection de propriétés.
// 1 - Supprimer par index :
properties.RemoveAt(3);

Assert.AreEqual(3, properties.Count);

// 2 - Supprimer par nom :
properties.Remove("Year");

Assert.AreEqual(2, properties.Count);

// 3 - Effacer toute la collection en une seule fois :
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Voir également

* class [CustomXmlPropertyCollection](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
