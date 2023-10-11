---
title: BuiltInDocumentProperties.Item
second_title: Référence de l'API Aspose.Words pour .NET
description: BuiltInDocumentProperties propriété. Renvoie unDocumentProperty objet par le nom de la propriété.
type: docs
weight: 130
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

### Remarques

Les noms de chaîne des propriétés correspondent aux noms des propriétés typed disponibles depuis[`BuiltInDocumentProperties`](../).

Si vous demandez une propriété qui n'est pas présente dans le document, mais que le nom de la propriété est reconnu comme un nom intégré valide, un nouveau[`DocumentProperty`](../../documentproperty/) est créé, ajouté à la collection et renvoyé. La propriété nouvellement créée se voit attribuer une valeur par défaut (chaîne vide, zéro,`FAUX` ou DateTime.MinValue selon le type de la propriété intégrée).

Si vous demandez une propriété qui n'est pas présente dans le document et que le nom n'est pas reconnu comme nom intégré, un`nul` est retourné.

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
* class [BuiltInDocumentProperties](../)
* espace de noms [Aspose.Words.Properties](../../builtindocumentproperties/)
* Assemblée [Aspose.Words](../../../)


