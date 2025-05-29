---
title: CustomXmlProperty.Uri
linktitle: Uri
articleTitle: Uri
second_title: Aspose.Words pour .NET
description: Gérez facilement vos attributs XML personnalisés grâce à l'URI CustomXmlProperty. Définissez ou récupérez facilement l'URI de l'espace de noms pour des fonctionnalités améliorées.
type: docs
weight: 30
url: /fr/net/aspose.words.markup/customxmlproperty/uri/
---
## CustomXmlProperty.Uri property

Obtient ou définit l'URI de l'espace de noms de l'attribut XML personnalisé ou de la propriété de balise active.

```csharp
public string Uri { get; set; }
```

## Remarques

Ne peut pas être`nul`.

La valeur par défaut est une chaîne vide.

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

* class [CustomXmlProperty](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
