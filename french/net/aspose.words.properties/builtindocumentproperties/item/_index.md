---
title: BuiltInDocumentProperties.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words pour .NET
description: Accédez facilement aux objets DocumentProperty grâce à la propriété Item BuiltInDocumentProperties. Simplifiez la gestion de vos documents dès aujourd'hui !
type: docs
weight: 140
url: /fr/net/aspose.words.properties/builtindocumentproperties/item/
---
## BuiltInDocumentProperties indexer

Renvoie un[`DocumentProperty`](../../documentproperty/) objet par le nom de la propriété.

```csharp
public override DocumentProperty this[string name] { get; }
```

| Paramètre | La description |
| --- | --- |
| name | Le nom insensible à la casse de la propriété à récupérer. |

## Remarques

Les noms de chaîne des propriétés correspondent aux noms des propriétés typed disponibles à partir de[`BuiltInDocumentProperties`](../).

Si vous demandez une propriété qui n'est pas présente dans le document, mais que le nom de la propriété est reconnu comme un nom intégré valide, un nouveau[`DocumentProperty`](../../documentproperty/) est créé, ajouté à la collection et renvoyé. Une valeur par défaut (chaîne vide, zéro,) est attribuée à la propriété nouvellement créée.`FAUX` ou DateTime.MinValue selon le type de la propriété intégrée).

Si vous demandez une propriété qui n'est pas présente dans le document et que le nom n'est pas reconnu comme un nom intégré, un`nul` est retourné.

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
* class [BuiltInDocumentProperties](../)
* espace de noms [Aspose.Words.Properties](../../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../../)
