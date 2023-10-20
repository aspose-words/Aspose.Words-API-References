---
title: CustomXmlSchemaCollection Class
linktitle: CustomXmlSchemaCollection
articleTitle: CustomXmlSchemaCollection
second_title: Aspose.Words pour .NET
description: Aspose.Words.Markup.CustomXmlSchemaCollection classe. Une collection de chaînes qui représentent les schémas XML associés à une partie XML personnalisée en C#.
type: docs
weight: 3960
url: /fr/net/aspose.words.markup/customxmlschemacollection/
---
## CustomXmlSchemaCollection class

Une collection de chaînes qui représentent les schémas XML associés à une partie XML personnalisée.

Pour en savoir plus, visitez le[Balises de documents structurés ou contrôle de contenu](https://docs.aspose.com/words/net/working-with-content-control-sdt/) article documentaire.

```csharp
public class CustomXmlSchemaCollection : IEnumerable<string>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlschemacollection/count/) { get; } | Obtient le nombre d'éléments contenus dans la collection. |
| [Item](../../aspose.words.markup/customxmlschemacollection/item/) { get; set; } | Obtient ou définit l'élément à l'index spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlschemacollection/add/)(*string*) | Ajoute un élément à la collection. |
| [Clear](../../aspose.words.markup/customxmlschemacollection/clear/)() | Supprime tous les éléments de la collection. |
| [Clone](../../aspose.words.markup/customxmlschemacollection/clone/)() | Crée un clone profond de cet objet. |
| [GetEnumerator](../../aspose.words.markup/customxmlschemacollection/getenumerator/)() | Renvoie un objet énumérateur qui peut être utilisé pour parcourir tous les éléments de la collection. |
| [IndexOf](../../aspose.words.markup/customxmlschemacollection/indexof/)(*string*) | Renvoie l'index de base zéro de la valeur spécifiée dans la collection. |
| [Remove](../../aspose.words.markup/customxmlschemacollection/remove/)(*string*) | Supprime la valeur spécifiée de la collection. |
| [RemoveAt](../../aspose.words.markup/customxmlschemacollection/removeat/)(*int*) | Supprime une valeur à l'index spécifié. |

## Remarques

Vous ne créez pas d'instances de cette classe. Vous accédez à la collection de schémas XML d'un part XML personnalisé via le[`Schemas`](../customxmlpart/schemas/) propriété.

## Exemples

Montre comment utiliser une collection de schémas XML.

```csharp
Document doc = new Document();

string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello, World!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

// Ajout d'une association de schéma XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Cloner la collection d'associations de schéma XML de la partie XML personnalisée,
// puis ajoutez quelques nouveaux schémas au clone.
CustomXmlSchemaCollection schemas = xmlPart.Schemas.Clone();
schemas.Add("http://www.w3.org/2001/XMLSchema-instance");
schemas.Add("http://schemas.microsoft.com/office/2006/metadata/contentType");

Assert.AreEqual(3, schemas.Count);
Assert.AreEqual(2, schemas.IndexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Énumère les schémas et imprime chaque élément.
using (IEnumerator<string> enumerator = schemas.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine(enumerator.Current);
}

// Vous trouverez ci-dessous trois façons de supprimer des schémas de la collection.
// 1 - Supprimer un schéma par index :
schemas.RemoveAt(2);

// 2 - Supprimer un schéma par valeur :
schemas.Remove("http://www.w3.org/2001/XMLSchema");

// 3 - Utilisez la méthode "Clear" pour vider la collection d'un coup.
schemas.Clear();

Assert.AreEqual(0, schemas.Count);
```

### Voir également

* espace de noms [Aspose.Words.Markup](../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../)
