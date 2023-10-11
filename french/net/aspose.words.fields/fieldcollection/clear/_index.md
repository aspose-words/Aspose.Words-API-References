---
title: FieldCollection.Clear
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldCollection méthode. Supprime tous les champs de cette collection du document et de cette collection ellemême.
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldcollection/clear/
---
## FieldCollection.Clear method

Supprime tous les champs de cette collection du document et de cette collection elle-même.

```csharp
public void Clear()
```

### Exemples

Montre comment supprimer des champs d’une collection de champs.

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

// Vous trouverez ci-dessous quatre façons de supprimer des champs d'une collection de champs.
// 1 - Récupère un champ à supprimer :
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Récupère la collection pour supprimer un champ que l'on passe à sa méthode de suppression :
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - Supprime un champ d'une collection à un index :
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - Supprimez tous les champs de la collection d'un coup :
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

### Voir également

* class [FieldCollection](../)
* espace de noms [Aspose.Words.Fields](../../fieldcollection/)
* Assemblée [Aspose.Words](../../../)


