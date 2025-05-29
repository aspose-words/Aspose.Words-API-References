---
title: DocumentPropertyCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words pour .NET
description: Découvrez la propriété DocumentPropertyCollection Count pour récupérer sans effort le nombre d'éléments de votre collection pour une gestion efficace des données.
type: docs
weight: 10
url: /fr/net/aspose.words.properties/documentpropertycollection/count/
---
## DocumentPropertyCollection.Count property

Obtient le nombre d'éléments dans la collection.

```csharp
public int Count { get; }
```

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

* class [DocumentPropertyCollection](../)
* espace de noms [Aspose.Words.Properties](../../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../../)
