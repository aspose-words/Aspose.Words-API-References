---
title: CustomXmlSchemaCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words pour .NET
description: Découvrez comment la méthode CustomXmlSchemaCollection Add améliore votre gestion XML en ajoutant de manière transparente des éléments à votre collection pour des performances optimales.
type: docs
weight: 30
url: /fr/net/aspose.words.markup/customxmlschemacollection/add/
---
## CustomXmlSchemaCollection.Add method

Ajoute un élément à la collection.

```csharp
public void Add(string value)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| value | String | L'élément à ajouter. |

## Exemples

Montre comment travailler avec une collection de schémas XML.

```csharp
Document doc = new Document();

string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello, World!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

// Ajouter une association de schéma XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Cloner la collection d'associations de schéma XML de la partie XML personnalisée,
// puis ajoutez quelques nouveaux schémas au clone.
CustomXmlSchemaCollection schemas = xmlPart.Schemas.Clone();
schemas.Add("http://www.w3.org/2001/XMLSchema-instance");
schemas.Add("http://schemas.microsoft.com/office/2006/metadata/contentType");

Assert.AreEqual(3, schemas.Count);
Assert.AreEqual(2, schemas.IndexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Énumérer les schémas et imprimer chaque élément.
using (IEnumerator<string> enumerator = schemas.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine(enumerator.Current);
}

// Vous trouverez ci-dessous trois manières de supprimer des schémas de la collection.
// 1 - Supprimer un schéma par index :
schemas.RemoveAt(2);

// 2 - Supprimer un schéma par valeur :
schemas.Remove("http://www.w3.org/2001/XMLSchema");

// 3 - Utilisez la méthode « Clear » pour vider la collection en une seule fois.
schemas.Clear();

Assert.AreEqual(0, schemas.Count);
```

### Voir également

* class [CustomXmlSchemaCollection](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
