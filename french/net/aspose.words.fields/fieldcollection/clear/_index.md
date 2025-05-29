---
title: FieldCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words pour .NET
description: Effacez facilement tous les champs de votre FieldCollection grâce à notre méthode Clear. Simplifiez la gestion de vos documents et gagnez en efficacité dès aujourd'hui !
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldcollection/clear/
---
## FieldCollection.Clear method

Supprime tous les champs de cette collection du document et de cette collection elle-même.

```csharp
public void Clear()
```

## Exemples

Montre comment supprimer des champs d'une collection de champs.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder.InsertField(" TIME ");
builder.InsertField(" REVNUM ");
builder.InsertField(" AUTHOR  \"John Doe\" ");
builder.InsertField(" SUBJECT \"My Subject\" ");
builder.InsertField(" QUOTE \"Hello world!\" ");
doc.UpdateFields();

FieldCollection fields = doc.Range.Fields;

Assert.AreEqual(6, fields.Count);

// Vous trouverez ci-dessous quatre manières de supprimer des champs d’une collection de champs.
// 1 - Obtenir un champ pour qu'il se supprime lui-même :
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Récupérer la collection pour supprimer un champ que nous passons à sa méthode de suppression :
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - Supprimer un champ d'une collection à un index :
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - Supprimez tous les champs de la collection en une seule fois :
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

### Voir également

* class [FieldCollection](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
