---
title: FieldCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words pour .NET
description: FieldCollection Remove méthode. Supprime le champ spécifié de cette collection et du document en C#.
type: docs
weight: 50
url: /fr/net/aspose.words.fields/fieldcollection/remove/
---
## FieldCollection.Remove method

Supprime le champ spécifié de cette collection et du document.

```csharp
public void Remove(Field field)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| field | Field | Un champ à supprimer. |

## Exemples

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

* class [Field](../../field/)
* class [FieldCollection](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
