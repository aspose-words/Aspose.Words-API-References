---
title: FieldChar.GetField
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldChar méthode. Renvoie un champ pour le champ car.
type: docs
weight: 40
url: /fr/net/aspose.words.fields/fieldchar/getfield/
---
## FieldChar.GetField method

Renvoie un champ pour le champ car.

```csharp
public Field GetField()
```

### Return_Value

Un champ pour le champ char.

### Remarques

Un nouveau[`Field`](../../field/) l'objet est créé chaque fois que la méthode est appelée.

### Exemples

Montre comment travailler avec un nœud FieldStart.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.Format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

FieldChar fieldStart = field.Start;

Assert.AreEqual(FieldType.FieldDate, fieldStart.FieldType);
Assert.AreEqual(false, fieldStart.IsDirty);
Assert.AreEqual(false, fieldStart.IsLocked);

// Récupère l'objet façade qui représente le champ dans le document.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Met à jour le champ pour afficher la date actuelle.
field.Update();
```

### Voir également

* class [Field](../../field/)
* class [FieldChar](../)
* espace de noms [Aspose.Words.Fields](../../fieldchar/)
* Assemblée [Aspose.Words](../../../)


