---
title: DocumentPropertyCollection Class
linktitle: DocumentPropertyCollection
articleTitle: DocumentPropertyCollection
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Properties.DocumentPropertyCollection, votre solution de référence pour gérer efficacement les propriétés de document intégrées et personnalisées.
type: docs
weight: 5210
url: /fr/net/aspose.words.properties/documentpropertycollection/
---
## DocumentPropertyCollection class

Classe de base pour[`BuiltInDocumentProperties`](../builtindocumentproperties/) et[`CustomDocumentProperties`](../customdocumentproperties/) collections.

Pour en savoir plus, visitez le[Travailler avec les propriétés du document](https://docs.aspose.com/words/net/work-with-document-properties/) article de documentation.

```csharp
public abstract class DocumentPropertyCollection : IEnumerable<DocumentProperty>
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
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | Supprime toutes les propriétés de la collection. |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(*string*) | Retours`vrai` si une propriété portant le nom spécifié existe dans la collection. |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | Renvoie un objet énumérateur qui peut être utilisé pour parcourir tous les éléments de la collection. |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(*string*) | Obtient l'index d'une propriété par nom. |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(*string*) | Supprime une propriété portant le nom spécifié de la collection. |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(*int*) | Supprime une propriété à l'index spécifié. |

## Remarques

Les noms des propriétés ne sont pas sensibles à la casse.

Les propriétés de la collection sont triées par ordre alphabétique par nom.

## Exemples

Montre comment travailler avec les propriétés personnalisées d'un document.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Les propriétés de document personnalisées sont des paires clé-valeur que nous pouvons ajouter au document.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// La collection trie les propriétés personnalisées par ordre alphabétique.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Imprimez chaque propriété personnalisée dans le document.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Affichez la valeur d'une propriété personnalisée à l'aide d'un champ DOCPROPERTY.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Nous pouvons trouver ces propriétés personnalisées dans Microsoft Word via "Fichier" -> "Propriétés" -> "Propriétés avancées" -> "Personnalisé".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Vous trouverez ci-dessous trois manières de supprimer les propriétés personnalisées d'un document.
// 1 - Supprimer par index :
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Supprimer par nom :
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Vider toute la collection en une seule fois :
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Voir également

* class [BuiltInDocumentProperties](../builtindocumentproperties/)
* class [CustomDocumentProperties](../customdocumentproperties/)
* class [DocumentProperty](../documentproperty/)
* espace de noms [Aspose.Words.Properties](../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../)
