---
title: DocumentPropertyCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words pour .NET
description: Accédez facilement aux objets DocumentProperty grâce à notre élément DocumentPropertyCollection. Récupérez les propriétés par nom pour une gestion documentaire fluide.
type: docs
weight: 20
url: /fr/net/aspose.words.properties/documentpropertycollection/item/
---
## DocumentPropertyCollection indexer (1 of 2)

Renvoie un[`DocumentProperty`](../../documentproperty/) objet par le nom de la propriété.

```csharp
public virtual DocumentProperty this[string name] { get; }
```

| Paramètre | La description |
| --- | --- |
| name | Le nom insensible à la casse de la propriété à récupérer. |

## Remarques

Retours`nul` si une propriété avec le nom spécifié n'est pas trouvée.

## Exemples

Montre comment créer une propriété de document personnalisée contenant une date et une heure.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);
DateTime authorizationDate = doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime();
Console.WriteLine($"Document authorized on {authorizationDate}");
```

### Voir également

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* espace de noms [Aspose.Words.Properties](../../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../../)

---

## DocumentPropertyCollection indexer (2 of 2)

Renvoie un[`DocumentProperty`](../../documentproperty/) objet par index.

```csharp
public DocumentProperty this[int index] { get; }
```

| Paramètre | La description |
| --- | --- |
| index | Indice de base zéro du[`DocumentProperty`](../../documentproperty/) à récupérer. |

## Exemples

Montre comment travailler avec les propriétés de document personnalisées.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Chaque document contient une collection de propriétés personnalisées qui, comme les propriétés intégrées, sont des paires clé-valeur.
 // Le document possède une liste fixe de propriétés intégrées. L'utilisateur crée toutes les propriétés personnalisées.
Assert.AreEqual("Value of custom document property", doc.CustomDocumentProperties["CustomProperty"].ToString());

doc.CustomDocumentProperties.Add("CustomProperty2", "Value of custom document property #2");

Console.WriteLine("Custom Properties:");
foreach (var customDocumentProperty in doc.CustomDocumentProperties)
{
    Console.WriteLine(customDocumentProperty.Name);
    Console.WriteLine($"\tType:\t{customDocumentProperty.Type}");
    Console.WriteLine($"\tValue:\t\"{customDocumentProperty.Value}\"");
}
```

### Voir également

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* espace de noms [Aspose.Words.Properties](../../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../../)
