---
title: DocumentPropertyCollection.Item
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentPropertyCollection propriété. Renvoie unDocumentProperty objet par le nom de la propriété.
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

### Remarques

Retour`nul` si une propriété portant le nom spécifié n'est pas trouvée.

### Exemples

Montre comment créer une propriété de document personnalisée contenant une date et une heure.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);

Console.WriteLine($"Document authorized on {doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime()}");
```

### Voir également

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* espace de noms [Aspose.Words.Properties](../../documentpropertycollection/)
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

### Exemples

Montre comment utiliser les propriétés de document personnalisées.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Chaque document contient une collection de propriétés personnalisées qui, comme les propriétés intégrées, sont des paires clé-valeur.
 // Le document a une liste fixe de propriétés intégrées. L'utilisateur crée toutes les propriétés personnalisées.
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
* espace de noms [Aspose.Words.Properties](../../documentpropertycollection/)
* Assemblée [Aspose.Words](../../../)


