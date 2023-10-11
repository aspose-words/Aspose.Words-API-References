---
title: CustomXmlPropertyCollection.Contains
second_title: Référence de l'API Aspose.Words pour .NET
description: CustomXmlPropertyCollection méthode. Détermine si la collection contient une propriété portant le nom donné.
type: docs
weight: 50
url: /fr/net/aspose.words.markup/customxmlpropertycollection/contains/
---
## CustomXmlPropertyCollection.Contains method

Détermine si la collection contient une propriété portant le nom donné.

```csharp
public bool Contains(string name)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| name | String | Nom sensible à la casse de la propriété à localiser. |

### Return_Value

`vrai` si l'objet est trouvé dans la collection ; sinon,`FAUX`.

### Exemples

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

* class [CustomXmlPropertyCollection](../)
* espace de noms [Aspose.Words.Markup](../../customxmlpropertycollection/)
* Assemblée [Aspose.Words](../../../)


