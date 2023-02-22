---
title: Class CustomDocumentProperties
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Properties.CustomDocumentProperties classe. Une collection de propriétés de document personnalisées.
type: docs
weight: 4210
url: /fr/net/aspose.words.properties/customdocumentproperties/
---
## CustomDocumentProperties class

Une collection de propriétés de document personnalisées.

```csharp
public class CustomDocumentProperties : DocumentPropertyCollection
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.properties/documentpropertycollection/count/) { get; } | Obtient le nombre d'éléments dans la collection. |
| [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Renvoie un[`DocumentProperty`](../documentproperty/) objet par index. |
| virtual [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Renvoie un[`DocumentProperty`](../documentproperty/) objet par le nom de la propriété. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add)(string, bool) | Crée une nouvelle propriété de document personnalisée du **PropertyType.Boolean** type de données. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_3)(string, DateTime) | Crée une nouvelle propriété de document personnalisée du **PropertyType.DateTime** type de données. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_1)(string, double) | Crée une nouvelle propriété de document personnalisée du **PropertyType.Float** type de données. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_2)(string, int) | Crée une nouvelle propriété de document personnalisée du **PropertyType.Number** type de données. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_4)(string, string) | Crée une nouvelle propriété de document personnalisée du **PropertyType.String** type de données. |
| [AddLinkToContent](../../aspose.words.properties/customdocumentproperties/addlinktocontent/)(string, string) | Crée une nouvelle propriété de document personnalisée liée au contenu. |
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | Supprime toutes les propriétés de la collection. |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(string) | Renvoie vrai si une propriété avec le nom spécifié existe dans la collection. |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | Renvoie un objet énumérateur qui peut être utilisé pour itérer sur tous les éléments de la collection. |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(string) | Obtient l'index d'une propriété par nom. |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(string) | Supprime une propriété portant le nom spécifié de la collection. |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(int) | Supprime une propriété à l'index spécifié. |

### Remarques

Chaque[`DocumentProperty`](../documentproperty/) L'objet représente une propriété personnalisée d'un document conteneur.

Les noms des propriétés ne sont pas sensibles à la casse.

Les propriétés de la collection sont triées par ordre alphabétique de nom.

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

* class [Document](../../aspose.words/document/)
* property [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/)
* property [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/)
* class [DocumentPropertyCollection](../documentpropertycollection/)
* espace de noms [Aspose.Words.Properties](../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../)


