---
title: DocumentPropertyCollection.Count
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentPropertyCollection propriété. Obtient le nombre déléments dans la collection.
type: docs
weight: 10
url: /fr/net/aspose.words.properties/documentpropertycollection/count/
---
## DocumentPropertyCollection.Count property

Obtient le nombre d'éléments dans la collection.

```csharp
public int Count { get; }
```

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

* class [DocumentPropertyCollection](../)
* espace de noms [Aspose.Words.Properties](../../documentpropertycollection/)
* Assemblée [Aspose.Words](../../../)


