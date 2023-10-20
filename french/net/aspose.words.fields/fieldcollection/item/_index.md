---
title: FieldCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words pour .NET
description: FieldCollection Item propriété. Renvoie un champ à lindex spécifié en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldcollection/item/
---
## FieldCollection indexer

Renvoie un champ à l'index spécifié.

```csharp
public Field this[int index] { get; }
```

| Paramètre | La description |
| --- | --- |
| index | Un index dans la collection. |

## Remarques

L'indice est de base zéro.

Les index négatifs sont autorisés et indiquent un accès depuis l'arrière de la collection. Par exemple -1 signifie le dernier élément, -2 signifie l'avant-dernier et ainsi de suite.

Si l'index est supérieur ou égal au nombre d'éléments de la liste, cela renvoie une référence nulle.

Si l'index est négatif et que sa valeur absolue est supérieure au nombre d'éléments de la liste, cela renvoie une référence nulle.

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
