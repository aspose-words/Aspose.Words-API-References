---
title: CustomXmlSchemaCollection.IndexOf
second_title: Référence de l'API Aspose.Words pour .NET
description: CustomXmlSchemaCollection méthode. Renvoie lindex de base zéro de la valeur spécifiée dans la collection.
type: docs
weight: 70
url: /fr/net/aspose.words.markup/customxmlschemacollection/indexof/
---
## CustomXmlSchemaCollection.IndexOf method

Renvoie l'index de base zéro de la valeur spécifiée dans la collection.

```csharp
public int IndexOf(string value)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| value | String | La valeur sensible à la casse à localiser. |

### Return_Value

L'indice de base zéro. Valeur négative si introuvable.

### Exemples

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

* class [CustomXmlSchemaCollection](../)
* espace de noms [Aspose.Words.Markup](../../customxmlschemacollection/)
* Assemblée [Aspose.Words](../../../)


