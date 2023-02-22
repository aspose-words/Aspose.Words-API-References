---
title: CustomXmlSchemaCollection.RemoveAt
second_title: Référence de l'API Aspose.Words pour .NET
description: CustomXmlSchemaCollection méthode. Supprime une valeur à lindex spécifié.
type: docs
weight: 90
url: /fr/net/aspose.words.markup/customxmlschemacollection/removeat/
---
## CustomXmlSchemaCollection.RemoveAt method

Supprime une valeur à l'index spécifié.

```csharp
public void RemoveAt(int index)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| index | Int32 | L'indice de base zéro. |

### Exemples

Montre comment travailler avec une collection de schémas XML.

```csharp
Document doc = new Document();

string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello, World!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

// Ajouter une association de schéma XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Clone la collection d'associations de schémas XML de la partie XML personnalisée,
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
// 1 - Supprimer un schéma par index :
schemas.RemoveAt(2);

// 2 - Supprimer un schéma par valeur :
schemas.Remove("http://www.w3.org/2001/XMLSchema");

// 3 - Utilisez la méthode "Clear" pour vider la collection d'un coup.
schemas.Clear();

Assert.AreEqual(0, schemas.Count);
```

### Voir également

* class [CustomXmlSchemaCollection](../)
* espace de noms [Aspose.Words.Markup](../../customxmlschemacollection/)
* Assemblée [Aspose.Words](../../../)


